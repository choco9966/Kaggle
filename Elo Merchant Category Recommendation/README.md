# [Elo Merchant Category Recommendation]( https://www.kaggle.com/c/elo-merchant-category-recommendation/overview )

![](https://drive.google.com/uc?export=view&id=1M2sW7AR91uV25P86wC92bBjhwMe1uci3)

## Abstract 

- Host : Elo
- Objective : Predicted loyalty score of customers (Regression)
- Evaluation : RMSE 
- Period :  2018.11.01 ~ 2019.01.30

Imagine being hungry in an unfamiliar part of town and getting restaurant recommendations served up, based on your personal preferences, at just the right moment. The recommendation comes with an attached discount from your credit card provider for a local place around the corner!

Right now, [Elo](https://www.cartaoelo.com.br/), one of the largest payment brands in Brazil, has built partnerships with merchants in order to offer promotions or discounts to cardholders. But do these promotions work for either the consumer or the merchant? Do customers enjoy their experience? Do merchants see repeat business? Personalization is key.

Elo has built machine learning models to understand the most important aspects and preferences in their customers’ lifecycle, from food to shopping. But so far none of them is specifically tailored for an individual or profile. This is where you come in.

In this competition, Kagglers will develop algorithms to identify and serve the most relevant opportunities to individuals, by uncovering signal in customer loyalty. Your input will improve customers’ lives and help Elo reduce unwanted campaigns, to create the right experience for customers.

## Result 

![](https://drive.google.com/uc?export=view&id=1CUCI13QSTDnR2eklHwRus2shqmm4CTUk)

| submission | Public LB | Rank | Private LB | Rank |
|:----------:|:---------:|:----:|:----------:|:----:|
|  Ensemble1 |  3.64604  |  10  |   3.61587  |  978 |
|  Ensemble2 |  3.65602  |  20  |   3.60859  |  86  |
|    Best    |  3.67812  |  193 |   3.60389  |  34  |

## Fold

```
.
├── code
│   ├── EDA
│   │   └── 1. Data Exploratory Analysis.ipynb
│   ├── PREPROCESSING
│   │   └── 2. Preprocessing.ipynb
│   ├── FEATURES
│   │   └── 3. Features.ipynb
│   ├── MODEL
|   │   └── 4. Modeling_Lightgbm_Model1.ipynb
|   │   └── 4. Modeling_Lightgbm_Model2.ipynb
├── Solution
│   ├── Code
│   ├── Discussion
└── Experience
```

## How to Run 

**[Data]**

Place data in `input` directory. You can download data from [here]( https://www.kaggle.com/c/elo-merchant-category-recommendation/data)

**[Code]** 

Above results can be replicated by running 

```
python code/main.py 
```

Make sure you are on windows with library versions same as specified in [requirements.txt](https://github.com/choco9966/Kaggle/blob/master/Elo%20Merchant%20Category%20Recommendation/requirements.txt)

**[Submit]**

Submit the resulting csv file [here]( https://www.kaggle.com/c/elo-merchant-category-recommendation/submit ) and verify the [score]( https://www.kaggle.com/c/elo-merchant-category-recommendation/leaderboard )

