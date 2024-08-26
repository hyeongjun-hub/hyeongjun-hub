# 조형준
- 이메일 : chogudwns@gmail.com
- 노션 : https://hyeongjun-hub.notion.site/TIL-22-01-681de6b68b7a492fb24de03f2b9cfbc9
- 깃허브 : https://github.com/hyeongjun-hub
- 블로그 : https://velog.io/@hyeongjun-hub


## Summary
신속한 장애 대응과 적절한 기술 도입을 통해 애플리케이션 개발자들에게 최적의 환경을 제공하는 DevOps 엔지니어입니다.

- 끊임없이 성장하는 사람
- 도움을 즐기는 사람
- 지식을 나누는 사람

## Skill
**Tech**: 
한 번 이상 다루어 본 기술들

<img src="https://img.shields.io/badge/Kubernetes-326CE5?&style=flat-square&logo=Kubernetes&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Ubuntu-E95420?style=flat-square&logo=Ubuntu&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Nginx-009639?&style=flat-square&logo=NGINX&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Jenkins-D24939?&style=flat-square&logo=Jenkins&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Java-007396?&style=flat-square&logo=Java&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Amazon S3-569A31?style=flat-square&logo=Amazon S3&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Python-3766AB?style=flat-square&logo=Python&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Firebase-FFCA28?&style=flat-square&logo=Firebase&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Spring Boot-6DB33F?&style=flat-square&logo=Spring Boot&logoColor=white"/></a>
<img src="https://img.shields.io/badge/MySQL-4479A1?&style=flat-square&logo=MySQL&logoColor=white"/></a>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?&style=flat-square&logo=JavaScript&logoColor=white"/></a>
<img src="https://img.shields.io/badge/React-61DAFB?&style=flat-square&logo=React&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Node.js-339933?&style=flat-square&logo=Node.js&logoColor=white"/></a>
<img src="https://img.shields.io/badge/MongoDB-47A248?&style=flat-square&logo=MongoDB&logoColor=white"/></a>
<img src="https://img.shields.io/badge/Jira Software-0052CC?&style=flat-square&logo=Jira Software&logoColor=white"/></a>



## Certification
- AWS Certified Solutions Architect – Associate

## Projects
### **On-premise Kubernetes 클러스터 유지 보수 및 관리 (23.07 ~ 현재)**

**기여도: 40% (관리자 총 3명)**

**Tech stack**

- Ubuntu, Kubernetes, Calico, MetalLB, HAProxy, Istio, Kiali, Prometheus, Grafana, Harbor, Keycloak, OAuth2 Proxy, Minio, OpenEBS, Helm, k9s, K6

**프로젝트 상세**

