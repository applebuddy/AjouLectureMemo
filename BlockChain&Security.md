<br>
<br>



# 블록체인과 보안

### 1st 오프라인 강의



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



<br><br>



## 4th 오프라인 강의

## **블록체인 합의 알고리즘**

- **다수 참여자들의 일치 된 의사 결정**
- **무결성 문제를 해결하기 위한 알고리즘**의 일종
- 대부분의 블록체인 합의 알고리즘은 새로운 개념이 아니라 새로운 사용 방법 
  - 비크코인 블록은 10분 주기로 생성
  - **모든 함의 알고리즘에는 Trade-Off 가 있음**
  - **일반적으로 확장성과 기밀성 사이의 Trade-Off**

- **Two general's Problem**
  - **A, B가 서로 적이라 할 때, 서로 동시에 공격하기 위해 합의가 이루어 지기 위해 A장군, B장군이 서로 합의를 볼 수 있는지를 확인해본 인종의 가상실험** (1972)
  - **이 문제는 실제로는 해결 불가로 판명** 됨
    - **불확실성에 의해 결국 함께 적국의 도시를 공격할 수 없음**
- **Bizantine Gerneral Problem**
  - **서로 같은시간에 공격을 해야 이기는 동시성 문제**
  - **앞서 언급 된 Two General's Problem에서 확장 된 문제**
  - **A, B가 아닌 여러 명의 상황으로 가정하는 문제**
    - 사령관이 전달한 것과 동일한 내용의 전령이 각 장군들 사이로 오가게 할 수 있을까?
    - 적어도 틀린 메시지를 받더라도 이를 구분해낼 수 있을까?
    - 항상 모두가 같은 답을 가진 상황을 유지하게 할 방법이 있을까?
      - **이와 같은 질문의 답을 찾는 것이 비잔틴 장군(Bizantine Gerneral Problem) 문제**임
- **BFT Algorithm** 
  - **Byzantine fault Tolerance**
  - **비잔티움 장군 문제의 딜레마에서 파생되는 실패들을 막기위한 시스템**
  - **장애가 있더라도 전체의 3분의 1을 넘지 않는다면 시스템이 정상작동하도록 허용하는 합의 알고리즘**
    - **비트코인은 작업증명(PoW) 이라는 합의구조를 도입 하였음**

- **PBFT Algorithm**
  - **Practical Pyzantine Fault Tolerance**
  - **리더 노드와 참여 노드의 메세지(블록) 송/수신 과정을 통해 합의**



### **블록체인 합의 알고리즘2**

- **작업증명 (Proof of Work, PoW)**
  - **블록체인에서 가장 보편적으로 사용 중인 확률적 합의 알고리즘**
  - **비트코인이 사용하고 있는 합의 알고리즘 방법** 
  - **전력소비가 큰 단점**이 있음
- **지분증명 (Proof of Stake, PoS)**
  - **초기 코인 분배 문제**
    - **초기에 코인을 많이 보유한 참여자가 블록생성에 유리하다는 점에 의한 공정성 문제** 
    - **코인을 많이 보유한 사람이 유리**함
  - **PoS의 단점을 보완한 DPoS 지분증명 방식**이 존재
    - **DPoS : 위임지분 증명 (Delegated Proof of Stake)**

<br><br>



# ✭ 블록체인과 보안 기말고사 문제 후보

- **총 6문제, o/x문제가 섞여있음 (이더리움은 o/x문제 에서만 냈음)**
- **12차시, 이더리움 취약점(중간고사 이후) ~ +병행수업 간 배웠던 Hyper Ledger 내용**
  - 합의 알고리즘 강의는 시험에 나오지 않음
- **월렛**
- **초기 싱크 블록버스터, ~~~ 버스터** 등에 대한 이해
- **비트코인 페이먼트 프로세싱 절차**
- **Astro 첨자 Contract**
- **Hyper Ledger에 대한 설명**