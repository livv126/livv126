## ☁️ 클라우드 인프라 및 보안 엔지니어

안전하고 확장성 있는 인프라 아키텍처를 고민합니다. IaC를 활용한 자동화와 하이브리드 클라우드 환경의 보안에 관심이 많습니다.

### 📜 Certifications
* **리눅스 마스터 2급**
* **네트워크 관리사 2급**
* **컴퓨터활용능력 1급**

### 🛠 Tech Stack

**Cloud & IaC**
![Azure](https://img.shields.io/badge/Microsoft_Azure-0089D6?style=flat-square&logo=microsoft-azure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?style=flat-square&logo=terraform&logoColor=white)

**OS & Infrastructure**
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Security**
![Metasploit](https://img.shields.io/badge/Metasploit-EE0000?style=flat-square&logo=metasploit&logoColor=white)

---

## 🚀 Projects

### 1. Terraform 기반 멀티 리전 클라우드 인프라 구축
> **기간:** 2026.01.13 ~ 2026.01.31 (3주)  
> **역할:** 클라우드 인프라 아키텍처 설계 및 IaC 코드 구현

* **인프라 코드화(IaC):** Terraform 활용 Azure 네트워크, 서버, 보안 자원 자동 배포 환경 구축
* **모듈화 설계:** 리소스별 모듈 분리를 통한 코드 재사용성 및 관리 효율성 확보
* **이중화 구성:** 메인 리전 – 세컨더리 리전 간 Azure Front Door 기반 Active-Active 트래픽 분산 아키텍처 설계
* **데이터 동기화:** MySQL Read Replica 구성을 통한 리전 간 데이터 복제 및 장애 대응 체계 마련

---

### 2. 하이브리드 클라우드 네트워크 및 보안 구축
> **기간:** 2026.01.27 ~ 2026.01.31 (1주)  
> **역할:** VPN 네트워크 연동 및 보안 정책 수립

* **VPN 터널링:** Azure VPN Gateway와 온프레미스 방화벽 장비(NGF-100) 간 IPSec 기반 Site-to-Site VPN 연결
* **보안 정책 적용:** 하이브리드 네트워크 구간별 트래픽 제어를 위한 NSG 인바운드/아웃바운드 정책 수립
* **로그 통합:** Azure EventHub 연동을 통한 클라우드 보안 로그 중앙 수집 파이프라인 구성

---

### 3. 시스템 모의해킹 및 취약점 분석 보고
> **기간:** 2025.12.24 ~ 2026.01.10 (2.5주)  
> **역할:** 웹 취약점 점검 시나리오 설계 및 결과 보고

* **공격 프레임워크 적용:** MITRE ATT&CK 프레임워크를 기반으로 공격 전술(Tactics) 및 기법(Techniques)을 선정하여 모의 침투 수행
* **시나리오 검증:** 초기 침투부터 권한 상승, 계정 탈취까지 이어지는 공격 체인(Kill Chain) 시나리오 검증
* **위험도 평가:** 발견된 취약점에 대해 CVSS(공통 취약점 등급 시스템) 기준 위험도를 산정하고 대응 방안 제시

---

### 4. GCP 기반 인프라 프로비저닝 및 애플리케이션 형상 관리(Configuration Management) 자동화
> **기간:** 2026.02.12 ~ 2026.02.21 (1.5주)  
> **역할:** 클라우드 인프라 배포, JVM 튜닝 및 애플리케이션 형상 관리 100% 자동화

* **인프라 자동화 및 DNS 제어:** Terraform을 활용하여 GCP 커스텀 VPC, 방화벽 규칙, 고성능 Compute Engine 배포를 자동화하고, Cloudflare 프록시 우회(UDP 통신 보장) 설정을 코드로 제어
* **WireGuard 기반 오버레이 네트워크 구성:** Tailscale을 도입하여 GCP 워크로드와 온프레미스(ELK) 간 복잡한 라우팅을 최소화하고, 종단 간(End-to-End) 암호화 통신을 구현
* **동적 변수 참조 (Cross-Host Facts):** Ansible 프로비저닝 단계에서 모니터링 노드의 VPN IP(`tailscale0`)를 실시간으로 수집(`gather_facts`)하여 타겟 노드에 주입하는 방식으로 하드코딩을 배제함.
* **애플리케이션 최적화 (Tuning):** 다중 접속 환경의 부하를 견디기 위해 Ansible로 JVM 메모리(Xms, Xmx 24g)를 자동 튜닝하고, 네트워크 최적화 클래스 파일(`NetworkZombiePacker.class`)을 패치함.
* **대규모 환경 변수 및 시크릿 관리:** 60여 개의 확장 모드 및 샌드박스 설정을 Jinja2 템플릿으로 구조화하여 배포하고, VPN 인증 키 및 데이터베이스 암호는 Ansible Vault로 암호화하여 보안성을 확보

---

### 🌱 Currently Learning
* Ansible 기반 구성 관리 자동화
* Kubernetes 컨테이너 오케스트레이션
