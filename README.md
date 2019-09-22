# AjouLectureMemo

<br>
<br>
<br>

# 블록체인과 보안

<br>

## 블록체인(BlockChain)  이란?
- 블록을 통해 데이터들이 사용 됨
- 무결성, 신뢰성, 보안성이 보장되는 데이터
- 블록은 각각이 거래(Transaction)을 발생시키는 노드이다. 
- 노드 간 사슬(Chain)처럼 연결이 되어있음
- 블록체인은 공공거래장부, 분산장부 
- P2P 네트워크를 통해 전파 및 거래가 가능

- 헤더의 해쉬값을 바꾸면 다른 노드의 해쉬값도 변경됨 
- 블록체인의 위조 및 변조가 어려운 이유
- bitcoind는 새로은 트랜젝션이 존재하는지 계속 확인한다.
- bitcoind : 일종의 데몬 프로그램

- *제네시스 블록 : 처음 생성되는 블록을 의미한다.

<br>
<br>

## 이더리움
- ETH(ether)
- 1 Ehter = 1,000,000,000,000,000,000 wei

### 이더리움 기능
- 스마트 컨트랙트 (Smart Contract)
- 거래를 위한 다양한 기능 추가 가능 
- 자동화된 계약 (Automated Contract)     

### 이더리움 구조
- 상태 전이 (state transition) 머클 트리를 사용
- 상태전이 일반 머클 확장 패트리샤 트리 
- 솔리디티 언어로 작동
- 개발경험이 있다면 배우기 어렵지 않음(
- 단, 개발경험이 없으면 좀 어려울 수도 있음

<br>
<br>

## 하이퍼 레저 패브릭 네트워크
- Hyperledger Fabric Network
- 다양한 언어를 통한 체인코드 제공
- Go, Java, Node.js 등..
- 다양한 합의 알고리즘 중 선택 가능
- PBFT, Kafka, RAFT...

<br>

### 분산원장
- Distributed ledger
- 데이터를 저장하는 데이터베이스를 블록체인에 참여하는 사람들이 동일한 원장을 소유 및 관리하는 기술
- 중앙화된 서버가 소유하지 않음 

- 분산 애플리케이션 (Dapp, Decentralized Application)
- 프로그래밍을 통해 다양한 응용프로그램을 만들 수 있음.
- 합의 (Consensus)
- 트랜젝션을 정해진 순서에 맞춰 정렬
- -> 정렬된 트랜젝션의 유효성 검증 후 최신 블록 업데이트

<br>

### 비트코인 vs 이더리움  vs  하이퍼레저 패브릭
- 네트워크 :         Public       / Public or Private / 허가형 Private
- 암호화폐 :         BTC          / ETH                    / 자체화폐x, 체인코드 통해 개발
- 스마트컨트랙트 :   x            / Solidity 개발       / 
Go, Java ,Node.js 등 개발
- 합의알고리즘 :   PoW         / PoW,PoA           / PBFT, Kafka, RAFT
- 블록 생성속도 : 10~20 min / 10~20 sec         / Faster than others

### 퍼블릭 vs 프라이빗 
- BTC, ETH / IBM Fabric, LoopChain, R3 Corda

### 하이퍼레저 패브릭 구성요소
- Peer 
- Peer Node라고도 부른다. 
- 하이퍼레저 패브릭 블록체인을 구성하는 네트워크 노드 (Network Node)
- 모든 Peer는 자기만의 분산원장과 체인코드를 관리

- ChainCode, 체인코드
- 분산원장에 데이터를 기록하거나 읽기 위한 스마트 컨트랙트
- 분산 애플리케이션 (DApp)과 함께 개발되어 사용한다. 
- 시스템 레벨에서의 다섯개의 체인코드를 제공
- 하이퍼레저 패브릭 시스템 레벨에서 수행되는 체인코드 (기본적으로 제공)
- GSCC (Query System Chaincode) : 블록, 트랜젝션 정보 조회
- ESCC (Endorser System Chaincode) : 트랜젝션 보증정책 담당
- VSCC (Validator System Chaincode) : 블록 검증
- CSCC (Configuration System Chaincode) : 채널 설정
- LSCC (Life Cycle System Chaincode)  : 체인코드의 생명주기를 위한 체인코드 
- DApp, 디앱
- Endorsement Policy, 보증정책
- 트랜젝션을 생성하는 클라이언트(분산 애플리케이션(Distributed Application)와 peer 사이에 작용
- Organization, 조직
- Channel
- Ledger
- Gossip
- Identity
- MSP (Membership Service Provider)
- Orderer 
- 들어온 트랜젝션의 보증정책 등 검증 후, 채널안에 구성되어있는 peer들에게 Broadcasting

<br>

<br>
<br>
<br>

# IoT 응용 및 서비스 사례 연구

<br>
<br>

## IoT 플랫폼 
- 1-1
- 센서 (Sensor) + 통신 (Communication) + 사람 (Human) 의 연결
- Producer -> Platform(Mart) -> Consumer 
- Platform의 예 -> App Store, SNS 

<br>

### ✓ Key Point : 플랫폼(Platform)의 의미, 각 시대별 주 플랫폼이 존재, 이 플랫폼을 어떻게 장악하느냐가 향후에 중요한 역할을 하기에 플랫폼에 대한 관심이 필요하다.

<br>

### Apple vs Andriod
- 폐쇄형 플랫폼, Apple 
- 공개형 플랫폼, Andriod


<br>

### 인터넷 세대 추세 
- I1)윈도우 운영체제 플랫폼 
- I2) -> 모바일+앱 융합 플랫폼 
- I3) -> SNS 서비스 플랫폼 
- I4) -> 사물인터넷(IoT) 플랫폼 -> 오늘날 플랫폼 장악을 위한 시장경쟁 중
-  * I : 인터넷

