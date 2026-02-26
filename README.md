# Cloud Infrastructure & Security Engineer

가용성과 보안이 확보된 하이브리드 클라우드 아키텍처를 설계하는 인프라 엔지니어.

- **Infrastructure as Code:** Terraform, Ansible을 활용한 리소스 프로비저닝 및 구성 관리 자동화
- **Hybrid Architecture:** 클라우드와 온프레미스 간 안전한 네트워크 연동 및 이중화 아키텍처 설계
- **Security Visibility:** 시스템 취약점 분석 및 보안 정책 수립을 통한 인프라 방어 체계 및 가시성 확보

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
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Security & Network**
![Metasploit](https://img.shields.io/badge/Metasploit-EE0000?style=flat-square&logo=metasploit&logoColor=white)
![Tailscale](https://img.shields.io/badge/Tailscale-FFFFFF?style=flat-square&logo=tailscale&logoColor=black)

---

## 🚀 Projects

### 1. Azure Multi-Region DR Infrastructure (멀티 리전 클라우드 인프라 구축)
🔗 **Repository:** [azure-dr-infrastructure-terraform](https://github.com/livv126/azure-dr-infrastructure-terraform)
> **기간:** 2026.01.13 ~ 2026.01.31  
> **역할:** 클라우드 인프라 아키텍처 설계 및 IaC 코드 구현

* **인프라 자동화:** Terraform 활용 Azure 네트워크, 서버, 보안 자원 배포 환경 구축 및 리소스 모듈화.
* **이중화 구성:** 메인 리전 – 세컨더리 리전 간 Azure Front Door 기반 Active-Active 트래픽 분산 아키텍처 설계.
* **데이터 동기화:** MySQL Read Replica 구성을 통한 리전 간 데이터 복제 및 장애 대응 체계 마련.

---

### 2. Azure Hybrid Network & Security (하이브리드 클라우드 네트워크 및 보안 구축)
🔗 **Repository:** [azure-hybrid-network-infrastructure](https://github.com/livv126/azure-hybrid-network-infrastructure)
> **기간:** 2026.01.27 ~ 2026.01.31  
> **역할:** VPN 네트워크 연동 및 보안 정책 수립

* **네트워크 연동:** Azure VPN Gateway와 온프레미스 방화벽 장비(NGF-100) 간 IPSec 기반 Site-to-Site VPN 연결.
* **보안 정책 적용:** 하이브리드 네트워크 구간별 트래픽 제어를 위한 NSG 인바운드/아웃바운드 정책 수립.
* **로그 통합:** Azure EventHub 연동을 통한 클라우드 보안 로그 중앙 수집 파이프라인 구성.

---

### 3. System Security Audit & Penetration Testing (시스템 모의해킹 및 취약점 분석)
🔗 **Repository:** [system-security-audit-report](https://github.com/livv126/system-security-audit-report)
> **기간:** 2025.12.24 ~ 2026.01.10  
> **역할:** 웹 취약점 점검 시나리오 설계 및 결과 보고

* **공격 시나리오 검증:** MITRE ATT&CK 프레임워크 기반으로 초기 침투부터 권한 상승, 계정 탈취까지 이어지는 공격 체인 검증.
* **위험도 평가:** 발견된 시스템 취약점에 대해 CVSS 기준 위험도 산정 및 실무적인 대응 방안 제시.

---

### 4. Automated Observability Provisioning Stack (인프라 프로비저닝 및 형상 관리 자동화)
🔗 **Repository:** [automated-observability-provisioning-stack](https://github.com/livv126/automated-observability-provisioning-stack)
> **기간:** 2026.02.12 ~ 2026.02.21  
> **역할:** 클라우드 인프라 배포 및 애플리케이션 환경 자동화

* **인프라 및 네트워크 자동화:** Terraform을 활용한 클라우드 리소스 배포 자동화 및 Tailscale 기반의 온프레미스(ELK) VPN 연동 구성.
* **동적 변수 관리:** Ansible을 통해 모니터링 노드의 VPN IP를 동적으로 수집하여 타겟 노드 설정에 자동 반영.
* **로그 수집 문제 해결:** Filebeat에서 Logstash로의 로그 전송 실패 이슈를 디버깅하여 해결하고, 목적에 맞는 로그 필터링 로직 구현.
* **애플리케이션 최적화:** 다수 접속 환경에서의 클라이언트 튕김 현상 및 위치 동기화(Desync) 불량 문제 해결을 위해 무거운 확장 모드(150여 개)를 제거하고 JVM 메모리 튜닝 수행.

---

### 🌱 Currently Learning
* Ansible 기반 구성 관리 자동화
* Kubernetes 컨테이너 오케스트레이션
