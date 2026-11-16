### 안녕하세요, 클라우드 엔지니어 이상문입니다 

AWS 인프라를 Terraform으로 구성하고 Kubernetes 위에서 서비스를 배포·운영합니다.
장애에 버티는 구조를 설계하고, **측정한 근거로 운영을 판단하는** 것을 중요하게 생각합니다.

**Stack** · AWS (EKS · RDS · Valkey · SQS · CloudFront · S3 · Lightsail) · Terraform · Kubernetes · Argo CD · Karpenter · KEDA · GitHub Actions · Datadog · Python · TypeScript

---

### 🎓 4x4 MIMO SVD 적응형 변조 시뮬레이션 — 졸업작품
[mimo-svd-adaptive-modulation](https://github.com/SangMun/mimo-svd-adaptive-modulation) · MATLAB

SVD로 MIMO 채널을 부채널로 분리하고, 부채널 SINR에 따라 변조 방식(BPSK~64QAM)과
전력(water-pouring)을 바꾸는 적응 변조를 고정 변조와 BER·처리량으로 비교했습니다.

### 🐧 코딩자율학습단 리눅스 19기 — 독학 (2026.01 ~ 2026.02, 4주)
[주차별 학습 기록](https://blog.naver.com/lsmeforna3/224151036118) · 우분투

책 한 권(14장)을 4주 동안 완주하며 매주 학습 내용을 블로그에 정리했습니다.
사용자·권한, 프로세스·시그널, Bash 스크립트(조건·반복·함수·확장, `errexit`·`pipefail`),
리디렉션·파이프라인, apt·systemd 유닛 파일, grep·find 등 필수 CLI 도구

### ☁️ CJ올리브네트웍스 AI Cloud Wave 1기 — 교육 (2026.06.19 ~ 08.28, 400시간)
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

### 📈 BTC/XRP 선물 페이퍼 트레이딩 봇 — 개인 프로젝트 (2026.08 ~)
[paper-futures](https://github.com/SangMun/paper-futures) · Python · AWS Lightsail · GitHub Actions

수익보다 **"이 전략이 우연이 아닌가"를 검증하는 절차**에 무게를 둔 자동매매 봇입니다.
- 실시간 루프와 과거 리플레이가 같은 엔진 코드를 쓰도록 설계, 미래참조 시점 오류 5건 수정
- pytest 551개 CI, 서버 pull 방식 커밋 기반 배포·자동 롤백(CD)
- systemd로 전략별 계좌 분리 운용, S3 일일 백업, 디스코드 알림
- 채택·기각한 실험을 [EXPERIMENTS.md](https://github.com/SangMun/paper-futures/blob/main/EXPERIMENTS.md)에 기록

### 🛒 O2 Live Commerce AIOps — 최종 프로젝트 (2026.08, 5인 · 3주)
[CJ-AI-Cloud-Wave/O2-live-ai-ops](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops) · 주 담당: **서비스 개발 · CI/CD 및 GitOps**

라이브커머스 서비스와 채팅·운영 지표를 활용해 장애를 진단하고 대응하는 AIOps 플랫폼을 5인 팀으로 구축했습니다. 서비스와 배포를 주로 맡았으며 자동 확장, 가용성 구성, 관측과 장애 시나리오 검증에도 참여했습니다.

**주요 기여**

- **서비스 개발** — 방송 정보 조회 API의 캐시 계층과 주문 API·워커를 구현했습니다. Valkey의 재고 차감과 멱등성을 함께 처리하고, SQS를 통해 접수한 주문을 MySQL에 기록하도록 구성했습니다. [#28](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/28) · [#33](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/33) · [#36](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/36) · [#37](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/37)
- **실시간 채팅·영상** — WebSocket 채팅 게이트웨이와 Valkey Pub/Sub 기반 전파를 구현하고, MediaMTX와 CloudFront를 이용한 HLS 영상 송출을 구성했습니다. [#38](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/38) · [#68](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/68) · [#71](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/71)
- **배포 자동화·보안** — GitHub Actions 검증과 ECR·Argo CD 기반 GitOps 배포를 구성하고, Trivy 이미지 검사에서 CRITICAL 취약점을 차단했습니다. 배포 매니페스트를 별도 저장소로 분리했습니다. [#3](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/3) · [#8](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/8) · [#11](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/11) · [#12](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/12)
- **자동 확장·가용성** — 부하를 측정해 Karpenter·KEDA를 도입하고, 방송 큐시트를 이용해 예상 트래픽 전에 파드를 늘리는 기능을 구현했습니다. 노드·NAT·RDS·Valkey를 여러 AZ에 걸쳐 구성했습니다. [#113](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/113) · [#127](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/127) · [#152](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/152) · [#176](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/176) · [#198](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/198) · [#200](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/200) · [#203](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/203)
- **관측·장애 대응 검증** — Datadog APM을 적용하고 알림을 Dify 웹훅에 연결했습니다. 채팅 부하 측정, 장애 시나리오 실행기와 복구 판정 기준 개선에 참여했습니다. [#47](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/47) · [#98](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/98) · [#210](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/210) · [#241](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/241) · [#251](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/251)

<details>
<summary><b>분야별 상세 작업과 검증 결과 보기</b></summary>

#### 서비스·데이터 흐름

- 방송 메타데이터는 로컬 캐시·Valkey·MySQL을 활용하고, 수시로 바뀌는 재고는 Valkey에서 별도로 조회했습니다. [#28](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/28)
- 주문 접수 시 멱등 확인과 재고 차감을 묶어 중복 차감을 방지하고, 비동기 주문 워커에서 MySQL 기록과 오류 유형별 재처리를 구현했습니다. 주문 상태 조회도 연결했습니다. [#33](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/33) · [#35](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/35) · [#36](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/36) · [#37](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/37)
- API 준비 상태에서 MySQL·Valkey 연결을 확인하도록 하고, 방송·상품·주문 스키마 및 마이그레이션을 구성했습니다. [#25](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/25) · [#26](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/26)
- WebSocket 채팅을 여러 파드로 전파하고, 이벤트에 채팅 원문 대신 길이·해시 등의 정보를 사용하도록 구성했습니다. 서비스 이벤트를 Kinesis로 보내는 연결도 작업했습니다. [#38](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/38) · [#29](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/29) · [#50](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/50)
- 프론트엔드를 실제 API·WebSocket에 연결하고 HLS 재생을 구성했습니다. 정상 재생 중 플레이어가 반복 재부착되던 문제를 측정해 수정했습니다. [#40](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/40) · [#66](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/66) · [#267](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/267)
- HLS만 CloudFront를 통과하도록 경로를 제한하고, 플레이리스트와 영상 세그먼트의 캐시 정책을 분리했습니다. [#68](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/68) · [#71](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/71) · [#73](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/73)

#### CI/CD·인프라

- 기존 팀의 네트워크·EKS Terraform 코드를 버전 관리에 편입하고, Argo CD와 Load Balancer Controller 등의 플랫폼 구성을 코드로 정리했습니다. [#4](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/4)
- Python·Node 프로젝트의 검증 잡을 확장하고, Trivy 검사 결과를 기록한 뒤 CRITICAL 취약점이 있으면 이미지 푸시를 막도록 구성했습니다. [#8](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/8) · [#11](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/11) · [#12](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/12)
- 파드당 주문 처리량을 측정하고 KEDA에 SQS 조회 권한을 부여했습니다. 측정 시점에는 파드당 약 49건/초를 확인하고 12개 파드까지 살펴봤습니다. [#127](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/127)
- 파드 준비 시간을 측정해 사전 확장 리드타임을 정하고, 큐시트를 읽어 캐시 워밍과 파드 사전 확장을 수행하는 cue-warmer를 구현했습니다. 파드 확장 기능의 실제 워머 이미지 내 동작은 해당 PR 당시 배포 후 확인 과제로 남겼습니다. [#152](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/152) · [#156](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/156) · [#157](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/157) · [#160](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/160) · [#176](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/176)
- AZ 장애 시 남은 노드의 수용량을 고려해 노드를 4대로 조정하고, AZ별 NAT와 RDS·Valkey 이중화 및 핵심 애드온 분산을 구성했습니다. [#198](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/198) · [#200](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/200) · [#201](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/201) · [#202](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/202) · [#203](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/203) · [#205](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/205)
- Valkey 백업이 존재하지 않는 MySQL 재고 반영 배치를 근거로 꺼져 있음을 확인해 백업을 켜고 주석을 수정했습니다. 장애 전환 시험에서 애플리케이션 기준 RDS 15초, Valkey 37초의 중단을 기록했습니다. [#200](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/200) · [#207](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/207)

#### 관측·장애 대응과 측정

- Datadog APM으로 서비스별 추적을 추가하고, 모니터 알림을 Dify 웹훅으로 연결했습니다. 서비스 측 이벤트를 Kinesis에 전달하는 지점도 구성했습니다. [#47](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/47) · [#50](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/50) · [#98](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/98)
- 채팅 장애 시나리오의 부하 주입·조치·검증을 단계별로 실행하고, 에이전트와 별도로 결과를 판정하는 실행기를 작성했습니다. [#210](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/210)
- 채팅 전파 부하를 다시 측정해 기존 추정치를 정정했습니다. 전파 초당 12만 건에서는 지연이 증가해도 파드가 유지됐고, 16만 건에서는 메모리 한도에 도달해 종료됐습니다. [#220](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/220) · [#238](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/238) · [#241](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/241)
- 채팅 제한 조치가 실제로는 사용자 발화 도달률을 낮추는 문제를 분석해 제한 창과 런북 값을 수정했습니다. 수정 후 실환경 E2E 재측정은 해당 PR의 후속 과제로 남겼습니다. [#261](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/261)
- 장애 중에도 복구로 잘못 판정되던 문제를 발견해 실측을 바탕으로 p99 응답 시간 50ms 이하 조건을 추가했습니다. 로컬 시뮬레이션에서 판정 분기를 확인했으며, 격리 후 실측은 당시 남은 과제로 기록했습니다. [#251](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/251) · [#256](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/256)
- 실행 가능한 런북이 없을 때 재진단을 반복하지 않고 사람에게 넘기도록 워크플로를 수정했습니다. 해당 PR 기준 저장소 구현과 테스트를 마쳤고 실환경 반영은 후속 과제로 남겼습니다. [#246](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/246)
- 결제사 장애 시뮬레이션과 사람의 검증 이력을 근거로 PG Failover 런북의 활성화를 정리했습니다. 해당 PR에서는 두 번째 실행의 E2E 증거가 남은 과제였습니다. [#263](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/263)
- Bedrock 호출의 60초 시간 제한과 Dify 설정이 서로 다른 구간에 적용됨을 추적하고, 같은 입력에서 모델별 응답 시간을 비교해 해결 방안을 문서화했습니다. [#252](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/252)

</details>

<details>
<summary><b>작성한 머지 PR 전체 목록 (96건)</b></summary>

아래는 프로젝트 저장소에서 `SangMun` 작성자로 검색한 머지 PR입니다. 각 PR에는 작업 내용과 당시 검증 범위·남은 과제가 기록돼 있습니다.

- [#267 fix(frontend): 재생 중인데 8초마다 플레이어를 재부착하던 것을 고친다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/267)
- [#263 feat(s3): PG Failover 런북을 실측 근거로 active 로 올린다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/263)
- [#261 fix(s1): 채널 총량 제한 카운터를 전송 창 단위로 바꾸고 상한을 실측값으로 잡는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/261)
- [#256 fix(s2): 진입 알림에서 원인 해설을 빼고 pod_load_skew 복구 판정을 고친다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/256)
- [#252 docs(T): Dify 컨테이너 재생성 502와 Bedrock read timeout을 남긴다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/252)
- [#251 fix(s2): 복구 판정을 p99 축으로 옮기고 실험 게이트를 갱신한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/251)
- [#249 Fix/s2 entry broadcast id tag](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/249)
- [#248 Docs/s2 canary cpu sweep](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/248)
- [#246 feat(s3): active 런북이 없으면 재진단 대신 ESCALATED로 끝낸다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/246)
- [#245 Docs/s2 cue warmer conflict](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/245)
- [#244 fix(s2): canary livenessProbe 확장 + assessment_input.observed_at 정규화](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/244)
- [#243 fix(s2): 라이브에만 있던 실험 게이트 값을 tfvars에 받아적는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/243)
- [#242 fix(s2): 런북의 replicas를 실행기 allowlist에 맞추고 어긋나면 시딩을 막는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/242)
- [#241 measure(s1): 서버 실제 한계를 다시 재고 M-010 의 안전선을 정정한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/241)
- [#238 test(s1): 판정 축을 런북과 맞추고 붕괴점 측정기를 더한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/238)
- [#234 fix(monitoring): S1 차단률 모니터를 소문자 failure_code 로 조회한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/234)
- [#220 measure(s1): 채팅 붕괴점을 재려다 지표 파이프라인이 못 믿을 값을 준다는 걸 찾았다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/220)
- [#210 feat(scenario): S1 을 단계별로 돌리고 스스로 판정하는 실행기를 만든다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/210)
- [#207 docs: AZ 이중화의 실측·판단·함정을 남긴다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/207)
- [#205 infra(eks): coredns·metrics-server 분산에 matchLabelKeys 를 넣는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/205)
- [#203 infra(network): NAT 게이트웨이를 AZ 마다 둔다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/203)
- [#202 infra(keda): KEDA 세 컴포넌트를 이중화하고 AZ 로 흩는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/202)
- [#201 infra(eks): coredns 와 metrics-server 를 AZ 로 흩는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/201)
- [#200 infra(data): RDS 와 Valkey 를 AZ 이중화하고 없는 복구 경로를 근거로 꺼져 있던 백업을 켠다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/200)
- [#198 infra(eks): AZ 하나를 잃어도 남은 AZ 가 받아낼 수 있게 노드를 넷으로 둔다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/198)
- [#184 docs(warmer): capacity 모듈 설명이 order-worker 를 뺀 채로 남아 있었다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/184)
- [#183 브랜치는 이미 있다. 커밋 메시지:](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/183)
- [#176 feat(warmer): 큐시트 기반 파드 사전 확장을 추가한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/176)
- [#162 infra(cicd): cue-warmer ECR 저장소를 서비스 목록에 추가한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/162)
- [#160 feat(warmer): 큐시트 사전 확장의 캐시 워밍만 구현한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/160)
- [#157 feat(api): 큐시트 저장소를 구성한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/157)
- [#156 feat(contracts): 큐시트 v1 계약과 검증을 추가한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/156)
- [#152 docs(measurements): 파드 Ready 시간을 재서 사전 확장 리드타임을 확정한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/152)
- [#128 fix(keda): 컨트롤러를 관리형 노드에 묶는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/128)
- [#127 feat(order-worker): KEDA 임계를 정하려고 처리량을 재고 권한을 붙인다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/127)
- [#119 Docs/karpenter verification](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/119)
- [#113 feat(scaling): Karpenter 와 KEDA 를 넣는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/113)
- [#101 fix(datadog): trace-agent 에 리소스를 준다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/101)
- [#100 fix(datadog): 주문 응답 p95 모니터의 no-data 알림을 끈다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/100)
- [#98 fix(datadog): 알림 대상을 @webhook-o2-dify 로 옮긴다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/98)
- [#97 docs(troubleshooting): 부하 테스트에서 막혔던 셋을 남긴다 (T-015 ~ T-017)](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/97)
- [#95 feat(loadtest): 부하 테스트 스크립트를 만들고 노드 사이징을 실측한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/95)
- [#93 docs: 유휴 스핀 수정 후 실측을 갱신하고 T-013 을 남긴다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/93)
- [#92 docs(measurements): metrics-server 로 처음 보인 클러스터 실측을 남긴다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/92)
- [#91 fix(api,order-worker): 이벤트 SDK 를 유휴 스핀이 고쳐진 커밋으로 올린다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/91)
- [#90 feat(eks): metrics-server 를 애드온 목록에 넣는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/90)
- [#81 feat(frontend): 방송 썸네일과 이벤트 배너도 실제 사진으로 맞춘다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/81)
- [#79 feat(frontend): 상품 도형을 실제 제품 사진으로 바꾼다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/79)
- [#77 chore(seed): 시연 상품을 실제 올영 편성으로 바꾼다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/77)
- [#76 fix(frontend): 조용히 삼켜지던 재생 실패를 드러내고 자산을 압축한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/76)
- [#75 fix(frontend): 재생 복구를 회로 차단기로 묶고 정지 감시를 붙인다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/75)
- [#73 fix(cloudfront): /hls 이외 경로를 엣지에서 끊는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/73)
- [#71 feat(media): 영상을 CloudFront 로 내보낸다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/71)
- [#69 fix(frontend): 재생이 끊기면 다시 붙는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/69)
- [#68 feat(media): CloudFront 로 HLS 를 배포한다 (07-media)](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/68)
- [#66 feat(media): 방송 화면에서 HLS 를 재생한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/66)
- [#64 feat(media): MediaMTX 송출 비밀번호를 클러스터에 넣는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/64)
- [#62 docs: 스케일링 부품을 필요해질 때 넣기로 한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/62)
- [#58 fix(datastream): env 태그를 dev 로 통일한다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/58)
- [#57 docs: 문서가 실제와 어긋난 곳을 맞추고 영상 스택을 07-media 로 옮긴다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/57)
- [#56 fix(api): 특가가 열리기 전에는 팔지 않는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/56)
- [#55 feat(frontend): 방송 시작 전 화면을 만들고 자리표시자 이미지를 걷어낸다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/55)
- [#52 fix(chat-gateway): event_id를 SDK와 같은 ULID로 만든다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/52)
- [#50 feat(events): 이벤트 목적지를 stdout에서 Kinesis로 바꾼다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/50)
- [#49 Fix/api contract schema sync](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/49)
- [#47 Feat/datadog apm](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/47)
- [#46 Docs/schema and openapi](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/46)
- [#45 feat(frontend): 올리브영 앱 형태로 화면을 다시 만든다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/45)
- [#44 feat(frontend): 화면 장식을 되살린다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/44)
- [#43 fix(frontend): HTTP 에서 화면이 안 뜨던 것 수정](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/43)
- [#41 fix(frontend): SPA 경로가 404 나던 것 수정](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/41)
- [#40 feat(frontend): 계약에 맞춰 실제 API 에 연결](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/40)
- [#39 fix(chat-gateway): 런타임 이미지에서 npm 제거](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/39)
- [#38 feat(chat-gateway): WebSocket 채팅 게이트웨이](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/38)
- [#37 feat(api): 주문 상태 조회](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/37)
- [#36 feat(order-worker): 주문 확정 워커](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/36)
- [#35 Feat/api order amount](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/35)
- [#34 feat(infra): order-worker·chat-gateway ECR 저장소 추가](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/34)
- [#33 Feat/api orders](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/33)
- [#32 fix(ci): 버전 라벨을 함께 갱신하고 조용한 no-op 을 막는다](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/32)
- [#31 fix(api): 런타임 스테이지에 남은 옛 SDK 설치 블록 제거](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/31)
- [#30 Fix/api sdk install via git](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/30)
- [#29 feat(api): 이벤트 SDK 배선과 inventory.check 발행](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/29)
- [#28 feat(api): 방송 진입 스냅샷과 캐시 계층](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/28)
- [#27 feat(api): 데모 시드 스크립트](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/27)
- [#26 feat(api): 스키마와 Alembic 마이그레이션](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/26)
- [#25 feat(api): readyz 추가와 데이터 계층 연결](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/25)
- [#15 chore(argocd): 안 쓰는 applicationSet·notifications 컨트롤러 비활성화](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/15)
- [#12 feat(ci): verify 잡을 Python·Node로 확장](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/12)
- [#11 feat(ci): Trivy를 CRITICAL 차단 모드로](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/11)
- [#10 fix(testpage): nginx 베이스 이미지 1.27 → 1.31](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/10)
- [#9 fix(api): Spring Boot 3.5.0 → 3.5.16](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/9)
- [#8 feat(ci): 이미지 취약점 스캔 추가 (Trivy)](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/8)
- [#4 feat(infra): 네트워크·EKS 코드 흡수와 04-platform 추가](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/4)
- [#3 refactor: 매니페스트를 별도 저장소로 분리](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/3)
- [#1 test: PR 경로와 브랜치 보호 검증](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops/pull/1)

</details>