- 클러스터 버전 업그레이드(v1.25.9 → v1.26.9) 및 [업그레이드 정책](https://www.notion.so/6d62e76fa2234929adf87147a0ba956b?pvs=21) 구축
- kubernetes manifest로 배포되있는 legacy들을 Helm chart로 전환
- keycloak과 oauth2-proxy, istio를 활용해 사내 sso구축
- harbor 이미지, 차트 저장소 구축
- 클러스터 모니터링을 위한 Grafana dashboard 생성
- [네트워크 이슈 대응](https://velog.io/@hyeongjun-hub/%EC%BF%A0%EB%B2%84%EB%84%A4%ED%8B%B0%EC%8A%A4-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-%EB%AC%B8%EC%A0%9C-%ED%8A%B8%EB%9F%AC%EB%B8%94-%EC%8A%88%ED%8C%85)

### **사내 개발자 플랫폼 구축 (23.11 ~ 현재)**

애플리케이션 개발자가 쿠버네티스를 몰라도 GUI로 손쉽게 클러스터에 앱을 배포할 수 있도록 제작한 개발자 플랫폼. 

**Role:** **api-server, build-daemon(이미지 빌드 프로세스), 배포 템플릿**

**기여도: 33%**

**프로젝트 상세**
- 사용자는 git 주소와 옵션값 입력으로 사내 쿠버네티스 환경에 배포할 수 있음
- go를 사용해 frontend, api-server, build-daemon, controller로 마이크로서비스 개발
- operator 패턴을 활용, [kube-builder](https://github.com/kubernetes-sigs/kubebuilder) 오픈소스 사용
- 현재 alpha 릴리즈
    - 지원 템플릿: fastapi, triton, dockerfile

### **REST API 사용자 인증 및 로그 모니터링 시스템 구축 (24.08)**

사내 AI 기술을 제공하는 REST API를 외부 익명의 사용자들에게 제공하기 위해 API 호출 시 사용자 로그를 남기고 모니터링 및 차단할 수 있는 시스템 구축

**기여도: 90%**

**프로젝트 상세**
- Keycloak을 이용한 OIDC 제공
- Istio access log를 이용해 사용자 로깅
- Vector와 OpenSearch를 이용해 로그 수집 & 적재
- Grafana 대시보드로 수집한 로그를 모니터링
    - 트래픽 공격이나 비정상적인 사용자들을 탐지
- Istio authorization policy로 사용자 인증 및 차단

### [ArgoCD를 이용한 사내 CI/CD 파이프라인 구축](https://www.notion.so/108f03cd5949484e92abad6a109469bc?pvs=21) (24.02 ~ 24.03)

기존에 gitlab으로만 구축되었던 파이프라인에 ArgoCD를 도입하여 CD의 role을 ArgoCD가 가짐

개발자들이 직접 쿠버네티스에 배포되어있는 애플리케이션을 확인하고 운영할 수 있음

**기여도: 100%**

**Tech stack**
- ArgoCD, gitlab-ci, Harbor, Helm, Telegram, Prometheus, Grafana, Minio

**프로젝트 상세**
- ArgoCD PoC를 통해 ArgoCD가 가져올 기대효과 측정
- ArgoCD 구축으로 gitops 패턴 도입
- CI/CD 파이프라인 구축 가이드 작성
- 배포/장애 알림 시스템 구축으로 개발자들이 빠른 이슈 대응 가능해짐
- [gitlab-ci local](https://pypi.org/project/gitlabci-local/) 도입으로 파이프라인 테스트 용이성 증가
- gitlab-ci의 cache기능을 활용해 minio에 node_module을 캐시
    - 기존 2분 걸리는 다운로드 시간을 cache hit시 2초로 줄임

### [Kubernetes 환경 마인크래프트 배포 프로젝트](https://www.notion.so/Kubernetes-b896b564fa1a46e3a028bc88beddb557?pvs=21) (22.10 ~ 22.11)

**기여도: 25%**

**Role: 풀스택 개발, CI/CD 파이프라인 구축**

**Tech stack**
- EKS, EC2, ECR, Jenkins, ArgoCD, Github Webhook, Slack

### [아이디어스 어플 클론코딩 프로젝트](https://www.notion.so/d923d53bf3ff4eb287c4311a3630397d?pvs=21) (22.04 ~ 22.05)

## Education
**연세대학교 미래캠퍼스 컴퓨터공학과 복수전공(2021~2022)**

**연세대학교 SW 집중교육**
- Java programming 수료 (20.12 ~ 21.01)
- React.js 수료(21.06 ~ 21.07)

**Boot Camp**
- Rising camp (Server) 4기 우수수료(22.02 ~ 22.04)
  - https://hyeongjun-hub.notion.site/8e41e07472d44ab7a4643f478267cb24
- 쿠버네티스 전문가 양성 과정 5기 우수수료(22.08 ~ 22.11)
  - https://hyeongjun-hub.notion.site/Goorm-5-3fbd3ed1276c4dc99874e66bcb490670

**Study**
- [알고리즘 스터디](https://www.notion.so/97337a38ed6f437db78954adaea81344) (22.03 ~ 23.08)
- [CS 면접 스터디](https://www.notion.so/91ae262ecd3d49d3a402dc2acd4aea2a) (23.03 ~ 23.06)
- [AWS SAA 자격증 준비 스터디](https://www.notion.so/AWS-SAA-8ded051ed0fc43f7a5ae4248a5bc4534) (23.03 ~ 23.05)
- [DevOps 스터디] (23.04 ~ 24.03)
- 사내 네트워크 스터디 (24.06 ~ 24.08)
- 사내 쿠버네티스 스터디 (24.08 ~ 현재)

**기여도: 50%**

**Role:** **Backend 개발, aws 인프라 관리**

**Tech stack**
- Java, Spring Boot, EC2, RDS(MySQL), Mybatis, Nginx
