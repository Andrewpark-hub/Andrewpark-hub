# 박정언 (Jungun Park)

순천향대학교 컴퓨터소프트웨어공학과 3학년이고, 핀테크 랩(Fintech Lab)에서 학부연구생으로 있습니다.

지금은 스테이블코인 발행사의 동결 권한을 주제로 논문을 준비하고 있습니다. 동결 절차를 코드로 어디까지 강제할 수 있는지, 무고한 이용자를 위한 유예 기간은 어떻게 두는 게 맞는지를 보고 있습니다.

아래 저장소들은 공부하면서 만든 실습입니다. 규칙을 컨트랙트로 옮겨 보고, 처음 만든 버전이 어디서 깨지는지를 테스트로 남기는 식으로 정리하고 있습니다.

- 관심 분야: 스마트 컨트랙트 보안, 영지식 증명(Circom/Groth16 공부 중), 스테이블코인·RWA 토큰화

---

### 프로젝트

**직접 주제를 정한 실습**

| 프로젝트 | 내용 | 사용 기술 |
| :--- | :--- | :--- |
| [**Stablecoin Freeze ZK Lab**](https://github.com/Andrewpark-hub/stablecoin-freeze-zk-lab) | 동결 제안이 실행 전에 공개되는 문제는 커밋-리빌로, 동결 사유가 남지 않는 문제는 "승인된 사유 목록에 있다"는 Groth16 증명으로 막아 봤습니다. 증명에 대상 주소를 묶지 않으면 다른 주소로 복사해 쓸 수 있다는 것도 테스트로 확인했습니다(테스트 11개). 사유 목록이 바뀌면 진행 중인 증명이 무효가 되는 문제는 아직 남아 있습니다. | `Solidity`, `Foundry`, `Circom`, `snarkjs` |
| [**K-Gold Reserve Breaker Lab**](https://github.com/Andrewpark-hub/kgold-reserve-breaker-lab) | 핀테크 아이디어 공모전에서 설계한 금 담보 정산 시스템(K-Gold)의 발행 한도, 보유고 증명 오라클(노드 5개 중 3개 서명), 서킷브레이커를 만들어 봤습니다. 처음 세운 설계가 깨지는 곳 네 군데를 테스트로 남겼습니다(불변식 퍼즈 포함 25개). | `Solidity`, `Foundry`, `EIP-712` |
| [**SEC TSV Tokenized Stock Lab**](https://github.com/Andrewpark-hub/sec-tsv-tokenized-stock-lab) | SEC가 토큰화 주식에 '혁신 면제'를 승인했다는 기사를 보고, 기사에 나온 조건 4개(거래량 한도, 거래정지 연계, 발행사 거부권, 권리 승계)를 컨트랙트로 옮겨 봤습니다. 문장을 그대로 옮기면 어디서 어긋나는지 테스트 13개로 확인했습니다. | `Solidity`, `Foundry` |

**블록체인 밋업데이 실습 (2026, 20~22회차)**

| 프로젝트 | 내용 | 사용 기술 |
| :--- | :--- | :--- |
| [**Smart Contract Audit Lab**](https://github.com/Andrewpark-hub/smart-contract-audit-lab) | 22회차 보안 과정. 교재에 나온 취약점 5종(접근제어 누락, delegatecall 초기화, tx.origin 피싱, 재진입, cross-function 재진입)을 공격 코드와 고친 코드로 재현했습니다(테스트 10개). Slither를 직접 돌려서 무엇을 잡고 무엇을 놓치는지도 비교했습니다. | `Solidity`, `Foundry`, `Slither` |
| [**Multichain Wallet Lab**](https://github.com/Andrewpark-hub/multichain-wallet-lab) | 21회차 Wallet 과정. 니모닉과 EVM 주소를 라이브러리 없이 직접 계산해 라이브러리 결과와 대조했고, EIP-1559 트랜잭션을 단계별로 조립해 서명해 봤습니다(기본은 dry-run). EIP-712 digest도 직접 조립해 비교했습니다. 무한 approve를 찾아 회수하는 스크립트를 따로 붙였고, Sui·Solana는 같은 니모닉으로 주소를 파생해 조회하는 데까지 했습니다. | `Node.js`, `ethers.js`, `@mysten/sui`, `@solana/web3.js` |
| [**Indy DID Credential Demo**](https://github.com/Andrewpark-hub/indy-did-credential-demo) | 20회차 DID 과정. 로컬 Indy 네트워크(von-network)를 Docker로 띄우고 DID 등록, VC 발급, VP 검증 흐름을 따라가 봤습니다. 필요한 속성만 공개하는 증명은 AnonCreds(CL 서명) 라이브러리 기능을 썼습니다. | `Python`, `Hyperledger Indy`, `Docker` |

---

### 기술

**주 언어**
<br/>
<img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" />
<img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" />

**블록체인 실습에서 주로 쓴 것**
<br/>
<img src="https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white" />
<img src="https://img.shields.io/badge/Foundry-1C1C1C?style=for-the-badge&logo=ethereum&logoColor=white" />

**실습에서 써 본 것**
<br/>
<img src="https://img.shields.io/badge/Circom-6F42C1?style=for-the-badge" />
<img src="https://img.shields.io/badge/snarkjs_(Groth16)-6F42C1?style=for-the-badge" />
<img src="https://img.shields.io/badge/Slither-4B2E83?style=for-the-badge" />
<img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" />
<img src="https://img.shields.io/badge/ethers.js-2535A0?style=for-the-badge&logo=ethereum&logoColor=white" />
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
<img src="https://img.shields.io/badge/Hyperledger_Indy-2F3134?style=for-the-badge" />
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />

---

### 연락

<a href="https://www.linkedin.com/in/%EC%A0%95%EC%96%B8-%EB%B0%95-975ab1323/">
  <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
</a>

---

<details>
<summary><b>English</b></summary>

<br/>

I'm a third-year Computer Software Engineering student at Soonchunhyang University and an undergraduate research student in the Fintech Lab.

I'm preparing a paper on stablecoin issuers' power to freeze accounts: how far the freeze procedure can be enforced in code, and how to set a grace period that protects innocent holders.

The repositories below are study projects. I turn a rule into a contract, then write tests that show where my first version breaks.

- **Interests:** smart contract security, zero-knowledge proofs (learning Circom/Groth16), stablecoins and RWA tokenization
- **Main languages:** Java, Kotlin
- **Mostly used in blockchain labs:** Solidity, Foundry
- **Also used in labs:** Circom, snarkjs (Groth16), Slither, Node.js (ethers.js), Python, Hyperledger Indy, Docker

**Labs on topics I picked**

| Project | What I did | Tech |
| :--- | :--- | :--- |
| [**Stablecoin Freeze ZK Lab**](https://github.com/Andrewpark-hub/stablecoin-freeze-zk-lab) | Two gaps in a freeze multisig: pending proposals are public, and freeze reasons are not recorded. I tried commit-reveal for the first and, for the second, a Groth16 proof that the reason is on an approved list. Tests also show that a proof not bound to the target address can be copied to freeze someone else (11 tests). Still open: updating the list invalidates pending proofs. | `Solidity`, `Foundry`, `Circom`, `snarkjs` |
| [**K-Gold Reserve Breaker Lab**](https://github.com/Andrewpark-hub/kgold-reserve-breaker-lab) | Mint cap, a 3-of-5 proof-of-reserve oracle and a circuit breaker for K-Gold, a gold-backed settlement design from a fintech idea contest. The four places where my first design broke are kept as tests (25 tests, including invariant fuzzing). | `Solidity`, `Foundry`, `EIP-712` |
| [**SEC TSV Tokenized Stock Lab**](https://github.com/Andrewpark-hub/sec-tsv-tokenized-stock-lab) | Four conditions from a news report on the SEC's "innovation exemption" for tokenized stocks (volume cap, halt linkage, issuer veto, rights pass-through), turned into contracts to see where a literal translation goes wrong (13 tests). | `Solidity`, `Foundry` |

**Blockchain Meetup Day labs (2026, sessions 20 to 22)**

| Project | What I did | Tech |
| :--- | :--- | :--- |
| [**Smart Contract Audit Lab**](https://github.com/Andrewpark-hub/smart-contract-audit-lab) | Session 22, security track. Five textbook vulnerabilities (missing access control, delegatecall initialization, tx.origin phishing, reentrancy, cross-function reentrancy) reproduced as exploit/fix pairs (10 tests). I also ran Slither on each to compare what it catches and misses. | `Solidity`, `Foundry`, `Slither` |
| [**Multichain Wallet Lab**](https://github.com/Andrewpark-hub/multichain-wallet-lab) | Session 21, wallet track. Derived the mnemonic and EVM address without a library and checked them against library output, built and signed an EIP-1559 transaction step by step (dry-run by default), and assembled an EIP-712 digest by hand. I then added a script that finds and revokes unlimited approvals. Sui and Solana go only as far as deriving and looking up addresses from the same mnemonic. | `Node.js`, `ethers.js`, `@mysten/sui`, `@solana/web3.js` |
| [**Indy DID Credential Demo**](https://github.com/Andrewpark-hub/indy-did-credential-demo) | Session 20, DID track. Ran a local Indy network (von-network) in Docker and walked through DID registration, VC issuance and VP verification. Selective disclosure comes from the AnonCreds (CL signature) library. | `Python`, `Hyperledger Indy`, `Docker` |

</details>
