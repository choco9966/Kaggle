# [Instant-gratification]( https://www.kaggle.com/c/instant-gratification/ )

![](https://drive.google.com/uc?export=view&id=13WiJAbB1eVdeZojqKFCNtSkls9bf4m0i)

## Abstract 

- Host : Kaggle 
- Objective : A synchronous Kernels only Competition (Kernel Test)
- Evaluation : AUC
- Period :  2019.05.21 ~ 2019.06.20

Welcome to Instant (well, *almost*) Gratification!

In 2015, Kaggle introduced Kernels as a resource to competition participants. It was a controversial decision to add a code-sharing tool to a competitive coding space. We thought it was important to make Kaggle more than a place where competitions are solved behind closed digital doors. Since then, Kernels has grown from its infancy--essentially a blinking cursor in a docker container--into its teenage years. We now have more compute, longer runtimes, better datasets, GPUs, and an improved interface.

We have iterated and tested several Kernels-only (KO) competition formats with a true holdout test set, in particular deploying them when we would have otherwise substituted a [two-stage competition](https://www.kaggle.com/two-stage-frequently-asked-questions). However, the experience of submitting to a Kernels-only competition has typically been asynchronous and imperfect; participants wait many days after a competition has concluded for their selected Kernels to be rerun on the holdout test dataset, the leaderboard updated, and the winners announced. This flow causes heartbreak to participants whose Kernels fail on the unseen test set, leaving them with no way to correct tiny errors that spoil months of hard work.

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
|   │   └── Best.ipynb
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

Submit the resulting csv file [here]( https://www.kaggle.com/c/elo-merchant-category-recommendation/submit ) and verify the [score]( https://www.kaggle.com/c/elo-merchant-category-recommendation/leaderboard )

