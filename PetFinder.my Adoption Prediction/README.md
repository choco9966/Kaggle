# [PetFinder.my Adoption Prediction]( https://www.kaggle.com/c/petfinder-adoption-prediction/ )

![](https://drive.google.com/uc?export=view&id=1q31m9Zt5ZN6tMn986V7Bcgr62viqkvOG)

## Abstract 

- Host : PetFinder.my 
- Objective : How cute is that doggy in the shelter? (Multi Classification)
- Evaluation : Kappa
- Period :  2019.03.01 ~ 2019.03.28

Millions of stray animals suffer on the streets or are euthanized in shelters every day around the world. If homes can be found for them, many precious lives can be saved — and more happy families created.

[PetFinder.my](https://petfinder.my/) has been Malaysia’s leading animal welfare platform since 2008, with a database of more than 150,000 animals. PetFinder collaborates closely with animal lovers, media, corporations, and global organizations to improve animal welfare.

Animal adoption rates are strongly correlated to the metadata associated with their online profiles, such as descriptive text and photo characteristics. As one example, PetFinder is currently experimenting with a simple AI tool called the Cuteness Meter, which ranks how cute a pet is based on qualities present in their photos.

In this competition you will be developing algorithms to predict the adoptability of pets - specifically, how quickly is a pet adopted? If successful, they will be adapted into AI tools that will guide shelters and rescuers around the world on improving their pet profiles' appeal, reducing animal suffering and euthanization.

Top participants may be invited to collaborate on implementing their solutions into AI tools for assessing and improving pet adoption performance, which will benefit global animal welfare.

## Result 

![](https://drive.google.com/uc?export=view&id=1fzG3C7jFTS6uSiav9QT65HERcjES0QyD)

| submission | Public LB | Rank | Private LB | Rank |
| :--------: | :-------: | :--: | :--------: | :--: |
|   Model1   |     -     |  -   |  0.42940   |  70  |
|   Model2   |     -     |  -   |  0.43129   |  52  |

## Fold

```
.
├── code
│   ├── MODEL
|   │   └── Model1.ipynb
|   │   └── Model2.ipynb
├── Solution
│   ├── Code
│   ├── Discussion
└── Experience
```

## How to Run 

**[Data]**

Place data in `input` directory. You can download data from [here]( https://www.kaggle.com/c/petfinder-adoption-prediction/data )

**[Code]** 

Above results can be replicated by running 

```
python code/main.py 
```

Make sure you are on windows with library versions same as specified in [requirements.txt](https://github.com/choco9966/Kaggle/blob/master/Elo%20Merchant%20Category%20Recommendation/requirements.txt)

**[Submit]**

Submit the resulting csv file [here]( https://www.kaggle.com/c/petfinder-adoption-prediction/submit ) and verify the [score]( https://www.kaggle.com/c/petfinder-adoption-prediction/leaderboard )
