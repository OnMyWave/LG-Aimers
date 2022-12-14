# LG-Aimers 
2022 LG Aimers : 자율주행 센서 안테나 성능예측 

# 개요

## 배경
    Radar는 자율주행 차에 있어 차량과의 거리, 상대 속도, 방향 등을 측정해주는 필수적인 센서 부품입니다. 
    전기자동차, 자율주행차, 로보택시, 자율주행 택배로봇 등 Radar가 활용되는 시장은 점차 커지고 있으며,
    제품 종류도 기존 단거리, 중거리 및 장거리 Radar 뿐 아니라 차량 실내용 및 4D 이미징 Radar 등 다변화 되는 추세입니다.
    LG에서는 제품의 성능 평가 공정에서 양품과 불량을 선별하고 있습니다.
    그리고 AI 기술을 활용하여 공정 데이터와 제품 성능간 상관 분석을 통해 제품의 불량을 예측/분석하고, 
    수율을 극대화하여 불량으로 인한 제품 폐기 비용을 감축 시키기 위해 노력하고 있습니다.

## 목적
공정 데이터를 활용하여 Radar 센서의 안테나 성능 예측을 위한 AI 모델 개발

# 분석

## Dataset
1. 학습(Train) 데이터셋 (39607개)

파일명: train.csv
설명: ID, X Feature(56개), Y Feature(14개)


2. 테스트(Test) 데이터셋 (39608개)

파일명: test.csv
설명: ID, X Feature(56개)


3. sample_submission.csv (제출양식)

설명 : ID, 예측한 Y Feature(14개)


4. ./meta/x_feature_info.csv

설명: 비식별화된 X Feature에 대한 세부 설명 자료


5. ./meta/y_feature_info.csv

설명 : 비식별화된 Y Feature에 대한 세부 설명 자료


6. ./meta/y_feature_spec_info.csv

설명 : 각 샘플의 정상, 불량을 판정할 수 있는 Y Feature 별 스펙 기준 자료 
실제 공정 과정에서의 데이터로, 대회 진행을 위해 해당 스펙 값들은 임의 조정된 상태입니다.

## 사용 Tool
### Pycaret : https://pycaret.org/guide/
    AutoML을 하게 해주는 파이썬 라이브러리입니다. 
    scikit-learn 패키지를 기반으로 하고 있으며 Classification, Regression, Clustering, Anomaly Detection 등등 다양한 모델을 지원합니다.
    PyCaret은 적은 코드로 머신러닝 워크 플로우를 자동화 할 수 있기 때문에
    머신러닝 모델 개발시 많은 시간을 소요했던 코딩, 전처리, 모델 선택, 파라미터 튜닝 작업을 자동화해주어 쉽고, 높은 생산성의 작업을 가능하게 합니다.
