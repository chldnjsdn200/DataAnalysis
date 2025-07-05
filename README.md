📈 빅 데이터를 활용한 실시간 주식 동향 분석 시스템

> **Capstone Design 프로젝트 + 대한임베디드학회 논문 요약 정리**

이 프로젝트는 Python과 다양한 데이터 분석 및 시각화 라이브러리를 활용하여 **주식 시장의 과거 및 실시간 데이터**를 수집하고 가공하여 시각적으로 표현함으로써, **개인 투자자들에게 효율적인 투자 정보를 제공**하는 것을 목표로 합니다.

<br/>

## 🔧 개발 환경

- **OS**: Windows 10
- **언어 및 라이브러리**:
  - Python 3.x
  - Pandas / Numpy / Matplotlib / Plotly / Dash / Tensorflow
- **DB**: MariaDB
- **Web**: Flask, Dash (Heroku 배포)
- **API**: 키움증권, 크레온 등 Open API + Web Crawling (BeautifulSoup 사용)

<br/>

## 🧠 주요 기능

- ✅ **상장 기업 코드 및 주가 데이터 자동 수집**
  - KRX에서 상장 코드 추출
  - Web Crawling 및 증권 API를 통해 실시간 주가 수집
- ✅ **데이터베이스 저장 및 관리**
  - 기업별 일간 주가 DB 저장 및 조회
- ✅ **시각화 및 분석**
  - 캔들 차트, 볼린저 밴드, MFI, 추세 추종 기법 기반 분석
  - Plotly 기반 인터랙티브 차트
- ✅ **LSTM 기반 주가 예측**
  - Tensorflow를 활용한 시계열 예측 모델 구현
- ✅ **웹 페이지 구현**
  - Dash를 통해 데이터 시각화 결과 제공
  - 드롭다운 기반 기업 선택 및 예측 결과 출력

<br/>

## 🖥️ 시스템 구성도
[ Client ] ←→ [ Web Server (Dash/Flask) ] ←→ [ Server ] ←→ [ DB ]
↑
[ Web Crawling / Open API ]


<br/>

## 📊 화면 예시

- 좌측: 종목 코드 및 전일 종가/거래량 표기, 금일 예측 종가
- 중앙: 종가 및 거래량 캔들차트
- 우측: 볼린저 밴드, MFI 등 보조 지표 시각화

![주가 분석 예시 이미지](#) <!-- https://user-images.githubusercontent.com/90487843/153156062-894cfee3-65c3-48f3-b9ab-70071770cf83.png -->

<br/>

## 🔍 사용된 주가 분석 기법

- **볼린저 밴드 (%b)**: 주가 위치 지표
- **MFI (Money Flow Index)**: 자금 유입/유출 흐름 파악
- **추세 추종 기법**:  
  - 매수 조건: `%b > 0.8 && MFI > 80`  
  - 매도 조건: `%b < 0.2 && MFI < 20`
- **LSTM (Long Short-Term Memory)**:  
  - 시계열 데이터 기반 주가 예측에 활용
  - Tensorflow 기반 모델 구성

<br/>

## 🏁 향후 발전 방향

- 다양한 주식 분석 기법 추가 (MACD, RSI 등)
- 예측 모델 고도화 및 다양한 하이퍼파라미터 실험
- 사용자 맞춤형 포트폴리오 추천 기능 추가

<br/>

## 📚 참고문헌

- 김황후, 「파이썬 증권 데이터 분석」, 한빛미디어, 2020  
- 존 볼린저, 「볼린저 밴드 투자기법」, 이레미디어, 2010  
- 김환희, 「텐서플로 2.0 프로그래밍」, 위키북스, 2020  
- [https://plotly.com/](https://plotly.com/)  
- [https://dash.plotly.com/](https://dash.plotly.com/)

---

## 👨‍💻 Contributors

- 최원우 **[GitHub](https://github.com/chldnjsdn200)**
- 김남규 **[GitHub](https://github.com/Isanghada/Stock_Analysis)**
- 한창재 (부경대학교 컴퓨터공학과)

