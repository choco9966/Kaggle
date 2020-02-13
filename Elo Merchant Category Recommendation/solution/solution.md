# 우승자의 아이디어

## 데이터 전처리 

![img](https://k.kakaocdn.net/dn/34Hnx/btqyfN14pqn/EC5OPuvhaSgAb7lEV1AYkk/img.png)

데이터는 Historical.csv , New merchant historical.csv, Merchants.csv 3가지와 변수의 조합에 따라서 나눈것이 인상적이었음. authorized_flag라는 거래가 성사 되었는지 여부라는 중요한 피쳐로 데이터를 분리해서 사용하거나 Month_lag로 달마다 데이터를 나누어서 사용. 

## 변수 생성

- 기본적인 연산, 통계값 

![img](https://k.kakaocdn.net/dn/rNa3k/btqyenC01Mh/k2m7MYitOflrxdwAP2Kqo1/img.png)

- purchase_amount_new : 기존의 시뮬레이션된 데이터가 어떻게 나온 것인지를 해석해서 만든 새로운 변수. 
  - https://www.kaggle.com/raddar/target-true-meaning-revealed
  - https://www.kaggle.com/raddar/towards-de-anonymizing-the-data-some-insights
  - purchase_amount_new만 사용했을때에는 의미 없었고 둘을 같이 사용하면 의미가 있었음 !!!

- 3에서는 max의 비율을 계산했는데 단순 빼기도 굉장히 중요한 변수 였음. 
- 카테고리 변수 

![img](https://k.kakaocdn.net/dn/doS3Wz/btqyfq0kDVN/MclxSWIKNtl4gmqk7mk4R1/img.png)

- historical과 new_merchant_historical에 있는 카테고리 정보의 손실을 막기 위한 방법. 
- **Word2Vec :** 단어의 유사도를 계산하는 방법(https://eda-ai-lab.tistory.com/118)
- **Fasttext :** Word2Vec를 기본으로 부분단어(subword)의 벡터들로 표현한다는 점. 예를들어, 영화가 들어오면 영화다, 영화였다, 작품, 영화임 이런식으로 나옴. 

위의 두가지는 보통 **단어**에 사용하는 방법. 이것을 카테고리형의 데이터에 적용하는게  신기했음. 여러개의 카테고리 변수들을 이은 다음에 Word2vec과 FastText 적용. 

- SVC : Support vector classifier인데 이것을 어떻게 활용하였는지는 잘 모르겠음. 
- Counter Vectorizer + SVD, PCA : 원핫인코딩형태로 만든 다음에 SVD, PCA를 사용하여 차원을 축소. 
- frequency : Frequency Encoding으로 각 값이 나온 빈도로 교체 

- 그 외

![img](https://k.kakaocdn.net/dn/vrxVZ/btqyfX4tMIx/d6yLv21Qfikd9BMWsM3waK/img.png)

## 변수 선택 

![img](https://k.kakaocdn.net/dn/cetTSh/btqygsv8DqB/YGx1gHB1xk3DsYmsifBpDK/img.png)

 참고링크 ; http://otzslayer.github.io/machine-learning/feature-selection/

- Null Importance
  - 참고링크 : https://www.kaggle.com/ogrellier/feature-selection-with-null-importances
- RFE(Recursive Feature Elimination) : 코드 http://blog.datadive.net/selecting-good-features-part-iv-stability-selection-rfe-and-everything-side-by-side/ : RF를 이용하여 변수의 조합을 만들어내고 가장 좋았던 케이스를 선택.
- LGB 
- Boruta
  - 참고링크 : http://otzslayer.github.io/machine-learning/boruta-algorithm/
- Adversarial validation 

## 트릭

![img](https://k.kakaocdn.net/dn/bg9Xqd/btqygCedMfD/cYEWpWZ3NcY8Q2YjyT8jbk/img.png)

 