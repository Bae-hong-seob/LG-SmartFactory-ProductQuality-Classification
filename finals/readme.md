## [LG Aimers 스마트 공장 제품 품질 상태 분류 AI 온라인 해커톤 - 본선('23.03.25 ~ '23.03.26)](https://dacon.io/competitions/official/236080/overview/description)


## Try:
feature 증가 (2875 -> 3326) 으로 인해 Curse of dimensionality 예상
    - corr 기준 feature elimination
    - corr 기준 threshold(0.9) 이상 PCA를 통해 하나의 feature로 통합.
    
## Solution: Multi model 구축 및 Dicision Boundary를 Decision Tree를 사용하여 동적 조절
  - 예선전 데이터 model 1
  - 본선 데이터 model 2
  - 전체 데이터 model 3
