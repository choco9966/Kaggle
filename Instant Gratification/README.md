# [Instant Gratification]( https://www.kaggle.com/c/instant-gratification/overview )

![](https://drive.google.com/uc?export=view&id=13WiJAbB1eVdeZojqKFCNtSkls9bf4m0i)

## Abstract 

- Host : Kaggle 
- Objective : A synchronous Kernels-only competition
- Evaluation : AUC
- Period :  2019.05.21 ~ 2019.06.20

## Preprocessing 
1. Feature Selection with variance 
2. KERNEL PCA

Try and Fail : PCA, SVD, AutoEncoder, DAE etc

## Feature Engineering 
We used the following three methods to make variable of the distribution of the dataset.
1. GMM_PRED 
2. GMM_SCORE
3. HIST_PRED
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&amp;fname=https%3A%2F%2Fk.kakaocdn.net%2Fdn%2FcdwpIM%2Fbtqwfl7ksHu%2FHrOefi5xBBPdVrJGSd2tSk%2Fimg.png)

## Model
- 1st layer : Nusvc + Nusvc2 + qda + svc + knn + lr / Stratified with GMM_LABEL 
- 2nd layer : Lgbm + mlp / Stratified
- 3rd layer : 1st layer + 2st layer / Average
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&amp;fname=https%3A%2F%2Fk.kakaocdn.net%2Fdn%2FVj3FG%2Fbtqwf3ylVfO%2FvvVCmYTe7z4TFIn8AKkSK1%2Fimg.png)

## Private Test with Make Classification
the process is as follows.
- 1. Estimate the number of private magic n(0~511) has number using the linear relationship between the number of magic and auc.
(ex. private magic 0 auc 0.97xx then magic number 250) 
- 2. Create public and private data by seed using make_classification with estimated magic number.
- 3. Test Model with maked public, private dataset and check score cv, pb, v
- 4. Finally, choose a model with cv + pb + pv close to 0.975. Others thought that overfitting.
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&amp;fname=https%3A%2F%2Fk.kakaocdn.net%2Fdn%2FcsSklH%2FbtqweIV0tL1%2FecqDnPjxbQ0CKLUPodtEm0%2Fimg.png)
But actually it did not work out.

## Result 
- 4% Rank (70/1832)
![](https://drive.google.com/uc?export=view&id=17W3OLw22PBKGBENRut7YwOTdOQjNdMjO)
| submission | Public LB | Rank | Private LB | Rank |
| :--------: | :-------: | :--: | :--------: | :--: |
|   Model1   |  0.97491  |  19  |  0.97536   |  70  |
|    Best    |  0.97432  |  -   |  0.97611   |  1   |
- Best Score
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&amp;fname=https%3A%2F%2Fk.kakaocdn.net%2Fdn%2FbX5sHq%2FbtqwfkURVtU%2FNzDybSbf4K5mKcC6whKhf0%2Fimg.png)
