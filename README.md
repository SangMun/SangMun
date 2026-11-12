### 안녕하세요, 클라우드 엔지니어 이상문입니다 

AWS 인프라를 Terraform으로 구성하고 Kubernetes 위에서 서비스를 배포·운영합니다.
장애에 버티는 구조를 설계하고, **측정한 근거로 운영을 판단하는** 것을 중요하게 생각합니다.

**Stack** · AWS (EKS · RDS · Valkey · SQS · CloudFront · S3 · Lightsail) · Terraform · Kubernetes · Argo CD · Karpenter · KEDA · GitHub Actions · Datadog · Python · TypeScript

---

### 🎓 4x4 MIMO SVD 적응 변조 시뮬레이션 — 졸업작품
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
[CJ-AI-Cloud-Wave/O2-live-ai-ops](https://github.com/CJ-AI-Cloud-Wave/O2-live-ai-ops) · 담당: **서비스 · CI/CD · GitOps**

라이브커머스 서비스와, 채팅·메트릭에서 장애 신호를 찾아 진단·조치·검증하는 AIOps 플랫폼.
- **CI/CD** — Terraform CI/CD 스택, GitHub Actions 검증 잡, Trivy 이미지 스캔(CRITICAL 차단), ECR → Argo CD
- **서비스** — 주문 API·스키마, 주문 확정 워커, WebSocket 채팅 게이트웨이, CloudFront HLS 영상 배포
- **확장·가용성** — Karpenter·KEDA 도입, 처리량 측정으로 KEDA 임계 결정, 큐시트 기반 사전 확장,
  AZ 하나를 잃어도 버티도록 노드·NAT·RDS·Valkey 이중화
- **측정 기반 운영** — 채팅 붕괴점·서버 한계를 실측해 런북 안전선을 정정하고, 장애 시나리오를
  단계별로 실행·판정하는 실행기 작성
