### 안녕하세요, 인프라·클라우드 엔지니어 이상문입니다

Linux와 네트워크를 공부하고 AWS와 Kubernetes로 서비스를 구축했습니다.
서비스를 운영하면서 발생할 수 있는 장애를 살펴보고, 부하와 복구 과정을 직접 측정해봤습니다.

**학습·프로젝트에서 사용한 기술**



**Infra** · Linux (Ubuntu) · systemd · Bash · Nginx · 네트워크 (TCP/IP · 서브네팅 · NAT · ACL) · 백업·복구

**Cloud** · AWS (EKS · RDS · Valkey · SQS · CloudFront · S3 · Lightsail) · Terraform · Kubernetes · Argo CD · Karpenter · KEDA · GitHub Actions

**Observability** · Prometheus · Grafana · Datadog

**Language** · Python · Bash

---

## 📜 자격증

- 정보처리기사
- PC정비사 2급
- 자동차운전면허 1종 보통


---

## 🤝 대외활동

### 점프렌즈 서포터즈 (2025.03.05 ~ 2025.04.30)

「2025년 충북 청년성장프로젝트」 공식 서포터즈 점프렌즈 1기로서 기간동안 다양하고 창의적인 홍보활동을 수행했습니다.
---

## 📚 학습·교육

### 🐧 코딩자율학습단 리눅스 19기 — 독학 (2026.01 ~ 2026.02, 4주)
[주차별 학습 기록](https://blog.naver.com/lsmeforna3/224151036118) · 우분투

책 한 권(14장)을 4주 동안 완주하며 매주 학습 내용을 블로그에 정리했습니다.
사용자·권한, 프로세스·시그널, Bash 스크립트(조건·반복·함수·확장, `errexit`·`pipefail`),
리디렉션·파이프라인, apt·systemd 유닛 파일, grep·find 등 필수 CLI 도구

### ☁️ CJ올리브네트웍스 AI Cloud Wave 1기 — 교육 (2026.06.19 ~ 08.28)
고용노동부 K-Digital Training 선도기업 아카데미 · 과목마다 CJ 현직자 특강

| 구분 | 과목 | 주요 실습 |
|---|---|---|
| 기본교과 64H | AI 인프라를 위한 네트워크 기초 | OSI·TCP/IP, 서브네팅·VLSM·CIDR, ACL, NAT (Packet Tracer) |
| | Linux 서버 운영 및 클라우드 인프라 | Linux 서버 관리(권한·systemd), AWS EC2·VPC·S3·IAM, Nginx 배포 |
| 심화교과 208H | 컨테이너 및 Kubernetes 운영 | Docker·Compose, Kubernetes, Helm |
| | 운영 데이터 수집 및 Observability | Prometheus·Grafana·Loki·Tempo·OpenTelemetry, 결함 주입 |
| | AIOps 기반 이상탐지 및 분석 | 운영 데이터 기반 이상탐지 |
| | 운영 자동화를 위한 LLM 활용 | Bedrock LLM 에이전트로 Kubernetes 장애 진단 |
| | RAG 및 Agent 기반 운영 자동화 | RAG 기반 운영 자동화, Dify |
| 프로젝트 120H | AI 기반 인프라 구축 프로젝트 | 팀 프로젝트·현직자 멘토링 → 아래 O2 |

---

## 🛠 프로젝트

### 🛒 O2 Live Commerce AIOps — 최종 프로젝트 (2026.08, 5인 · 3주)
[CJ-AI-Cloud-Wave/O2-live-ai-ops](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops) · 주 담당: **서비스 개발 · CI/CD 및 GitOps**

라이브커머스 서비스와 채팅·운영 지표를 활용해 장애를 진단하고 대응하는 AIOps 플랫폼을 5인 팀으로 구축했습니다. 서비스와 배포를 주로 맡았으며 자동 확장, 가용성 구성, 관측과 장애 시나리오 검증에도 참여했습니다. 교육 프로젝트 환경에서 구현하고 검증했으며, 일부 장애 시나리오의 전체 자동 복구는 추가 검증이 필요합니다.

**주요 기여**

- **서비스 개발** — 방송 정보 조회 API의 캐시 계층과 주문 API·워커를 구현했습니다. Valkey의 재고 차감과 멱등성을 함께 처리하고, SQS를 통해 접수한 주문을 MySQL에 기록하도록 구성했습니다. [#28](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/28) · [#33](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/33) · [#36](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/36) · [#37](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/37)
- **실시간 채팅·영상** — WebSocket 채팅 게이트웨이와 Valkey Pub/Sub 기반 전파를 구현하고, MediaMTX와 CloudFront를 이용한 HLS 영상 송출을 구성했습니다. [#38](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/38) · [#68](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/68) · [#71](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/71)
- **배포 자동화·보안** — GitHub Actions 검증과 ECR·Argo CD 기반 GitOps 배포를 구성하고, Trivy 이미지 검사에서 CRITICAL 취약점을 차단했습니다. 배포 매니페스트를 별도 저장소로 분리했습니다. [#3](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/3) · [#8](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/8) · [#11](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/11) · [#12](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/12)
- **자동 확장·가용성** — 부하를 측정해 Karpenter·KEDA를 도입하고, 방송 큐시트를 이용해 예상 트래픽 전에 파드를 늘리는 기능을 구현했습니다. 노드·NAT·핵심 애드온을 여러 AZ에 나눠 구성했습니다. [#113](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/113) · [#127](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/127) · [#152](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/152) · [#176](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/176) · [#198](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/198) · [#203](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/203)
- **관측·장애 대응 검증** — Datadog APM을 적용하고 알림을 Dify 웹훅에 연결했습니다. 채팅 부하 측정, 장애 시나리오 실행기와 복구 판정 기준 개선에 참여했습니다. [#47](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/47) · [#98](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/98) · [#210](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/210) · [#241](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/241) · [#251](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/251)

<details>
<summary><b>분야별 상세 작업 보기</b></summary>

#### 서비스·데이터 흐름

- 방송 메타데이터는 로컬 캐시·Valkey·MySQL 순서로 조회하고, 자주 바뀌는 재고는 Valkey에서 따로 조회했습니다. [#28](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/28)
- 주문 접수 시 멱등 확인과 재고 차감을 묶어 중복 차감을 막고, 비동기 워커에서 MySQL 기록과 오류 유형별 재처리를 구현했습니다. [#33](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/33) · [#36](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/36) · [#37](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/37)
- API 준비 상태(readyz)에서 MySQL·Valkey 연결을 확인하고, 스키마와 마이그레이션을 구성했습니다. [#25](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/25) · [#26](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/26)
- WebSocket 채팅을 여러 파드로 전파하고, 서비스 이벤트를 Kinesis로 보내도록 연결했습니다. [#38](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/38) · [#50](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/50)
- HLS 영상만 CloudFront를 통과하도록 경로를 제한하고, 플레이리스트와 영상 세그먼트의 캐시 정책을 나눴습니다. [#68](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/68) · [#71](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/71) · [#73](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/73)

#### CI/CD·인프라

- 팀의 네트워크·EKS Terraform 코드를 버전 관리에 편입하고, Argo CD·Load Balancer Controller 등 플랫폼 구성을 코드로 정리했습니다. [#4](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/4)
- Python·Node 검증 잡을 확장하고, Trivy 검사에서 CRITICAL 취약점이 나오면 이미지 푸시를 막도록 구성했습니다. [#8](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/8) · [#11](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/11) · [#12](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/12)
- 파드당 주문 처리량을 측정해 KEDA 확장 기준을 정했습니다. [#127](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/127)
- 파드 준비 시간을 측정해 사전 확장 시점을 정하고, 방송 큐시트를 읽어 캐시 워밍과 파드 사전 확장을 하는 cue-warmer를 구현했습니다. [#152](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/152) · [#176](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/176)
- AZ 하나가 멈춰도 남은 노드가 트래픽을 받아낼 수 있게 노드 수를 조정하고, AZ별 NAT와 핵심 애드온 분산을 구성했습니다. [#198](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/198) · [#201](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/201) · [#202](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/202) · [#203](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/203)

#### 관측·장애 대응

- Datadog APM으로 서비스별 추적을 추가하고, 모니터 알림을 Dify 웹훅으로 연결했습니다. [#47](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/47) · [#98](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/98)
- 채팅 장애 시나리오의 부하 주입·조치·검증을 단계별로 실행하고, 결과를 따로 판정하는 실행기를 작성했습니다. [#210](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/210)
- 부하를 다시 측정해 채팅 서버 한계에 대한 기존 추정치를 바로잡았습니다. [#220](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/220) · [#241](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/241)
- 장애 중인데 복구로 잘못 판정되던 문제를 찾아 응답 시간 조건을 추가했습니다. [#251](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/251)
- 실행할 런북이 없으면 재진단을 반복하지 않고 사람에게 넘기도록 워크플로를 수정했습니다. [#246](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/246)
- 결제사 장애 시뮬레이션 결과를 근거로 PG Failover 런북을 활성화했습니다. [#263](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/263)
- Bedrock 호출 시간 제한 문제를 추적하고, 모델별 응답 시간을 비교해 해결 방안을 문서화했습니다. [#252](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/252)
</details>

<details>
<summary><b>주요 머지 PR (전체 96건 중 21건)</b></summary>

분야별로 대표 PR만 골랐습니다. 각 PR에는 작업 내용과 당시 검증 범위·남은 과제가 기록돼 있습니다. 전체 목록은 [저장소의 머지 PR](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pulls?q=is%3Apr+is%3Amerged+author%3ASangMun)에서 볼 수 있습니다.

**CI/CD·보안**

- [#8 feat(ci): 이미지 취약점 스캔 추가 (Trivy)](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/8)
- [#11 feat(ci): Trivy를 CRITICAL 차단 모드로](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/11)
- [#12 feat(ci): verify 잡을 Python·Node로 확장](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/12)
- [#32 fix(ci): 버전 라벨을 함께 갱신하고 조용한 no-op 을 막는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/32)

**서비스 개발**

- [#28 feat(api): 방송 진입 스냅샷과 캐시 계층](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/28)
- [#33 Feat/api orders](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/33)
- [#36 feat(order-worker): 주문 확정 워커](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/36)
- [#38 feat(chat-gateway): WebSocket 채팅 게이트웨이](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/38)
- [#50 feat(events): 이벤트 목적지를 stdout에서 Kinesis로 바꾼다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/50)

**영상 송출**

- [#68 feat(media): CloudFront 로 HLS 를 배포한다 (07-media)](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/68)
- [#73 fix(cloudfront): /hls 이외 경로를 엣지에서 끊는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/73)

**자동 확장**

- [#113 feat(scaling): Karpenter 와 KEDA 를 넣는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/113)
- [#127 feat(order-worker): KEDA 임계를 정하려고 처리량을 재고 권한을 붙인다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/127)
- [#152 docs(measurements): 파드 Ready 시간을 재서 사전 확장 리드타임을 확정한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/152)
- [#176 feat(warmer): 큐시트 기반 파드 사전 확장을 추가한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/176)

**가용성 (AZ 이중화)**

- [#198 infra(eks): AZ 하나를 잃어도 남은 AZ 가 받아낼 수 있게 노드를 넷으로 둔다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/198)
- [#203 infra(network): NAT 게이트웨이를 AZ 마다 둔다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/203)

**관측·장애 대응 검증**

- [#47 Feat/datadog apm](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/47)
- [#95 feat(loadtest): 부하 테스트 스크립트를 만들고 노드 사이징을 실측한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/95)
- [#210 feat(scenario): S1 을 단계별로 돌리고 스스로 판정하는 실행기를 만든다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/210)
- [#263 feat(s3): PG Failover 런북을 실측 근거로 active 로 올린다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/263)
</details>

### 📈 BTC/XRP 선물 페이퍼 트레이딩 봇 — 개인 프로젝트 (2026.08 ~)
[paper-futures](https://github.com/SangMun/paper-futures) · Python · AWS Lightsail · GitHub Actions

**자동매매 후 손해를 분석하고 보완하는** 자동매매 봇입니다.
- 실시간 루프와 과거 리플레이가 같은 엔진 코드를 쓰도록 설계, 미래참조 시점 오류 5건 수정
- pytest 551개 CI, 서버 pull 방식 커밋 기반 배포·자동 롤백(CD)
- systemd로 전략별 계좌 분리 운용, S3 일일 백업, 디스코드 알림
- 채택·기각한 실험을 [EXPERIMENTS.md](https://github.com/SangMun/paper-futures/blob/main/EXPERIMENTS.md)에 기록

### 📱 Mobile To-Do — 모바일프로그래밍 기말 과제 (2025.09 ~ 2025.12)
[mobile-todo](https://github.com/SangMun/mobile-todo) · Kotlin · Spring Boot · AWS RDS

앱 안에만 저장되던 투두리스트를 Spring Boot 서버와 AWS RDS(MySQL)에 연결해, 앱을 다시 실행해도 데이터가 유지되도록 개선했습니다.
- Android(Kotlin) 앱에서 Retrofit으로 할 일 조회·추가·삭제 API 호출
- Spring Boot REST API와 Spring Data JPA로 DB 연결

### 🎓 4x4 MIMO SVD 적응형 변조 시뮬레이션 — 졸업작품 (2024.09 ~ 2025.11, 2인)
[mimo-svd-adaptive-modulation](https://github.com/SangMun/mimo-svd-adaptive-modulation) · MATLAB · 2인 팀 · 2025 전자정보대학 캡스톤디자인 졸업작품전시회 출품 (2025.11.13)

SVD로 MIMO 채널을 부채널로 분리하고, 부채널 SINR에 따라 변조 방식(BPSK~64QAM)과
전력(water-pouring)을 바꾸는 적응 변조를 고정 변조와 BER·처리량으로 비교했습니다.



- SVD로 분리한 각 부채널에 워터푸어링 방식으로 전력을 할당하고, 유효 SNR에 따라 BPSK·QPSK·16-QAM·64-QAM을 선택했습니다.
- Eb/N0에 따른 BER과 처리량을 비교했습니다. 적응 변조에는 SVD 기반 수신을, 고정 변조에는 MMSE 수신을 적용했습니다.
- 전시 자료에서 적응 변조의 처리량은 신호 조건이 좋아질수록 증가했지만 BER이 모든 고정 변조보다 낮지는 않았습니다. 수신 방식도 다른 비교이므로 차이를 변조 방식만의 효과로 단정할 수 없습니다.

- **담당 역할:** 2인 팀으로 적응형 변조 방식 설계부터 MATLAB 시뮬레이션 구현, 성능 분석까지 공동으로 진행했습니다.
