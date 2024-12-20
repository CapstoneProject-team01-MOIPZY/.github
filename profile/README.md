# 💡MOIPZY
사용자의 위치 및 날씨 정보를 기반으로 일정과 소유 의류를 고려하여 최적의 옷차림을 추천하는 웹 애플리케이션입니다.🌤️

[2024-2] 중앙대학교 소프트웨어학부 캡스톤 디자인 프로젝트  

<br>

## 💻 팀원

| 이름    | 이석주                                        | 박상훈                            | 강정훈                           |
| ------- | --------------------------------------------- | --------------------------------- | ------------------------------- |
| **git** | [hknhj](https://github.com/hknhj) | [sanghuniolsida](https://github.com/sanghuniolsida) | [KangJeungHun](https://github.com/KangJeungHun)   |

<br>
<br>

## 역할 분담
- **강정훈**: UI / UX
  - 피그마를 사용하여 기초적인 웹 와이어프레임 작성

- **박상훈**: Front-end
  - React를 사용하여 프론트엔드 전체 구현 담당
  - Vercel을 통하여 프론트엔드 배포

- **이석주**: Back-end
  - Springboot를 사용하여 백엔드 전체 구현 담당
  - AWS EC2, AWS RDS를 사용하여 백엔드 서버 배포

<br>

## 주요 기능
- **🌡️날씨 정보 제공**: 현재 위치의 실시간 날씨, 최고/최저 기온 표시
- **🧥옷차림 추천**: 사용자의 소유 의류를 활용하여 기온과 일정에 적합한 옷차림 추천
- **🗓️일정 연동**: 일정에 따라 옷 스타일 조정
- **🎨사용자 맞춤 경험**: 사용자별 데이터 저장 기능(선택한 옷차림, 옷차림 피드백, 옷 등록, 옷 정보 수정 및 삭제 등)
- **🤖챗봇 연동**: 카카오톡 챗봇을 연결하여 사용자 편의성 개선

<br>

## 기술 스택
**Frontend**: React.js, Vercel
<br>
<br>
**Backend** : 
<br>
<img src="https://img.shields.io/badge/java-007396?style=for-the-badge&logo=java&logoColor=white">
<img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
<br>
<img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
<img src="https://img.shields.io/badge/redis-FF4438?style=for-the-badge&logo=redis&logoColor=white">
<br>
<img src="https://img.shields.io/badge/amazonec2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white"> 
<img src="https://img.shields.io/badge/amazonrds-527FFF?style=for-the-badge&logo=amazonrds&logoColor=white"> 

**API**:
  - OpenWeather API: 실시간 날씨 데이터
  - Google Calendar API: 일정 연동
  - ChatGPT API: 스타일 추천 로직
**Authentication**: JWT, OAuth 2.0 (Google 로그인)
**Deployment**: AWS EC2, Vercel

<br>

## 🛠️ Architecture
![아키텍쳐 다이어그램](https://github.com/user-attachments/assets/91ec3e15-eed5-4c0a-85cb-f2665bc28948)

<br>

## 프로젝트 구조 (Backend)
```
src  
 └── main  
     ├── java  
     │   └── com.wrongweather.moipzy  
     │       ├── domain  
     │       │   ├── calendar      # 캘린더 관련 도메인 로직 및 API  
     │       │   ├── chatGPT       # ChatGPT API와의 통신 및 데이터 처리  
     │       │   ├── clothes       # 옷 관련 데이터 처리 및 로직  
     │       │   ├── clothImg      # 옷 이미지 업로드 및 관리  
     │       │   ├── crawling      # 옷 쇼핑몰 크롤링 관련 API  
     │       │   ├── email         # 이메일 전송 및 인증 처리  
     │       │   ├── jwt           # JWT 관련 인증 및 토큰 처리  
     │       │   ├── kakao         # 카카오톡 챗봇 연동 및 로직  
     │       │   ├── oAuth2        # OAuth 2.0 인증 처리  
     │       │   ├── schedule      # 서버 구동 시, 일정 시간 마다 일정, 기온 업데이트 하는 스케줄러  
     │       │   ├── style         # 옷차림 추천 로직  
     │       │   ├── token         # 구글 캘린더 연동을 위해 필요한 access/refresh token 관리  
     │       │   ├── users         # 사용자 관련 데이터 처리  
     │       │   ├── weather       # 날씨 데이터 연동 및 처리  
     │       │   └── BaseTimeEntity # 엔티티 생성 및 수정 시간 추적 공통 모듈  
     │       └── global  
     │           ├── MoipzyApplication # Spring Boot 애플리케이션 시작점  
     └── resources  
         ├── static.uploads.clothes  # 옷 이미지 업로드 저장소  
         ├── templates               # 이메일 템플릿 또는 기타 HTML 파일  
         └── application.yml         # Spring Boot 설정 파일
```
