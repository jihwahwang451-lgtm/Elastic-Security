# Elastic Security 8.x Offline (Air-Gapped) 구축 및 운영 실무 가이드

> **Elastic Security를 인터넷 환경에서 구축한 후 Air-Gapped(Offline) 환경으로 이전하여 운영하기 위한 한글 실무 가이드**

---

## 프로젝트 소개

본 프로젝트는 Elastic Security 8.x를 **폐쇄망(Air-Gapped)** 환경에서 구축하고 운영하기 위한 한글 기술 문서입니다.

Elastic 공식 문서를 기반으로 실무 구축 경험을 반영하여 다음 목표를 제공합니다.

- 단계별 구축 절차
- 운영 환경 기준 권장 설정
- Offline(Air-Gapped) 운영 방법
- Fleet Server 구축
- Elastic Package Registry(EPR)
- Endpoint Artifact Repository 구축
- Windows/Linux Agent 운영
- Elastic Defend 구성
- Detection Rule 작성
- Troubleshooting

본 저장소는 단순한 설치 문서가 아닌 **실무 구축 표준 문서**를 목표로 합니다.

---

# 프로젝트 목표

본 프로젝트의 목표는 다음과 같습니다.

- Elastic Stack 설치
- Kibana 구축
- Fleet Server 구축
- Air-Gapped 환경 구축
- Elastic Agent 등록
- Elastic Defend 운영
- Detection Rule 운영
- Offline 업데이트
- 장애 대응

최종적으로 다음 환경을 구축합니다.

```text
Internet

        │

        ▼

Elastic Stack 구축

        │

Fleet Server

        │

EPR

        │

Artifact Repository

        │

기능 검증

        │

Offline 이전

        │

Windows Agent

        │

Ubuntu Agent

        │

Elastic Security 운영
```

---

# 지원 환경

| 항목 | 지원 |
|------|------|
| Elastic Stack | 8.x |
| Ubuntu Server | 22.04 LTS |
| Windows | Windows 11 |
| Hypervisor | VMware Workstation Pro 17 |
| VMware ESXi | 8.x |

---

# 시스템 요구사항

## Host PC

| 항목 | 권장 |
|------|------|
| CPU | 8 Core 이상 |
| Memory | 64 GB 이상 |
| Storage | NVMe SSD 1 TB 이상 |

---

## Virtual Machine

| VM | 역할 | CPU | Memory | Disk |
|----|------|------|---------|------|
| ES-Server | Elasticsearch + Kibana + Fleet | 8 | 16 GB | 300 GB |
| Windows11 | Elastic Agent | 2 | 4 GB | 80 GB |
| Ubuntu | Elastic Agent | 2 | 2 GB | 40 GB |

---

# Repository 구조

```text
Elastic-Security-Offline-Guide/

README.md

SUMMARY.md

mkdocs.yml

docs/

configs/

scripts/

images/

diagrams/

pdf/
```

---

# 문서 구성

| 장 | 내용 |
|----|------|
| 01 | 구축 개요 |
| 02 | VMware |
| 03 | Ubuntu Server |
| 04 | TLS |
| 05 | Elasticsearch |
| 06 | Kibana |
| 07 | Fleet Server |
| 08 | Elastic Package Registry |
| 09 | Artifact Repository |
| 10 | Offline 구축 |
| 11 | Elastic Agent |
| 12 | Elastic Defend |
| 13 | Detection Rule |
| 14 | Upgrade |
| 15 | Troubleshooting |
| Appendix | 부록 |

---

# 빠른 시작

```bash
git clone https://github.com/<YOUR_ID>/Elastic-Security-Offline-Guide.git

cd Elastic-Security-Offline-Guide
```

문서는 `docs/` 디렉터리에서 순서대로 진행하는 것을 권장합니다.

```
01.Introduction.md

↓

02.VMware.md

↓

03.Ubuntu.md

↓

...

↓

15.Troubleshooting.md
```

---

# 제공 예정 자료

### 설정 파일

- elasticsearch.yml
- kibana.yml
- fleet.yml
- nginx.conf
- docker-compose.yml

### 자동화 스크립트

- install-elasticsearch.sh
- install-kibana.sh
- install-fleet.sh
- create-cert.sh
- backup.sh
- restore.sh

### 다이어그램

- Architecture.drawio
- Fleet.drawio
- Offline.drawio
- Network.drawio

---

# 프로젝트 원칙

모든 문서는 다음 원칙에 따라 작성됩니다.

- 실제 구축 환경 기준
- 단계별 실습
- 명령어 검증
- 설정 파일 전문 제공
- 운영 노하우 포함
- 장애 사례 포함
- 보안 권장사항 포함

---

# 향후 제공 예정

- PDF 기술서
- Word 문서
- GitHub Pages
- MkDocs Material
- Draw.io 원본
- 설치 자동화 스크립트
- 체크리스트
- 운영 매뉴얼

---

# 로드맵

| 버전 | 내용 |
|------|------|
| v0.1 | Repository 생성 |
| v0.2 | VMware 문서 |
| v0.3 | Ubuntu 문서 |
| v0.4 | Elasticsearch |
| v0.5 | Kibana |
| v0.6 | Fleet Server |
| v0.7 | EPR |
| v0.8 | Offline 구축 |
| v1.0 | 초판 완료 |

---

# 라이선스

본 프로젝트는 학습 및 연구 목적으로 작성됩니다.

Elastic 제품 사용 시에는 Elastic의 라이선스 정책을 반드시 확인하시기 바랍니다.

---

# 기여(Contribution)

버그 제보 및 문서 개선 제안은 Issue를 통해 등록할 수 있습니다.

문서 개선은 Pull Request 형태로 기여할 수 있도록 프로젝트를 구성할 예정입니다.

---

# 프로젝트 상태

**현재 상태:** 🚧 작성 진행 중

- Repository 구조 설계 완료
- README 작성 완료
- VMware 장 작성 예정
- Ubuntu 장 작성 예정
- Elasticsearch 장 작성 예정

---

> **목표:** Elastic Security Air-Gapped 구축을 위한 국내 최고 수준의 한글 실무 가이드를 제공하는 것.
