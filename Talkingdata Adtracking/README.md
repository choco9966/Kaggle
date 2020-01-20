# [TalkingData AdTracking Fraud Detection Challenge]( https://www.kaggle.com/c/talkingdata-adtracking-fraud-detection/ )

![](https://github.com/choco9966/Kaggle/blob/master/Talkingdata%20Adtracking/image/header.png?raw=true)

## Abstract 

- Host : TalkingData
- Objective :  To build an algorithm that predicts whether a user will download an app after clicking a mobile app ad (Classification)
- Evaluation : AUC
- Period :  2018.3.01 ~ 2019.04.30

Fraud risk is everywhere, but for companies that advertise online, click fraud can happen at an overwhelming volume, resulting in misleading click data and wasted money. Ad channels can drive up costs by simply clicking on the ad at a large scale. With over 1 billion smart mobile devices in active use every month, China is the largest
mobile market in the world and therefore suffers from huge volumes of fradulent traffic.

[TalkingData](https://www.talkingdata.com/), China’s largest independent big data service platform, covers over 70% of active mobile devices nationwide. They handle 3 billion clicks per day, of which 90% are potentially fraudulent. Their current approach to prevent click fraud for app developers is to measure the journey of a user’s click across their portfolio, and flag IP addresses who produce lots of clicks, but never end up installing apps. With this information, they've built an IP blacklist and device blacklist.

While successful, they want to always be one step ahead of fraudsters and have turned to the Kaggle community for help in further developing their solution. In their 2nd competition with Kaggle, you’re challenged to build an algorithm that predicts whether a user will download an app after clicking a mobile app ad. To support your modeling, they have provided a generous dataset covering approximately 200 million clicks over 4 days!

## Result 

- 11% Rank (405 / 3948)

![](https://github.com/choco9966/Kaggle/blob/master/Talkingdata%20Adtracking/image/result.PNG?raw=true)

| submission | Public LB | Rank | Private LB | Rank |
| :--------: | :-------: | :--: | :--------: | :--: |
|   Model1   |  0.98115  | 449  |  0.98195   | 406  |

