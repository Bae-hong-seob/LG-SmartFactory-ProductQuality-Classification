[LG Aimers 스마트 공장 제품 품질 상태 분류 AI 온라인 해커톤 - 예선전](https://dacon.io/competitions/official/236055/overview/description)

1. EDA 진행
2. Try
  Try1 : feature selection(전진 선택법, 후진 소거법, VIF 기준 제거) and RFE(Recursive Feature Elimination) 시도
  Try2 : Handling missing value(공장별 or 제품별 mean, median, mode, iterativeimputer 기법 적용)
  Try3 : semi-supervised learning 시도(test dataset에 Y_Quality column 추가 -> Y_Class 예측)
  Try4 : Data Augmentation(CTGAN 사용)
  Try5 : tablur dataset -> Graph dataset 구축, GNN(GCN 적용)
  
# Dataset Info.
train.csv [파일] 598(rows) * 2881(columns)  
PRODUCT_ID : 제품의 고유 ID  
Y_Class : 제품 품질 상태(Target) (0 : 기준 미달, 1 : 적합, 2 : 기준 초과)  
Y_Quality : 제품 품질 수치  
TIMESTAMP : 제품이 공정에 들어간 시각  
LINE : 제품이 들어간 공정 LINE 종류 ('T050304', 'T050307', 'T100304', 'T100306', 'T010306', 'T010305' 존재)  
PRODUCT_CODE : 제품의 CODE 번호 ('A_31', 'T_31', 'O_31' 존재)  
X_1 ~ X_2875 : 공정 과정에서 추출되어 비식별화된 변수  

test.csv [파일]  
PRODUCT_ID : 제품의 고유 ID  
TIMESTAMP : 제품이 공정에 들어간 시각  
LINE : 제품이 들어간 공정 LINE 종류 ('T050304', 'T050307', 'T100304', 'T100306', 'T010306', 'T010305' 존재)  
PRODUCT_CODE : 제품의 CODE 번호 ('A_31', 'T_31', 'O_31' 존재)  
X_1 ~ X_2875 : 공정 과정에서 추출되어 비식별화된 변수  

sample_submission.csv [파일] - 제출 양식  
PRODUCT_ID : 제품의 고유 ID  
Y_Class : 예측한 제품 품질 상태 (0 : 기준 미달, 1 : 적합, 2 : 기준 초과)  
