# [Santander Customer Transaction Prediction]( https://www.kaggle.com/c/santander-customer-transaction-prediction )

![](https://drive.google.com/uc?export=view&id=1F6psWqrJzLkYUdK5AwjK5Mm8vLzW1e8H)

## Abstract 

- Host : Santander
- Objective : Can you identify who will make a transaction? (Classification) 
- Evaluation : AUC
- Period :  2019.2.01 ~ 2019.04.10

At [Santander](https://www.santanderbank.com/) our mission is to help people and businesses prosper. We are always looking for ways to help our customers understand their financial health and identify which products and services might help them achieve their monetary goals.

Our data science team is continually challenging our machine learning algorithms, working with the global data science community to make sure we can more accurately identify new ways to solve our most common challenge, binary classification problems such as: is a customer satisfied? Will a customer buy this product? Can a customer pay this loan?

In this challenge, we invite Kagglers to help us identify which customers will make a specific transaction in the future, irrespective of the amount of money transacted. The data provided for this competition has the same structure as the real data we have available to solve this problem.

## Result 

- 0.4% Rank (38/8802)

![](https://drive.google.com/uc?export=view&id=1NUXoYyOiDKo7E6UtzhSQX1dQdYjTWrDp)

| submission | Public LB | Rank | Private LB | Rank |
| :--------: | :-------: | :--: | :--------: | :--: |
|   Model1   |  0.92399  |  32  |  0.92245   |  38  |

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

Place data in `input` directory. You can download data from [here]( https://www.kaggle.com/c/santander-customer-transaction-prediction/data)

**[Code]** 

Above results can be replicated by running 

```
python code/main.py 
```

Make sure you are on windows with library versions same as specified in [requirements.txt](https://github.com/choco9966/Kaggle/blob/master/Elo%20Merchant%20Category%20Recommendation/requirements.txt)

**[Submit]**

Submit the resulting csv file [here]( https://www.kaggle.com/c/santander-customer-transaction-prediction/submit ) and verify the [score]( https://www.kaggle.com/c/santander-customer-transaction-prediction/leaderboard )

