# 하나 헤리티지 🧓🏻🏦
### 💬 시니어용 유언대용신탁 및 개인뱅킹 시스템

![표지](https://github.com/hee-ha/images/blob/main/00.%20%E1%84%91%E1%85%AD%E1%84%8C%E1%85%B5.jpg?raw=true)

### Index

- [⚡️ 프로젝트 정보](#%EF%B8%8F-프로젝트-정보)
- [🔥 작업 기간](#-작업-기간)
- [📌 프로젝트 및 기능 소개 ](#-프로젝트-및-기능-소개)
- [🌳 탐구 목표](#-탐구-목표)
- [🏕️ 아키텍처](#-아키텍처)
- [🛠️ 기술 스택](#%EF%B8%8F-기술-스택)
- [📚 백엔드 파일 트리](#-백엔드-파일-트리)
- [🦸🏻‍ 팀원 및 역할](#-팀원-및-역할)

<br/>

## ⚡️ 프로젝트 정보

- [디지털 하나로](https://hanaro.recruiter.co.kr/career/home) 2기 개발반 2차 프로젝트

<br/>

## 🔥 작업 기간

- 2024.05.09 - 2024.06.12

<br/>

## 📌 프로젝트 및 기능 소개 (작성중)

> 시니어용 유언대용신탁 및 개인뱅킹 시스템

- 🏦 오직 시니어만을 위한 웹뱅킹 시스템을 구축한다.
- 🪦 기존에 오프라인으로만 가입 가능한 하나은행의 '리빙트러스트'상품을 디지털화한다.

### ➊ 제목(작성예정)

| 헤더(작성예정(                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![회원가입](https://github.com/Claksion/images/blob/main/01.%20%E1%84%92%E1%85%AC%E1%84%8B%E1%85%AF%E1%86%AB%E1%84%80%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%B8.gif?raw=true) |
| 소셜 로그인 시, 등록되지 않은 계정일 경우 회원가입 절차가 진행됩니다.                                                                                                                            |


<br/>

## 🌳 탐구 목표 (작성중)

> 🧙 교실 속 필요한 다양한 소통에 Redis의 장점을 활용하며 탐구

- Redis의 **Sorted Set**과 AOP의 Around를 활용해 부하를 줄인 '선착순 자리선택'기능을 개발한다.
- Redis의 **Pub/Sub 패턴**과 **Socket**을 활용해 '실시간 채팅'기능을 개발한다.
- **Redis를 Session Storage로 사용**함으로써 빠른 응답속도의 장점을 취하고, 현재 서비스에 로그인돼 있는 클라이언트 정보를 출력한다.

<br/>

## 🏕️ 아키텍처 (작성중)
추가예정입니다.

<br/>

## 🛠️ 기술 스택 (작성중)

#### Environment

<img src="https://img.shields.io/badge/intellijidea-000000?style=flat&logo=intellijidea&logoColor=white">

#### Development

<img src="https://img.shields.io/badge/Java-007396?style=flat&logo=Java&logoColor=white"> <img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=flat&logo=Spring Boot&logoColor=white"> <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat&logo=Bootstrap&logoColor=white"> <img src="https://img.shields.io/badge/Javascript-F7DF1E?style=flat&logo=Javascript&logoColor=white">

#### DataBase

<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=MySQL&logoColor=white"> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat&logo=Redis&logoColor=white">

#### Communication

<img src="https://img.shields.io/badge/Slack-4A154B?style=flat&logo=Slack&logoColor=white"> <img src="https://img.shields.io/badge/Notion-000000?style=flat&logo=Notion&logoColor=white">

<br/>

## 📚 백엔드 파일 트리
> 도메인을 기준으로 프로젝트를 구조화하였습니다.
<details>
<summary>파일트리</summary>

```
📦 
└─ src
   ├─ main
   │  ├─ java
   │  │  └─ com
   │  │     └─ heeha
   │  │        ├─ HanaHeritageBeApplication.java
   │  │        ├─ domain
   │  │        │  ├─ account
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  ├─ auth
   │  │        │  │  ├─ Auth.java
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ filter
   │  │        │  │  │  ├─ CustomerAuthenticationFilter.java
   │  │        │  │  │  └─ ExceptionHandlingFilter.java
   │  │        │  │  ├─ jwt
   │  │        │  │  │  ├─ JwtTokenExtractor.java
   │  │        │  │  │  └─ JwtTokenProvider.java
   │  │        │  │  └─ service
   │  │        │  ├─ autoTransfer
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  ├─ scheduler
   │  │        │  │  │  └─ AutoTransferScheduler.java
   │  │        │  │  └─ service
   │  │        │  ├─ base
   │  │        │  │  ├─ entity
   │  │        │  │  │  ├─ BaseEntity.java
   │  │        │  │  │  └─ Status.java
   │  │        │  │  └─ service
   │  │        │  │     └─ BaseService.java
   │  │        │  ├─ consulting
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  ├─ customer
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  ├─ deathNotifier
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  ├─ depositsProduct
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  ├─ service
   │  │        │  │  └─ util
   │  │        │  │     └─ DepositsProductUtil.java
   │  │        │  ├─ history
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  ├─ livingTrust
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  ├─ ocr
   │  │        │  ├─ postBeneficiary
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  ├─ property
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  ├─ signDeposit
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  ├─ signSaving
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  ├─ sms
   │  │        │  │  ├─ controller
   │  │        │  │  ├─ dto
   │  │        │  │  ├─ entity
   │  │        │  │  ├─ repository
   │  │        │  │  └─ service
   │  │        │  └─ statistics
   │  │        │     ├─ controller
   │  │        │     ├─ dto
   │  │        │     ├─ entity
   │  │        │     ├─ repository
   │  │        │     └─ service
   │  │        └─ global
   │  │           ├─ aop
   │  │           │  ├─ Preference.java
   │  │           │  └─ PreferenceAop.java
   │  │           ├─ config
   │  │           │  ├─ BaseException.java
   │  │           │  ├─ BaseResponse.java
   │  │           │  ├─ BaseResponseStatus.java
   │  │           │  ├─ CorsConfig.java
   │  │           │  ├─ GlobalExceptionHandler.java
   │  │           │  ├─ JwtAuthorizationArgumentResolver.java
   │  │           │  ├─ RedisConfig.java
   │  │           │  ├─ SwaggerConfig.java
   │  │           │  └─ WebConfig.java
   │  │           ├─ job
   │  │           │  ├─ AutoTransferJobConfig.java
   │  │           │  ├─ AutoTransferTasklet.java
   │  │           │  ├─ SettlementCalculateTasklet.java
   │  │           │  ├─ SettlementJobConfig.java
   │  │           │  └─ SettlementValidTasklet.java
   │  │           └─ scheduler
   │  │              ├─ BatchScheduler.java
   │  │              └─ SmsScheduler.java
   │  └─ resources
   │     ├─ application-dev.yml
   │     └─ application.yml
   └─ test

```

</details>


<br/>

## 🦸🏻‍ 팀원 및 역할



| 황혜림 `팀장` | 정찬수 `부팀장` | 변정흠 `FE파트장` |
| --- | --- | --- |
| [<img src="https://avatars.githubusercontent.com/u/70644449?v=4"  height=150 width=150> ](https://github.com/hyerimmy) | [<img src="https://avatars.githubusercontent.com/u/77047099?v=4"  height=150 width=150> ](https://github.com/iamcharles98) | [<img src="https://avatars.githubusercontent.com/u/111037279?v=4"  height=150 width=150> ](https://github.com/quswjdgma83) |
| - 백엔드 프로젝트 초기셋팅<br/>- 예적금 가입 시 약관 동의<br/>- 일별 이체 내역 정산 (어드민)<br/>- 예약 문자 발송 (어드민)<br/>- 상담 및 상속 가입 관리 (어드민) | - 클라우드 환경 구축(서버 및 DB)<br/>- 실시간 금융상품 클릭수 통계(어드민)<br/>- 예금 가입, 계좌개설 및 조회<br/>- 고객 회원가입 및 조회<br/>- 유언대용신탁 가입 및 조회<br/>- sms 본인인증 | - 프론트엔드 프로젝트 초기셋팅<br/>- JWT 토큰 인증<br/>- OCR 인증<br/>- 로그인<br/>- 거래내역 조회<br/>- 홈화면(일반, 유언대용신탁) |


| 유민아 | 이지후 | 황유진 |
| --- | --- | --- |
| [<img src="https://avatars.githubusercontent.com/u/157072173?v=4"  height=150 width=150> ](https://github.com/minahyou) | [<img src="https://avatars.githubusercontent.com/u/140700053?v=4"  height=150 width=150> ](https://github.com/lee010207) | [<img src="https://avatars.githubusercontent.com/u/80201454?v=4"  height=150 width=150> ](https://github.com/YoujinHwang) |
| - 금감원 예적금 상품 조회 및 검색<br/>- 계좌 상세 조회<br/>- 유언 대용 신탁 계약서 내용 확인<br/>- Face ID 화면 제작 | - 계좌이체<br/>- 자동이체 등록 및 실행<br/>- 유언대용신탁 자산 조회<br/>- 유언대용신탁 자산 현황 시각화 | -예적금 가입 페이지 제작<br/>-준비물 페이지 제작<br/>-상담대기, 승인 api 연결<br/>-유언대용신탁 승인 api 연결 |
