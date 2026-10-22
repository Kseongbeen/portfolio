# 대기·기상 데이터 기반 미세먼지(PM10) 농도 예측

> 코드·보고서: [Kseongbeen/finedust-prediction-ml](https://github.com/Kseongbeen/finedust-prediction-ml)

## 1. 프로젝트 개요
대기질·기상 데이터(2021–2022)로 여러 회귀 모델을 비교해 PM10 농도를 예측한 수업 프로젝트입니다. (AI+X 중급, 2조)

## 2. 문제 정의 / 동기
- 미세먼지 농도는 기상 조건과 국외 유입의 영향을 함께 받아, 단순 통계 모델로는 고농도 구간을 맞히기 어렵습니다.
- 어떤 변수와 모델 조합이 예측에 도움이 되는지 단계별로 확인하고자 했습니다.

## 3. 접근 방식
- 결측치 처리와 VIF 기반 다중공선성 검정으로 변수 정리
- 선형회귀·SVR·Random Forest·XGBoost·Gradient Boosting 비교 후 그리드 서치 튜닝
- PCA 적용, 전일 베이징 풍향·풍속으로 만든 해외 유입 특징 추가 실험

## 4. 본인 역할
- 팀 프로젝트
- 데이터 EDA, 머신러닝 모델링(모델 비교·튜닝·특징 실험)
- 딥러닝(ANN)·시계열 모델링은 다른 팀원 담당

## 5. 결과
- SVR 베이스라인 R² 0.642 → 튜닝 0.681 → PCA 0.686 → 해외 유입 특징 추가 0.689
- '매우 나쁨' 구간과 고농도 이상치 예측은 한계로 남음

## 6. 사용 기술
Python · pandas · scikit-learn · XGBoost · matplotlib · seaborn
