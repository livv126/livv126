# Cloud Infrastructure & Security Engineer

안정적인 하이브리드 클라우드 연동과 인프라 프로비저닝 자동화에 주력하는 엔지니어입니다.

- **Infrastructure as Code:** Terraform, Ansible을 활용한 인프라 프로비저닝 및 반복 작업 자동화
- **Hybrid Architecture:** 퍼블릭 클라우드와 온프레미스 간의 안전한 네트워크 연동 및 이중화 설계
- **Security Visibility:** 시스템 취약점 점검(CVE/CCE) 및 모니터링 파이프라인(ELK) 기반의 관측성 확보

### 📜 Certifications
* **리눅스 마스터 2급**
* **네트워크 관리사 2급**
* **컴퓨터활용능력 1급**

### 🛠 Tech Stack

**Cloud & IaC**
![Azure](https://img.shields.io/badge/Microsoft_Azure-0089D6?style=flat-square&logo=microsoft-azure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white)

**OS & Infrastructure**
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**Security & Network**
![Metasploit](https://img.shields.io/badge/Metasploit-EE0000?style=flat-square&logo=metasploit&logoColor=white)
![Tailscale](https://img.shields.io/badge/Tailscale-FFFFFF?style=flat-square&logo=tailscale&logoColor=black)

---

## 🚀 Projects

### 1. Azure Multi-Region DR Infrastructure (멀티 리전 클라우드 인프라 구축)
> **목표:** 단일 장애점(SPOF) 리스크를 제거한 다중 리전 고가용성(HA/DR) 아키텍처 설계
* **인원 및 역할:** 5인 팀 프로젝트 / 팀장 (메인 아키텍처 설계 및 인프라 배포 총괄)
* **사용 기술:** Terraform, Azure Cloud
* **기간:** 2026.01.13 ~ 2026.01.31
* **Repository:** [azure-dr-infrastructure-terraform](https://github.com/livv126/azure-dr-infrastructure-terraform)

* **Situation:** 특정 리전 장애 발생 시에도 무중단 서비스를 제공하기 위한 이중화 아키텍처 요구.
* **Task & Action:**
  * Terraform을 활용해 Front Door 기반 Active-Active 트래픽 분산 및 다중 리전 인프라 구성.
  * Terraform 모듈 간 상태 참조(Implicit Dependency) 구조를 최적화하여 인프라 병렬 배포를 구현하고, 프로비저닝 소요 시간을 약 40% 단축.
  * 글로벌/지역 로드밸런서 계층화로 인해 발생한 웹 서버의 프로토콜 인식 오류(무한 리다이렉션)를 OS 구동 스크립트(`cloud-init`) 레벨에서 환경 변수를 주입하여 해결.
* **Result:** 재해 복구(DR) 시나리오에 대비한 인프라 가용성을 확보하고, IaC 기반의 일관된 배포 환경 마련.

### 2. Automated Observability Provisioning Stack (인프라 프로비저닝 및 중앙 모니터링 자동화)
> **목표:** 수동 개입을 최소화한 배포 자동화(IaC/CaC) 및 중앙 집중형 로그 수집(ELK) 환경 구축
* **인원 및 역할:** 개인 프로젝트
* **사용 기술:** Terraform, Ansible, GCP, ELK Stack, Tailscale
* **기간:** 2026.02.12 ~ 2026.02.21
* **Repository:** [automated-observability-provisioning-stack](https://github.com/livv126/automated-observability-provisioning-stack)

* **Situation:** 다수 서버 구성 시 발생하는 수동 설정의 비효율성을 개선하고, 분산된 서버 로그를 안전하게 중앙화할 필요성 대두.
* **Task & Action:**
  * Terraform으로 인프라 배포 후 Ansible Inventory를 동적 생성하도록 구성하여, OS 설정부터 미들웨어 설치까지 파이프라인 통합.
  * 퍼블릭 망을 통한 데이터 노출을 막기 위해 Tailscale 사설망(VPN)을 구성하여 로그 수집(Logstash) 트래픽 격리.
  * 비정형 애플리케이션 로그를 Grok 패턴으로 파싱해 시계열 분석이 가능하도록 만들고, 수집된 에러 로그를 바탕으로 JVM 메모리 튜닝 수행.
* **Result:** 대규모 마이그레이션이나 서버 증설 시 즉각 대응할 수 있는 자동화 환경을 구축하고, 데이터 기반의 트러블슈팅 환경 조성.

### 3. Azure Hybrid Network & Security (하이브리드 클라우드 네트워크 및 보안 구축)
> **목표:** 퍼블릭 클라우드의 확장성과 온프레미스의 보안성을 결합한 하이브리드 연동망 구축
* **인원 및 역할:** 5인 팀 프로젝트 / 클라우드 인프라 배포 및 VPN 네트워크 연동 총괄
* **사용 기술:** Terraform, Azure Cloud, BlueMax NGF-100(물리 방화벽), ELK Stack
* **기간:** 2026.01.27 ~ 2026.01.31
* **Repository:** [azure-hybrid-network-infrastructure](https://github.com/livv126/azure-hybrid-network-infrastructure)

* **Situation:** 핵심 데이터(DB)는 온프레미스에 격리하고, 웹 서버만 클라우드에 배치하는 하이브리드 연동 및 보안 관제 요구.
* **Task & Action:**
  * 퍼블릭 클라우드(Azure)와 온프레미스 방화벽(NGF-100) 간 IPsec 기반 Site-to-Site VPN 터널링 구축.
  * 네트워크 장비 결함으로 일정이 지연된 상황에서, 기존 대규모 DR 용으로 작성해 둔 Terraform 코드를 하이브리드 요건에 맞춰 필수 모듈 위주로 경량화하여 클라우드 인프라를 신속히 배포.
  * 물리 방화벽의 상태 꼬임(State Lock)으로 인한 VPN 연결 실패를 장비 초기화 및 재구성으로 해결하고, 통신 로그를 ELK Stack으로 연동.
* **Result:** 코드로 관리되는 인프라(IaC)의 높은 재사용성을 확인하고, 이기종 환경 간의 안전한 통신망 확보.

### 4. System Security Audit & Penetration Testing (시스템 보안 취약점 진단 및 리포트)
> **목표:** 인프라 마이그레이션 및 운영 단계에서 발생할 수 있는 잠재적 보안 위협 식별 및 대응
* **인원 및 역할:** 개인 프로젝트
* **사용 기술:** Nmap, OpenVAS, Metasploit
* **기간:** 2025.12.24 ~ 2026.01.10
* **Repository:** [system-security-audit-report](https://github.com/livv126/system-security-audit-report)

* **Situation:** 레거시 인프라 환경의 보안 취약점(CVE)을 사전 점검하여, 안전한 클라우드 전환 및 운영 기준 마련 필요.
* **Task & Action:**
  * 이기종 서버(Windows/Linux)를 대상으로 EOL(End of Life) OS 취약점 및 불필요한 개방 포트 스캐닝(Nmap, OpenVAS) 수행.
  * 식별된 취약점을 바탕으로 실제 공격 표면(Attack Surface)을 검증하고 권한 상승 가능성 점검.
  * 소스코드 패치로 인한 가용성 저하를 방지하기 위해, 인바운드 방화벽(ACL) 통제 정책 및 '최소 권한의 원칙'에 기반한 아키텍처 개선 방안 도출.
* **Result:** 인프라 관점에서의 실무적인 취약점 조치 방안(네트워크 격리 등)을 포함한 보안 감사 리포트 작성.

---

## 🎯 Vision

**"인프라의 안정성은 예측 가능한 변수를 통제하는 것을 넘어, 예상치 못한 충격에도 유연하게 복구되는 환경을 만드는 것이라고 생각합니다."**

단순히 서버를 띄우는 데 그치지 않고, 인프라를 코드로 관리(IaC)하여 운영 장애를 신속하게 복구하고 시스템의 잠재적 취약점을 선제적으로 차단하는 클라우드 엔지니어가 되겠습니다.
