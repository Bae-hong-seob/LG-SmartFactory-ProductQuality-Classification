[LG Aimers 스마트 공장 제품 품질 상태 분류 AI 온라인 해커톤 - 예선전](https://dacon.io/competitions/official/236055/overview/description)
  - '23.02.01 ~ '23.02.28

# 1. EDA 진행
# 2. Try
  - Try1 : feature selection(전진 선택법, 후진 소거법, VIF 기준 제거) and RFE(Recursive Feature Elimination) 시도
  - Try2 : Handling missing value(공장별 or 제품별 mean, median, mode, iterativeimputer 기법 적용)
  - Try3 : semi-supervised learning 시도(test dataset에 Y_Quality column 추가 -> Y_Class 예측)
  - Try4 : Data Augmentation(CTGAN 사용)
  - Try5 : tablur dataset -> Graph dataset 구축, GNN(GCN 적용)

# 3. solution
  - feature selection : 하지 않는게 public score 상 best
  - Handling missing value : -1로 결측치 대체
  - PRODCUT 별로 multi model 구축
  - 평가 방식 Macro F1 score 에 따른 decision boundary 수정