<br>

### 현 마켓 추세 
- F(acebook)A(mazon)N(etflex)G(oogle) 
-> M(icrosoft)A(pple)G(oogle)A(mazon)
- 세계 시가총액 1위 -> 마이크로소프트(2018년에 애플 제치고 1위 등극)
- 아마존은 현재 뭘로 돈을 버나? -> 클라우드 서비스(AWS)
* Amazon : AI 엔지니어가 가장 많은 곳… AI 스피커를 최초로 만든 곳

<br>

### Clouding Platform을 누가 장악했나?? 
- MS : 장터(platform)를 만들고 자기들도 파는 상황, 윈도우뿐만 아니라… 
- 플랫폼을 어떻게 장악하고 플레이 하느냐가 중요
iOS Android 는 운영체제 

<br>

### 가상화폐 != 블록체인
-> 가상화폐가 블록체인 기술을 응용한 것 뿐이다. 

<br>
<br>


## IoT 응용
- 1-2
- Healthcare, Home, Car...

<br>

### Smart Healthcare
- 질병치료 중심, 예방과 관리 -> 건강한 삶의 유지 및 패러다임 전환
- Healthcare 플랫폼
  - Apple
    - Apple은 헬스케어 플랫폼, HealthKit, Application "Health"를 탑재
  - Google
    - Google Fit :은 개인 건강종보를 받고 공유가능한 저장소 역할, Apple의 "HeathKit"보다 좀더 개방 된 플랫 폼

- ✓ 응용 예시
  - GlowCap
    - 스마트 약병으로 복약시간이 되면 뚜껑의 램프가 점등 + 소리를 냄
    - 제 시간에 뚜껑이 안열리점 SMS 등으로 정보 전송
    - 약일 떨어지면 해당 사실 통보
  
  - HAPIfork
    - 스마트 포크  
    - 과학적인 건강관리로 삶의 질 향상 유도 
    - 음식 투입속도, 포크 이용 횟수 등 데이터 측정, 데이터 기반 식습관 제안
    
  - Bee+
    - 스마트 인슐린 펜
    - 당뇨병 환자의 투약정보를 스마트폰에 전송 및 투약주기 관리
    
  - UrinCare
    - 스마트폰 기반 대소변 관리 시스템
    - 스스로 대소변을 처리하기 힘든 고령층, 환자들이 사용
    - 대소변 배출 시, 보호자나 요양사에게 해당 사실 전송
  
  - Corventis
    - 심장박동 모니터링 기계
    - 심장 이상여부를 판단 하고 이상 발생 시 환자에게 조언
    - 심장 질환으로 인한 사망 확률 최소화
    
  - MPM
    - 1회용 밴드처럼 심장 부위 부착 
    - 심장의 부정맥, 심부전 등 체크 및 경고 
    
  - OMsignal
    - 스마트 의류
    - 옷에 내장된 센서를 통해 심박수, 호흡상태, 칼로리 소모량, 운동량 등 모니터링
      - 이상 시 스마트폰으로 해당 내용을 알림
      
  - Connected Bicycle
    - 삼성 커넥티드 자전거
    - 자전거 주행속도, 운행거리, 운동량 등 파악 

