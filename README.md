![header](https://capsule-render.vercel.app/api?type=rect&color=auto&height=250&section=header&text=CompanyCore%20(Server)&fontSize=70)

> Spring Boot 기반 기업용 그룹웨어 백엔드 API 서버 (팀 스터디)

<br>

## :open_book: 목차
- [프로젝트 소개](#프로젝트-소개)
- [👤 저의 기여](#-저의-기여)
- [🛠️ 기술 스택](#-기술-스택)
- [📁 프로젝트 구조](#-프로젝트-구조)
- [🔗 관련 레포지토리](#-관련-레포지토리)

<br>

<a id="프로젝트-소개"></a>
## 📋 프로젝트 소개

**CompanyCore Server**는 `companycore` (JavaFX 클라이언트)에 REST API를 제공하는 백엔드 서버입니다. 풀스택 개발 역량 함양을 위한 **팀 스터디** 프로젝트의 일환으로 구축되었습니다.

Spring Boot, Spring Data JPA, Spring Security(JWT)를 기반으로 하여 그룹웨어의 핵심 비즈니스 로직을 처리하는 API를 제공합니다.

### 🚀 주요 기능 (API)
- **인증 API:** Spring Security와 JWT를 이용한 로그인 및 토큰 기반 인증
- **사용자 관리 API:** 직원 생성, 이메일/사원번호 중복 체크, 직원 정보 조회 및 수정
- **근태 관리 API:** 출/퇴근 시간 기록, 휴가 신청 및 승인/반려, 월별 출근 통계 조회
- **업무 API:** (결재, 공지사항, 회의록 등)

<br>

<a id="-저의-기여"></a>
## 👤 저의 기여

이 풀스택 스터디 프로젝트에서 저의 주된 역할은 **클라이언트(companycore) 개발**이었습니다.

이 백엔드 서버는 제가 개발한 JavaFX 애플리케이션과 연동되는 **API 서버** 역할을 했습니다. 따라서 저는 이 서버가 제공하는 API 명세를 이해하고, 클라이언트에서 API를 호출하여 데이터를 연동하는 작업을 수행했습니다.

<br>

<a id="-기술-스택"></a>
## 🛠️ 기술 스택

| 구분 | 기술 |
|------|------|
| **Core** | ![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white) |
| **Data & ORM** | ![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white) |
| **Security** | ![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white) ![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white) |
| **Database** | ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white) |
| **Build** | ![Apache Maven](https://img.shields.io/badge/Apache_Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white) |

<br>

<a id="-프로젝트-구조"></a>
## 📁 프로젝트 구조
```bash
src/main/java/com/example/companycoreserver/
├── CompanyCoreServerApplication.java   # 메인 애플리케이션
├── config/
│   └── SecurityConfig.java             # Spring Security 설정
├── controller/
│   ├── AuthController.java             # 인증 API
│   ├── AttendanceController.java       # 근태관리 API
│   ├── LeaveRequestController.java     # 휴가 API
│   ├── TaskController.java             # 업무 API
│   └── UserController.java             # 사용자 API
├── dto/                                # 데이터 전송 객체
├── entity/                             # JPA 엔티티
│   ├── User.java
│   ├── Attendance.java
│   ├── LeaveRequest.java
│   └── ...
├── repository/                         # Spring Data JPA 리포지토리
│   ├── UserRepository.java
│   ├── AttendanceRepository.java
│   └── ...
├── service/                            # 비즈니스 로직
│   ├── AuthService.java
│   ├── UserService.java
│   ├── AttendanceService.java
│   └── ...
└── util/
    └── JwtUtil.java                    # JWT 유틸리티
