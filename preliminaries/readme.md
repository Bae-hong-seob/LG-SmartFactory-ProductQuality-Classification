## [LG Aimers 스마트 공장 제품 품질 상태 분류 AI 온라인 해커톤 - 예선('23.02.01 ~ '23.02.28)](https://dacon.io/competitions/official/236055/overview/description)

# 1. EDA 진행
# 2. Try
  - Try1 : feature selection
    - 전진 선택법
    - 후진 소거법
    - VIF 기준 제거
    - RFE(Recursive Feature Elimination) 
  - Try2 : Handling missing value
    - 공장별 mean, median, mode, iterativeimputer 기법 적용
    - 제품별 mean, median, mode, iterativeimputer 기법 적용
  - Try3 : semi-supervised learning 시도
    - test dataset에 Y_Quality column 추가 -> Y_Class 예측
  - Try4 : Data Augmentation
    - CTGAN 사용
  - Try5 : tablur dataset -> Graph dataset 구축
    - GNN(GCN 적용)
  - Try6 : Modeling 비교
    - Linear, Lasso, Ridge, Elastic net
    - GBM, LGBM, Catboost
    - DT, RF
    - GCN

# 3. solution
  - feature selection : 하지 않는게 public score 상 best
  - Handling missing value : -1로 결측치 대체
  - Y_Quality log transformation 적용
  - PRODCUT 별로 multi model 구축
  - 평가 방식 Macro F1 score 에 따른 decision boundary 수정
