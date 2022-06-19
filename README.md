# Project6-American-Express---Default-Prediction



<hr />
공지사항
<hr />

1. 미팅 간격은 유동적으로 수행
2. 다음 미팅부터는 진행사항 프레젠테이션 (텍스트파일도 OK) 
3. 회의록은 돌아가면서 작성
4. 다음 미팅: 7월 3일
   - 베이스라인 모델 찾아 발표
   - 하나의 contribution 찾아보고 적용해보기



<hr />
모델 스코어 (Single Model)
<hr />

| date| name | 알고리즘 | 변수개수 | CV | LB | 전략 |
|-----|------|---------|---------|----|-----|-----|
| 2022-06-19 | kyy | LGB |  |  |  |  |


<hr />
Submit CountBoard (팀 병합후 활용)
<hr />

| 8-18 | 8-19 | 8-20 | 8-21 | 8-22 | 8-23 | 8-24 |
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
|   o  |   o  |   o  |   o  |  o   |   o  |   o  |
|   o  |   o  |   o  |   o  |  o   |   o  |   o  |
|   o  |   o  |   o  |   o  |  o   |   o  |   o  |
|   o  |   o  |   o  |   o  |  o   |   o  |   o  |
|   o  |   o  |   o  |   o  |  o   |   o  |   o  | 


[대회 주요 일정 (UTC 기준)]
- 대회 시작일시 : 2022년 5월 25일 
- 최종 submit : 2022년 8월 24일 11:59 PM
- 팀merge 데드라인 : 2022년 8월 17일 11:59 PM
- (개인) 일 최대 submit 횟수 : 5번 
- (팀) 최대 submit 횟수 : 대회 시작일 이후 경과일수 X 일 최대 submit 횟수(5)
  단, 최종 private LB가 동률일 경우, submit 횟수가 더 적을 경우 선순위 랭크 (submit 남용은 자제)
  
 
<hr />
주요 진행 내용 (미팅 후 작성)
<hr />

[1차 미팅 요약]

데이터
- 데이터를 batch 단위가 아닌 그룹을 이루는 시계열 데이터로 다뤄 처리
- XGBoost계열의 모델 대신 Transformer 등을 사용해 매핑 

AutoML
- AutoML Framework: AutoGluon, pycaret, etc.
- 데이터가 어떤 모델과 맞을지 인사이트를 얻을 수 있을 것.

노트북: Why is there so much test data?
- https://www.kaggle.com/competitions/amex-default-prediction/discussion/329088
- Val를 2개로 쪼갰는데, iteration마다 성능차가 발생 (일관성이 없음)
- 평가방법이 noisy하기에 test dataset을 train dataset보다 더 크게 주어 일반화되게 함.

