

# IoT 플랫폼

- 김재훈 교수

## IoT 플랫폼 OT

### IoT 

- 사물의 상태를 파악하고 모니터링하고, 효율적으로 움직이도록 제어하는 것
- IoT가 새로운 Business Model들을 만들고 있음

### More on 4 Layers Model (IoT 4 Layer)

- **Integrated Application**
  - 응용, 비즈니스 플랫폼
- **Information Processing**
  - IoT 블록체인
  - 클라우드, 빅데이터
  - 상황인지
- **Network Construction**
  - 미들웨어 플랫폼
  - 자원관리, 데이터처리
- **Sensing and Identification (low level device)**
  - 자원관리, 데이터처리
  - 디바이스, 센서



## 1-1) IoT 플랫폼 소개

IoT산업은 연 평균 10~20%의 성장을 거듭하고 있었다. (2020년 기준)

### IoT를 가능하게 하는 기술들

- Device Technologies : 기기 제조 기술
- Connectivity Technologies : 연결 기술
- Service Technologies

### 사물인터넷의 범위 및 요소 기술

- 데이터 수집 > 데이터 전송 > 통신 > 데이터 분석 > 활용

### IoT 이외 유사개념과의 비교 (CPS, M2M ... )

- IoT : 사물 인터넷, 개방형 시스템, 서비스 지향형
- CPS : 사이버물리시스템, 폐쇄형 시스템, 자원 중심적
- M2M : Machine to Machine
- Internet of Everything : 모든것이 인터넷으로 연결이 된다.
- Fog Computing : 안개 처럼 우리 주변에 게이트웨이나 지역을 담당하는 분산된 클라우드가 존재



### IoT 전망

- 사물인터넷의 시장규모는 2022년까지 연 평균 10% 이상 꾸준히 성장하고 있습니다.



### IoT 플랫폼 동향

- 디바이스/데이터/서비스/... 중심 플랫폼,



### Simplified IoT Architecture

- Application
- Decision Support Tools
- Big Data Stores
- Network and Telecommunications Equipment
  - LTE, WiFi, Bluetooth...

### IoT 플랫폼 구조의 구성 요소

- 응용, 정보처리, 네트워크, 센서/디바이스



## 1-2) IoT 플랫폼 구조

### 학습 목표

- IoT 프랫폼 구조와 구성 요소를 이해한다. 
- IoT 플랫폼 구성요소의 주요 이슈를 알아본다.



### 사물인터넷 등장배경

- 소형화
- 저전력화
- 저가격화 : 센서 사용을 위한 비용이 급격히 줄어듦
- 표준화
  - 스마트홈, 헬스케어, 건설, 제조, 농업(온도제어), 에너지, 환경, 국방 등 다양한 도메인 분야에서 사용이 되고 있음



### 센서와 엑츄에이터(actuator)

- 센서 : 물리량을 측정하는 기기
  - 카메라, 가속도계, 레이더, 스위치 ...
- 엑츄에이터 : 물리량을 변화시키는 기기
  - Motor controllers, LEDs, lasers, Loudspeakers

#### Mobius Platform

사물 간에 인터넷을 할 수 있는 물적 기반인 통신 네트워크가 원활하게 작동하도록 하는 운영체제



### Distributed Computing in IoT (IoT 분산 네트워크 플랫폼)

- 서버쪽에서 모든 일을 처리하는 것이 아니라, 지역적인 서비스를 분산된 게이트웨이가 맡게되면 더욱 효율적으로, 빠르게 처리할 수 있음



### IoT 미들웨어 플랫폼

- 미들웨어란, 말 그대로 중간에 있다는 것, 사물(Thing, 하드웨어)들이 있고, OS가 올라가고, 그 다음 올라갈 수 있는 것이 middleware 이다.
- 블록체인도 하나의 미들웨어
  - 폐쇄적이고 집중화된 IoT Network ---클라우드---> 개발형의 집중화된 클라우드 IoT Network ---블록체인---> 개방형의 분산화된 클라우드 IoT Network





## 2-1) 사물인터넷 표준화

- IoT와 관련된 다양한 표준화 기구가 있습니다. (ITU, ISO, IEEE, oneM2M ...)
- oneM2M
  - 플랫폼 환경을 통합, 공유하고, 사물인터넷 공동서비스 플랫폼 개발을 위해 발족 된 사실상 표준화 단체
  - 표준화 관련 Release를 지속 업데이트 하고 있음 (1, 2, 3, ...)
- OCF(Open Connectivity Foundation)
  - 사물인터넷 구현 시 REST 구조 기반, 경량형 CoAP 프로토콜을 사용하여 **사물인터넷 장치들을 연결하고, 장치에 존재하는 자원들을 상호제어**할 수 있게 하는 표준 플랫폼 기술
- IETF(Internet Engineering Task Force, 국제 인터넷 표준화 기구)

#### MEMS

- 미세 전자 기계 시스템(Micro-Electro-Mechanical systems)의 약자

#### 시멘틱 웹

- 컴퓨터가 정보자원의 뜻을 이해하고, 논리적 추론까지 할 수 있는 차세대 지능형 웹

