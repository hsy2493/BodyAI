# `BodyAI` - <적정몸무게 예측 AI 사이트(머신러닝 개인 프로젝트(1차)>👣 <br>
1. 작업 기간 : 2025. 03. 18 ~ 2025. 03. 19
2. 주제 : 적정몸무게 예측 AI 사이트 
3. 목적 : 건강에 관심 있는 고객이 온라인에서 BodyAI 사이트를 통하여 키와 성별 기반의 적정 몸무게 예측 결과를 제공받고, 이를 통해 고객 스스로 건강 관리를 효과적으로 수행함으로서 장기적인 건강 관리 비용을 절감하는 것을 주목적으로 진행된 적정몸무게 예측 AI 사이트 프로젝트 입니다.
4. 주요 기능 : 키와 성별 기반으로 적정 몸무게 예측 
* 몸무게 예측 AI 보고서 자료 <br>
https://github.com/hsy2493/BodyAI/issues/1#issue-3042546787 <br>
5. 작업 툴
- 사용 언어 : python
- 머신러닝 모델 정의 : 선형 회귀 모델
- UI : streamlit
- 데이터 프로파일링 (EDA) : ydata_profiling <br>

  
6. 결과물 : <br>

## <화면 구현(streamlit 기반)><br>
(1) 키와 성별 기반 적정몸무게 예측 <br> 
  <img width="674" alt="image" src="https://github.com/user-attachments/assets/9e1c5c4e-23ae-4ba6-b508-0ab6b2c6055b" />
 <br> 
<설명> <br>
- 키(cm) 입력과 성별 선택 후, 몸무게 예측하기 버튼 클릭 시, 적정 몸무게가 예측된다. <br>
- 몸무게 예측 - 화면구현 (streamlit 기반) 상세 코드 <br>
https://github.com/hsy2493/BodyAI/blob/main/streamlit/heightvsweight.py <br> 

## <기능 구현> <br>
(1) 데이터 수집 <br>
<img width="443" alt="image" src="https://github.com/user-attachments/assets/42a2b79e-f148-4168-ae39-f475aad158f8" />
 <br>
<설명> <br>
-몸무게 예측에 사용되는 dataset으로, 순서대로 성별, 키, 몸무게의 약 1000개의 데이터셋을 사용했다. <br> 
- 데이터 수집 자료 (weight-height.csv) <br>
https://github.com/hsy2493/BodyAI/blob/main/streamlit/dataset/weight-height.csv <br>
- dataset 출처 (kaggle 사이트) <br>
https://www.kaggle.com/datasets/mustafaali96/weight-height <br> 

(2) 데이터 분석 (EDA 기반)<br>
- 데이터 분석 과정 상세 코드 <br>
https://github.com/hsy2493/BodyAI/blob/main/streamlit/heightvsweight.ipynb <br> 
- 데이터 분석 자료 (EDA) <br>
https://github.com/hsy2493/BodyAI/blob/main/streamlit/report/heightvsweight.html <br>
<img width="578" alt="image" src="https://github.com/user-attachments/assets/20b7e4a5-13d8-43e4-9e59-759bd6d52017" />
 <br>
<설명> <br>
-Gender(성별), Height(키), Weight(몸무게) 간의 상관관계 히트맵 <br>
-키와 몸무게 : 매우 강한 양의 상관 관계 (0.92)를 나타낸다. <br>
-성별 : 키와 몸무게 모두와 음의 상관 관계로, 이는 성별 인코딩 방식에 따라 남성이 여성보다 키가 크고 무겁다. <br>

<br>
<img width="762" alt="image" src="https://github.com/user-attachments/assets/4421f96b-c7da-42b5-af49-9424a488798a" />
 <br>
<img width="679" alt="image" src="https://github.com/user-attachments/assets/da9f67d6-7f4d-4517-981a-1cfb7eb342f6" />
 <br>
<설명> <br>
-변수 : 3개(성별, 키, 몸무게)<br>
-결측치 : 데이터 전처리로 결측치(0개)는 없다.<br>

<br>
<img width="765" alt="image" src="https://github.com/user-attachments/assets/7294c4eb-8f8c-46d4-b598-7b6f3870ed34" />
 <br>
<img width="767" alt="image" src="https://github.com/user-attachments/assets/c92d2140-5e4c-4b3f-9ba0-962bb7b373a0" />
 <br>
<설명> <br>
-주요 데이터로, 성별, 키, 몸무게 3개가 사용된다.<br>

<br>
(3) 데이터 학습 및 모델정의 <br>
- AI 모델 정의 및 학습 과정 (선형 회귀 모델) <br>
https://github.com/hsy2493/BodyAI/blob/main/streamlit/heightvsweight.ipynb <br> 
<img width="777" alt="image" src="https://github.com/user-attachments/assets/67c16501-40e0-45b2-92bc-39c1c9843836" />
 <br>
<img width="778" alt="image" src="https://github.com/user-attachments/assets/23e32972-241b-4f89-b61c-c1c82d406219" />
 <br>
 
<설명> <br>
-모델 정의 : 선형 회귀 모델와 랜덤 포레스트 모델 정의 (모델 비교) <br>
-모델 학습 : 훈련용 데이터로 모델 훈련 진행 <br>
-모델 예측 비교 (실제값 vs 예측값) : 선형 회귀 모델이 랜덤 포레스트 모델보다 더 적합함.<br>


<b><br>
6. 성과 <br>
- kaggle 사이트에서 데이터셋 수집이 가능함. 데이터셋 선택 시, Comments에서 사용 후기를 고려하여 선정하는 학습 성공률을 높인다 것을 이번 프로젝트의 모델 학습 결과를 통하여 깨달음 (데이터셋 정확도의 중요성). <br>
- streamlit 라이브러리를 활용하여, 머신러닝 프로젝트의 프로토타이핑(화면 UI)으로 사용하는 것을 학습함. <br> 
- 수집한 데이터셋으로 머신러닝 모델 정의 및 데이터 학습이 가능함. 또한 이를 streamlit를 활용하여, UI 시각화가 가능함. <br>
- ydata_profiling 라는 데이터 프로파일링 라이브러리를 활용하여, 탐색적 데이터 분석(Exploratory Data Analysis, EDA) html 파일 생성 후, 데이터 분석 자료로 사용하는 방법을 학습함. <br>
- ipynb(주피터 노트) 파일을 py(파이썬) 파일로 변경이 가능함 (streamlit 활용을 위한 변경).<br>
- 파이썬 가상환경(.venv) 생성 및 pip 사용법(Module 다운, 삭제, 업데이트, pip list 확인)을 학습함. <br>
- requirements.txt 활용하여, pip 리스트 관리법(사용 중인 pip 목록 저장 및 다른 프로젝트에서도 사용)을 학습함. <br> </b>