<br>

### Smart Home
- 주거환경에 IT를 융합, 복지증진 및 안전한 생활이 가능 
- 스마트 라이프 환경 구축

- ✓ 응용 예시
  - Google IoT 플랫폼
    - Android 기반 IoT 플랫폼
    - 가정용 CCTV기업, "드롭캠" 인수
    
  - Google Nest Labs
    - 실내의 온도 조절
    - 실내 온도와 보일러의 가동 내역 등 기록
    - 기록 된 데이터들을 클라우드에 누적되어 분석에 활용
    - 인터넷과 연결되어 실내를 쉽게 관리 
    
  - Apple HomeKit
    - iOS를 활용해서 스마트폰으로 연결된 가전제품을  제어 
    
  - Samsung SmartThings
    - IoT 개방형 플랫폼
    - 습도센서, 개폐센서, 모션센서, 카메라, 스피커 등이 스마트폰과 연결
    - 스마트폰을 통한 원격 모니터링, 제어 가능
    
  - LG전자 SmartThinQ Hub
    - 스마트홈(Smart Hime) 서비스를 지원
    - 가전제품 상태, 개인일정, 날씨등을 화면과 음성으로 제공
    
  - 그 외
    - 스마트폰을 통한 조명 제어
    - 초인종을 눌렀을때 카메라가 스마트폰으로 공유
    - 아기의 내의에 부착되어 모니터링되는 카메라가 스마트폰과 공유 
  
<br>

### Smart Car
- 첨단 컴퓨터 / 통신 / 측정기술, 지능제어 기술 등을 이용, 자동 운행 차량 개발
- ✓ 응용 예시
  - 커넥티드 카(Connected Car), 무인 자동차, 자율주행 차량

<br>
  
### Smart Grid
- 전력망에 IT기술을 접목 
  - 실시간 전력망 정보 확인 및 에너지 효율 최적화
- ✓ 응용 예시
  - 송도 AMI
    - 송도 인천 경제자유구역, 송도국제도시가 스마트그리드 도시
    - 에너지 컨설팅 사업 진행
  
<br>

### Smart Factory
- 4차 산업혁명의 목표
- CPS(CyberPhysical System), IoT, BigData 등 핵심기술사용 
- Smart Factory 핵심기술
  - IoT (Internet of Things)
  - CPS (CyberPhysical System)
  - BigData
  - Cloud
  - 3D Printing
  - etc. 에너지 철강, Smart Sensor, Hologram, AR...

- ∙ 산업혁명의 변천사 
  - 1차 산업혁명
    - 수력, 증기기관 / 기계식 생산설비
  - 2차 산업혁명
    - 컨베이어벨트, 전기동력을 사용한 대량생산
  - 3차 산업혁명
    - 전자기술과 IT를 활용한 부분 자동화 
  - 4차 산업혁명
    - ICT와 제조업의 융합 
    - 사물인터넷 (IoT) 확산

<br>

### Smart Farm
- ICT를 결합한 지능화 농장
- CCTV, 각종 센서를 통한 모니터링, 환경 분석

<br>

### Smart City
- 스마트시티 의 최종 가치
  - 기본욕구 충족
  - 인간성 회복
  - 도시공간의 본질 회복
  
  
<br>

