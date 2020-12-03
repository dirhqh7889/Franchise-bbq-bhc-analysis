# Franchise-BBQ-BHC-analysis
# 프랜차이즈(BBQ, BHC) 분석

## 문제정의
한국인이 생각하는 배달음식 중 치킨이 1등을 하였다.   
이는 우리가 치킨을 많이 먹고 가장 많이 접한다는 소리이다.   
그 중에서도 치킨을 좋아하는 치킨 갤러리라는 싸이트에서 치킨 브랜드 순위를 정했었다.   
![캡처](https://user-images.githubusercontent.com/59160781/101049835-393d1300-35c7-11eb-85f6-e98fe944fd64.PNG)   

그림을 보면 1위가 BBQ(황금올리브치킨), 2위가 BHC(뿌링클)이였다.   
그러면 과연 치킨 갤러리에서 뽑은 1,2위 치킨중 어느 가게가 더 많은지, 어느 지역에 많이 분포하고 있는지를 분석 해볼것이다.
   
## 데이터 수집
데이터는 공공데이터 포털을 통해 얻었다.   
공공데이터 포털은 공공데이터를 한 곳에서 제공하는 통합 창구로 쉽고 편리하게 공공데이터를 얻을 수 있다.   
   
수집한 데이터:   
상가업소정보_201912_01.csv   

## 데이터 전처리
1. 파일에서 컬럼이 총 39개나 되기 때문에 전처리를 통해 핵심부분만 표시하여 11개의 컬럼으로 줄였다.   
2. 음식부분의 치킨이 아닌 관련없는 소매부분의 데이터가 있어 제외했다.   
3. 음식부분이고 같은 이름을 공유하지만 BBQ, BHC 프랜차이즈가 아닌 가게들을 제외하였다.   
   
## 데이터 모델링
BBQ와 BHC라고 해서 상호명이 무조건 BBQ와 BHC가 아닌 여러 이름들(EX.BHC치킨은평뉴타운점)이 있기 때문에    
브랜드명 컬럼을 생성하여 BBQ와 BHC로 통일시켰다.   

## 시각화 및 탐색
### 서울의 BBQ, BHC 개수
![서울 치킨 갯수](https://user-images.githubusercontent.com/59160781/101051367-c0d75180-35c8-11eb-9a97-c29088945e31.PNG)
### 구별 BBQ, BHC 개수
![구별 치킨 갯수](https://user-images.githubusercontent.com/59160781/101051441-dba9c600-35c8-11eb-9a79-77d91b7316cc.PNG)
### 서울 전체 분포 지도(folium이용)
![지도 치킨 갯수](https://user-images.githubusercontent.com/59160781/101051488-e9f7e200-35c8-11eb-8faf-d8acbe66f85d.PNG)
### 서울 전체 분포 지도(heatmap이용)
![구별 치킨 갯수3](https://user-images.githubusercontent.com/59160781/101051807-380ce580-35c9-11eb-8875-c670042c5c8b.PNG)
### 서울 지역별 분포 지도(MarkerCluster이용)
![구별 치킨 갯수2](https://user-images.githubusercontent.com/59160781/101051544-fa0fc180-35c8-11eb-8418-c8216e118cbe.PNG)





