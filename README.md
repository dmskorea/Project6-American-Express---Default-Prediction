# Project6-American-Express---Default-Prediction



<hr />
공지사항(22.7.3)
<hr />
1. 미팅 간격은 2주간격
2. 진행사항 프레젠테이션 (텍스트파일도 OK) 
3. 미팅 종료 후 Done(2주간진행내용) / Todo(2주간 진행할 내용) 구글 시트에 작성 요망
   https://docs.google.com/spreadsheets/d/13seldUdlQIFgzjZb-ukfmC3vQBsHUNY0RD3QekgCgpI/edit?usp=sharing
4. 다음 미팅: 7월 17일
   - 데이터 탐색 결과 혹은 캐글러의 아이디어 등을 활용해 베이스라인 모델 만들기
5. 향후 일정 : 
   - 베이스라인 모델 설정 및 공유 : 3차 미팅(7.17)
   - single 모델 최적화1(모델 튜닝, 파생변수 생성, 변수선택 등 적용) : 4차 미팅(7.31)
   - single 모델 최적화2 & 협업(앙상블) 모델 적용1 : 5차 미팅(8.14)
   - 협업(앙상블) 모델 적용1 & 최종 2개 모델 선정(8.25일 오전 9시 대회 마감 전 확정, 별도 미팅 X)


<hr />
모델 스코어 (Single Model)
<hr />

| date| name | 알고리즘 | 변수개수 | CV | LB | 전략 |
|-----|------|---------|---------|----|-----|-----|
| 2022-06-19 | kyy |  |  |  |  |  |
| 2022-06-26 | jrh | XGB |  | 0.7902 |  |  |


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

[1차 미팅 요약 ('22.6.19)]

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

