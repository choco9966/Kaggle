# Public 13th / Private 184th Solution

### 1. Overview 

We selected two versions by increasing the variety of models and models with the highest score on the leaderboard.

**Submission1 (Variety Models)**

- Public LB : 904 Private LB : 899
- Inference Code : https://www.kaggle.com/hihunjin/avengers-assemble-3-model10-tta2?scriptVersionId=54655767

![Submission1](https://drive.google.com/uc?export=view&id=1JRuoN2D1g9VADhwvxFBsfDIV77BknY0K)

**Submission2 (Highest LB)** 

- Public LB : 908 Private LB : 897
- Inference Code : https://www.kaggle.com/chocozzz/sub4-effx3-regx3-tta-3?scriptVersionId=54655742

![Submission2](https://drive.google.com/uc?export=view&id=1QtU3t9qS2g96fuxRBKKsSqWIM9zcwfiZ)

### 2. Tricks or Magics 

- Augmentations : LB 899 to 900 with GridMask

  ```python
  def get_train_transforms():
      return Compose([
              RandomResizedCrop(CFG['img_size'], CFG['img_size']),
              Transpose(p=0.5),
              HorizontalFlip(p=0.5),
              VerticalFlip(p=0.5),
              ShiftScaleRotate(p=0.5),
              HueSaturationValue(hue_shift_limit=0.2, sat_shift_limit=0.2, val_shift_limit=0.2, p=0.5),
              RandomBrightnessContrast(brightness_limit=(-0.1,0.1), contrast_limit=(-0.1, 0.1), p=0.5),
              Normalize(mean=[0.485, 0.456, 0.406], std=[0.229, 0.224, 0.225], max_pixel_value=255.0, p=1.0),
              CoarseDropout(p=0.5),
              GridMask(num_grid=3, p=0.5), # 899 to 900 
              ToTensorV2(p=1.0),
          ], p=1.)
  ```

- Label Smoothing Loss : LB 900 to 901 

  - alpha : 0.2 (When testing values between 0.05 and 0.3, 0.2 was the best score.)

- SWA : LB 901 to 902 

- TTA Inference : LB 902 to 905 

  ```python
  def get_inference_transforms():
      return Compose([
              OneOf([
                  Resize(CFG['img_size'], CFG['img_size'], p=1.),
                  CenterCrop(CFG['img_size'], CFG['img_size'], p=1.),
                  RandomResizedCrop(CFG['img_size'], CFG['img_size'], p=1.)
              ], p=1.), 
              Transpose(p=0.5),
              HorizontalFlip(p=0.5),
              VerticalFlip(p=0.5),
              Resize(CFG['img_size'], CFG['img_size']),
              Normalize(mean=[0.485, 0.456, 0.406], std=[0.229, 0.224, 0.225], max_pixel_value=255.0, p=1.0),
              ToTensorV2(p=1.0),
          ], p=1.)
  ```

  - only CenterCrop : 902 
  - using RandomResized + CenterCrop : 904
  - using Resize + CenterCrop + RandomResizedCrop : 905 

- Optimizer : Adam to Adamp (EfficientNet has reduced performance)

  - VIT : 901 to 902 
  - RegNetY40 : 904 to 905 
  - Eff : 905 to 904
  
- Ensemble (Eff 905 / RegNetY 905 / VIT 902)

  - EFF(2019+2020) + EFF(2020) + EFF(SEED 720) + RegNetY(2019+2020) + RegNetY(2020) + RegNetY(Distillation) : 908
  - EFF(2019+2020) + EFF(2020) + RegNetY(2019+2020) + RegNetY(2020) : 907
  - EFF + RegNetY : 907 
  - EFF + VIT : 906 
  - EFF + VIT + RegNetY : 906 

### 3. Trial and Error 

- Preprocessing : Noise Label Delete (using oof score), Clean Lab, Merging 2019 Dataset 
- Augmentation : Cutmix, Cutout, Fmix, , 5 Crop etc.
- Loss : Bi-Tempered Logistic Loss, Focal Loss, Taylor Loss etc.
- Models : NFNet, BotNet, DeiT, Distillation, Fixmatch 
- Optimizer : Adamw, Adamp (Sometimes it works for each model, and sometimes it doesn't) , RAdam, SAM 
- Ensemble : SEED Ensemble, VIT + RegNetY40 + EfficientNet etc. 
- Others : Batch Normalization Freeze, Hyper parameter Tuning (lr, gradient accum etc), Global Average Pooling to Concatenate Max Pooling and GAP etc. 

You can see our All Training code in the GitHub below. 

- GitHub : https://github.com/choco9966/Cassava-Leaf-Disease-Classification

Lastly, I would like to say thank you to the team members who worked hard for 2 months.@Minyong Shin @bellwood @hihunjin @CY Sohn