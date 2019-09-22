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

### ✓ Key Point : 플랫폼(Platform)의 의미, 각 시대별 주 플랫폼이 존재, 이 플랫폼을 어떻게 장악하느냐가 향후에 중요한 역할을 하기에 플랫폼에 대한 관심이 필요하다.

<br>

### Apple vs Andriod
- 폐쇄형 플랫폼, Apple 
- 공개형 플랫폼, Andriod

<br>

### IoT 플랫폼 
- Producer -> Platform(Mart) -> Consumer 
- Platform의 예 -> App Store, SNS 

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


