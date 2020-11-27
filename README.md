# 2020-2-OSSP-3P-1

# 프로젝트 주제 : 

- 공공데이터를 활용하여 창업 예정자들의 성공적 창업을 돕는 상권 분석 모델 개발

# 주제 선정 배경 : 

### 최근 노년층의 정년퇴직 시기가 빨라지고 청년들의 취업난이 심해짐에 따라 창업을 통해 자신만의 사업을 계획하는 사람들이 늘어나고 있다.

우리나라의 창업 유형은 주로 ‘생계형 창업’에 해당한다. 
생계형 창업이란 도∙소매업과 숙박∙외식업 등 부가가치는 낮지만 진입장벽이 낮아 쉽게 시작할 수 있는 업종을 바탕으로 한 창업을 의미한다. 



### 하지만 생계형 창업의 생존 가능성은 매우 낮다. 

2018년 중소벤처기업부의 자료에 의하면 주로 생계형 창업에 해당하는 숙박∙외식업과 도∙소매업의 2년차 생존률은 각각 42.3%와 45.4%에 불과했고, 5년차 생존률은 각각 17.9%와 24.2%에 불과함으로써 업종 자체뿐만 아니라 타 업종과 비교해봤을 때도 낮은 생존률을 기록했다. 

### < 서울 1496개 상권별 폐업률 >
![캡처](https://user-images.githubusercontent.com/72516027/99644512-5fc06180-2a91-11eb-8abf-5b3a63ceeb38.PNG)
 ㄴ 대체로 폐업률이 0% 에서 15% 사이에 위치하고 있지만 30%까지, 혹은 60% 가까이 치솟는 폐업률을 예측하는 것이 우리 모델의 Goal 이다.
 
 ㄴ 단순한 회귀 분석으로는 위와같이 치솟는 폐업률을 예측하기가 불가능하고, 보다 정교한 모델링이 있어야 해당 폐업률을 예측할 수 있다. 

### 생계형 창업의 생존 가능성을 높이기 위해서는 창업 전 철저한 사전준비가 필요하다. 

생계형 창업은 진입장벽이 낮아 쉽게 접근할 수 있다는 장점을 갖지만 이는 반대로 누구나 쉽게 유사한 업종을 개업하고 운영할 수 있다는 것을 의미하기도 한다. 경쟁 속에서 생계형 창업이 성공하기 위해서는 철저한 상권 분석을 바탕으로 다른 업체들과 차별화된 전략을 설정하여 경쟁 우위를 확보하고, 보다 유리한 입지를 선정할 필요가 있다. 



### 하지만 이러한 상권분석은 실제로 잘 이루어지지 않는다. 

2019년 통계청의 조사에 따르면 당해 기준 1년 이내에 사업을 시작한 자영업자 중 준비기간이 1~3개월 미만인 비중이 전체의 약 52.3%에 달했다. 이는 많은 창업자들이 철저한 준비 없이 바로 창업에 뛰어든다는 점을 알려준다.



### 따라서 본 조는 이번 프로젝트를 통해 창업 예정자의 성공적인 창업을 돕는 상권 분석 모델을 도출해내고자 한다. 

따라서 창업 예정자들은 해당 모델을 사용하여 상권 분석 정보를 쉽게 획득할 수 있음과 동시에 창업 최적 입지를 선정하고 운영 전략을 설정하는 데에 해당 정보를 사용할 수 있을 것이다. 
이를 통해 창업 예정자의 성공적인 창업을 지원하며 거시적으로는 활발한 창업 생태계를 조성하고 시장 경제 활성화에 기여할 수 있을 것이다.


### 딥러닝 기법(RNN), 회귀분석 기법(ARIMA), 머신러닝 기법(Xgboost) 을 통해 작년 1년동안의 데이터로 미래(다음 분기)의 폐업률을 예측하는 모델을 만든다.
ex) Xgboost의 미래 폐업률 예측 ( 파란 선 : 예측한 폐업률 , 주황 선 : 실제 폐업률 , 갈색 선 : 예측 값과 실제 값이 일치하는 경우
![image](https://user-images.githubusercontent.com/72516027/100472136-fee2fa00-311e-11eb-8f9a-ff849a445cc3.png)
### 그리고 과거의 어떤 요인이 다음 분기 폐업률을 예측하는데 큰 영향을 주는지 알아본다.
ex) Xgboost로 알아본 다음 분기 폐업률 예측시 중요한 요소 ( 데이터 : 강남구 )
![image](https://user-images.githubusercontent.com/72516027/100472149-04d8db00-311f-11eb-9067-e2e2e6d2ba57.png)
작년 같은 분기의 유동인구수가 미래 폐업률 예측시 매우 중요한 요소임을 알 수 있다.

