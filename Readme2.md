# 스마트 공장의 제어 시스템 구축을 위한 제품 품질 분류 AI 모델 개발

## Preliminaries(예선전)
  - '23.02.01 ~ '23.02.28
  - online
  - Top 20 team(100명) 진출

## Finals(본선) Public 1st, Private 5st
  - '23.03.25 ~ '23.03.26
  - offline(LG 경기 연수원)
  - Top 3 team 수상
<hr>

Try1 : feature selection
- 전진 선택법, 후진 소거법 
- VIF 기준 제거
- RFE(Recursive Feature Elimination) 

Try2 : Handling missing value
- 공장별 mean, median, mode, iterativeimputer 기법 적용
- 제품별 mean, median, mode, iterativeimputer 기법 적용

Try3 : semi-supervised learning 시도
- test dataset에 Y_Quality column 추가 -> Y_Class 예측

Try4 : Data Augmentation
- CTGAN 사용

Try5 : tablur dataset -> Graph dataset 구축
- GNN(GCN 적용)

Try6 : Modeling 비교
- Linear, Lasso, Ridge, Elastic net
- GBM, LGBM, Catboost
- DT, RF
- GCN

solution:
  - feature selection : 하지 않는게 public score 상 best
  - Handling missing value : -1로 결측치 대체
  - Y_Quality log transformation 적용
  - PRODCUT 별로 multi model 구축
  - 평가 방식 Macro F1 score 에 따른 decision boundary 수정

### Final Try:
feature 증가 (2875 -> 3326) 으로 인해 Curse of dimensionality 예상
    - corr 기준 feature elimination
    - corr 기준 threshold(0.9) 이상 PCA를 통해 하나의 feature로 통합.
    
### Final Solution: Multi model 구축 및 Dicision Boundary를 Decision Tree를 사용하여 동적 조절
  - 예선전 데이터 model 1
  - 본선 데이터 model 2
  - 전체 데이터 model 3
