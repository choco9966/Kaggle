# [Instant Gratification]( https://www.kaggle.com/c/instant-gratification/overview )

![](https://drive.google.com/uc?export=view&id=13WiJAbB1eVdeZojqKFCNtSkls9bf4m0i)

## Abstract 

- Host : Kaggle 
- Objective : A synchronous Kernels-only competition
- Evaluation : AUC
- Period :  2019.05.21 ~ 2019.06.20

## Result 

- 4% Rank (70/1832)

![](https://drive.google.com/uc?export=view&id=17W3OLw22PBKGBENRut7YwOTdOQjNdMjO)

| submission | Public LB | Rank | Private LB | Rank |
| :--------: | :-------: | :--: | :--------: | :--: |
|   Model1   |  0.97491  |  19  |  0.97536   |  70  |
|    Best    |  0.97432  |  -   |  0.97611   |  1   |

## Fold

```
.
├── code
│   ├── EDA
│   │   └── Data Exploratory Analysis.ipynb
│   ├── MODEL
|   │   └── Model.ipynb
├── Solution
│   ├── Code
│   ├── Discussion
└── Experience
```

## How to Run 

**[Data]**

Place data in `input` directory. You can download data from [here]( https://www.kaggle.com/c/instant-gratification/data)

**[Code]** 

Above results can be replicated by running 

```
python code/main.py 
```

Make sure you are on windows with library versions same as specified in [requirements.txt](https://github.com/choco9966/Kaggle/blob/master/Elo%20Merchant%20Category%20Recommendation/requirements.txt)

**[Submit]**

Submit the resulting csv file [here]( https://www.kaggle.com/c/instant-gratification/submit ) and verify the [score]( https://www.kaggle.com/c/instant-gratification/leaderboard )

