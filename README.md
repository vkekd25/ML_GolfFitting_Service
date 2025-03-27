# AI_GolfFitting_Service

## 프로젝트
<br>

- **프로젝트 주제**
  - 스크린 골프 데이터를 기반으로 ML을 활용하여 소비자들에게 맞춤형 분석을 제공하고, 스코어링 및 클럽 매칭을 추천하는 골프 피팅 서비스

- **프로젝트 개요**
  -	사용자 스윙 유형별/골프 클럽별 휴먼/로봇 테스트 분석
  -	ML 결과기반 골프 피팅 스코어링 서비스 개발
  -	AI 골프 클럽매칭 추천 시스템 개발
  -	AWS EC2기반 ML-Ops 시스템 구축 : 학습용 데이터 파이프라인 구축


- **프로젝트 결과**

  [서비스 결과]

<img width="621" height = "280" alt="스크린샷 2025-03-07 오전 7 16 23" src="https://github.com/user-attachments/assets/0eb41017-1aa5-403f-87cb-b743e20af248" />
<img width="621" height = "280" alt="스크린샷 2025-03-07 오전 7 17 13" src="https://github.com/user-attachments/assets/a53f5ae0-bc3e-400f-b7bc-f93b67a61de5" />
<img width="621" height = "280" alt="스크린샷 2025-03-07 오전 7 28 48" src="https://github.com/user-attachments/assets/c0098d09-674d-4a35-900e-b5a4539b1732" />

  [데이터 분석 결과]

   **유저샷분석**
  
  **연구 배경 및 목적**
  
      (주) QED 콘솔에 내재화할 Q-Fit 사용자 입력 데이터의 평균값 신뢰성을 파악하기 위해 유저 샷 분석을 진행하였습니다. 본 분석에서는 2022년 6월과 8월의 샷 데이터를 통합하여
      약 200만 개의 데이터 행을 활용하였으며, 데이터를 정제하여 드라이버 샷을 중심으로 분석 하였습니다.  
      가설 설정:  
          1. 가설 1: 데이터 전처리를 통해 이상치를 제거하면 정규성을 가지는 유저 비율이 증가할 것이다.  
          2. 가설 2: 샷 데이터 수가 많을수록 정규성을 가지는 유저의 비율이 감소할 것이다.  
          3. 가설 3: 특정 기준(비거리, Back Spin 등)으로 데이터를 전처리하면 일부 특성에서 정규성이 향상될 것이다.  
      
      **결론 및 향후 연구 방향**
      
      본 연구를 통해 이상치를 제거할수록 Q-Fit 데이터의 신뢰성이 향상될 가능성이 있음을 확인하였습니다. 그러나 데이터 손실이 발생할 위험도 있으므로, 적절한 전처리 기준을 설정해야합니다.  
      향후 연구 방향:  
          1. 샷 개수에 따른 평균, 표준편차, 최대값, 최소값을 분석하여 드라이버, 웨지, 아이언 샷을 구분하는 추가 연구 진행.  
          2. 정규성 외에도 데이터 품질 지표(예: 변동성, 일관성 등)를 고려한 심층 분석.  
          3. 이상치 제거에 따른 데이터 손실을 최소화하는 최적의 전처리 방법 도출.  
      
      추가 및 상세자료는 데이터 분석 파일 참고

  **스크린골프 장비 상관관계**
  
  **연구 배경 및 목적**
  
  본 연구는 QED 데이터와 GCquad 데이터 간의 상관관계를 분석하여 두 시스템 간 데이터의 일관성을 검토하고, 클럽별/샤프트별/클럽패스별 특성의 차이를 파악하는 것을 목적으로
  합니다. GCquad 스티커를 헤드 단면에 부착한 상태에서 실제 휴먼이 스윙을 수행하였으며, 클럽패스별(-2, 0, 2)로 다양한 헤드/샤프트 조합을 각 3샷씩 진행하였습니다. 본 연구에서는 QED
  데이터와 GCquad 데이터의 특성별 증감률과 평균값을 비교 분석하여, 두 시스템 간 데이터 차이를 정량적으로 평가하고 신뢰도를 검토하고자 합니다.
  
  **결론 및 향후 연구 방향 (Conclusion & Future Research)**
  
  본 연구를 통해 QED 데이터와 GCquad 데이터 간의 차이가 특성별로 다르게 나타나는 것을 확인하였습니다.
  결론:
      1. Backspin, Ball Speed, Face Angle, Club Path의 경우 QED와 GCquad 데이터 간 수치가 유사하므로 신뢰할 수 있음.
      2. Launch Angle, Peak Height, Descent Angle, Attack Angle은 일정한 비율로 차이를 보이므로 보정 가능성이 있음.
      3. Sidespin과 Side Angle의 경우 불규칙한 차이를 보이므로 두 데이터 간 신뢰도를 검토할 필요가 있음.
  
  향후 연구 방향:  
      1. Sidespin 및 Side Angle 데이터의 신뢰도를 검토하고 보정 가능성을 평가    
      2. 특정 특성별 차이 보정 모델을 개발하여 QED 및 GCquad 데이터를 일관성 있게 사용할 수 있도록 조정   
      3. 다양한 클럽 및 샤프트 조합에서 추가 실험을 수행하여 데이터의 일관성을 더욱 검증  
  
  추가 및 상세자료는 데이터 분석 파일 참고

  **골프스윙유형 분석**
  
  <img width="621" height = "280" alt="스크린샷 2025-03-08 오후 5 12 47" src="https://github.com/user-attachments/assets/11b6934e-46e9-4c7e-877c-a1a7a3f9511d" />
  
  추가 및 상세자료는 데이터 분석 파일 참고


  [ML 결과]

<img width="621" height = "280" alt="스크린샷 2025-03-08 오후 4 43 32" src="https://github.com/user-attachments/assets/98cc90ac-0876-429a-adb4-2b4d1c17a697" />

추가 및 상세자료는 데이터 분석 파일 참고

- **References**
  - [Scraps From the Loft, “Stand-Up Comedy Transcripts.” https:// scrapsfromtheloft.com/stand-up-comedy-scripts/.](https://xgboost.readthedocs.io/en/stable/)
  - [Dead Frog. https://www.dead-frog.com/.](https://trackmanuniversity.com/Home)
  - https://airflow.apache.org/docs/
  - https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/concepts.html



<br><br>


