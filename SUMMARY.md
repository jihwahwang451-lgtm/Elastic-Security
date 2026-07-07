# SUMMARY

# Elastic Security 8.x Offline (Air-Gapped) 구축 및 운영 실무 가이드

---

# PART I. 프로젝트 소개

* [프로젝트 소개](README.md)

---

# PART II. 기반 환경 구축

## Chapter 1. 구축 개요

* [1.1 문서 목적](docs/01.Introduction.md#11-문서-목적)
* [1.2 Elastic Security란](docs/01.Introduction.md#12-elastic-security란)
* [1.3 Air-Gapped 환경이란](docs/01.Introduction.md#13-air-gapped-환경이란)
* [1.4 구축 목표](docs/01.Introduction.md#14-구축-목표)
* [1.5 시스템 구성도](docs/01.Introduction.md#15-시스템-구성도)
* [1.6 구축 절차](docs/01.Introduction.md#16-구축-절차)
* [1.7 지원 버전](docs/01.Introduction.md#17-지원-버전)
* [1.8 시스템 요구사항](docs/01.Introduction.md#18-시스템-요구사항)

---

## Chapter 2. VMware 환경 설계

* [2.1 VMware 소개](docs/02.VMware.md#21-vmware-소개)
* [2.2 VMware 설치](docs/02.VMware.md#22-vmware-설치)
* [2.3 Virtual Machine 생성](docs/02.VMware.md#23-virtual-machine-생성)
* [2.4 CPU 구성](docs/02.VMware.md#24-cpu-구성)
* [2.5 Memory 구성](docs/02.VMware.md#25-memory-구성)
* [2.6 Disk 구성](docs/02.VMware.md#26-disk-구성)
* [2.7 Network 구성](docs/02.VMware.md#27-network-구성)
* [2.8 Snapshot 관리](docs/02.VMware.md#28-snapshot-관리)
* [2.9 Clone](docs/02.VMware.md#29-clone)
* [2.10 구축 검증](docs/02.VMware.md#210-구축-검증)

---

## Chapter 3. Ubuntu Server 설치

* [3.1 Ubuntu Server 소개](docs/03.Ubuntu.md#31-ubuntu-server-소개)
* [3.2 Ubuntu ISO 준비](docs/03.Ubuntu.md#32-ubuntu-iso-준비)
* [3.3 설치](docs/03.Ubuntu.md#33-설치)
* [3.4 Static IP 설정](docs/03.Ubuntu.md#34-static-ip-설정)
* [3.5 Hostname](docs/03.Ubuntu.md#35-hostname)
* [3.6 DNS](docs/03.Ubuntu.md#36-dns)
* [3.7 SSH](docs/03.Ubuntu.md#37-ssh)
* [3.8 UFW](docs/03.Ubuntu.md#38-ufw)
* [3.9 NTP](docs/03.Ubuntu.md#39-ntp)
* [3.10 Kernel Parameter](docs/03.Ubuntu.md#310-kernel-parameter)
* [3.11 Swap](docs/03.Ubuntu.md#311-swap)
* [3.12 검증](docs/03.Ubuntu.md#312-검증)

---

## Chapter 4. TLS 인증서

* [4.1 TLS 개요](docs/04.TLS.md#41-tls-개요)
* [4.2 PKI](docs/04.TLS.md#42-pki)
* [4.3 CA 생성](docs/04.TLS.md#43-ca-생성)
* [4.4 Server Certificate](docs/04.TLS.md#44-server-certificate)
* [4.5 Fleet Certificate](docs/04.TLS.md#45-fleet-certificate)
* [4.6 Endpoint Certificate](docs/04.TLS.md#46-endpoint-certificate)
* [4.7 검증](docs/04.TLS.md#47-검증)

---

# PART III. Elastic Stack 구축

## Chapter 5. Elasticsearch

* [5.1 Elasticsearch 소개](docs/05.Elasticsearch.md#51-elasticsearch-소개)
* [5.2 설치](docs/05.Elasticsearch.md#52-설치)
* [5.3 elasticsearch.yml](docs/05.Elasticsearch.md#53-elasticsearchyml)
* [5.4 Security](docs/05.Elasticsearch.md#54-security)
* [5.5 Heap](docs/05.Elasticsearch.md#55-heap)
* [5.6 Cluster](docs/05.Elasticsearch.md#56-cluster)
* [5.7 Index](docs/05.Elasticsearch.md#57-index)
* [5.8 API](docs/05.Elasticsearch.md#58-api)
* [5.9 Troubleshooting](docs/05.Elasticsearch.md#59-troubleshooting)

---

## Chapter 6. Kibana

* [6.1 Kibana 소개](docs/06.Kibana.md#61-kibana-소개)
* [6.2 설치](docs/06.Kibana.md#62-설치)
* [6.3 kibana.yml](docs/06.Kibana.md#63-kibanayml)
* [6.4 Fleet 활성화](docs/06.Kibana.md#64-fleet-활성화)
* [6.5 Dashboard](docs/06.Kibana.md#65-dashboard)
* [6.6 Troubleshooting](docs/06.Kibana.md#66-troubleshooting)

---

## Chapter 7. Fleet Server

* Fleet Architecture
* Fleet Policy
* Fleet Server 설치
* Enrollment
* Fleet 통신
* Fleet Troubleshooting

---

## Chapter 8. Elastic Package Registry

* EPR 소개
* Docker Image
* Offline EPR
* Registry 구성
* Package 관리
* Troubleshooting

---

## Chapter 9. Endpoint Artifact Repository

* Artifact 소개
* Endpoint Artifact
* Nginx 구성
* Artifact Download
* Offline 운영

---

# PART IV. Air-Gapped 구축

## Chapter 10. Offline 환경 구축

* Air-Gapped Architecture
* Offline 구성
* Offline Migration
* Offline Update
* Offline 운영
* Offline Troubleshooting

---

# PART V. Endpoint 구축

## Chapter 11. Elastic Agent

* Windows Agent
* Linux Agent
* Fleet Enrollment
* Agent Upgrade
* Troubleshooting

---

## Chapter 12. Elastic Defend

* Endpoint Security
* Malware Detection
* 정책 구성
* Isolation
* Response
* Exceptions

---

## Chapter 13. Detection Rule

* Detection Engine
* Rule
* KQL
* EQL
* ES|QL
* Rule 작성
* Alert
* Cases

---

# PART VI. 운영

## Chapter 14. 운영 및 유지보수

* Backup
* Restore
* Upgrade
* Monitoring
* License
* Performance Tuning

---

## Chapter 15. Troubleshooting

* Elasticsearch
* Kibana
* Fleet
* Agent
* Endpoint
* TLS
* Offline
* FAQ

---

# Appendix

* A. 명령어 모음
* B. Port
* C. Directory
* D. 설정 파일
* E. Docker
* F. REST API
* G. MITRE ATT&CK
* H. Elastic Common Schema(ECS)
* I. 참고자료
* J. 용어집

---
