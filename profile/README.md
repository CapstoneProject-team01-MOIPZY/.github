# 💡MOIPZY
사용자의 위치 및 날씨 정보를 기반으로 일정과 소유 의류를 고려하여 최적의 옷차림을 추천하는 웹 애플리케이션입니다.🌤️


[2024-2] 중앙대학교 소프트웨어학부 캡스톤 디자인 프로젝트

## 💻 팀원

| 이름    | 이석주                                        | 박상훈                            | 강정훈                           |
| ------- | --------------------------------------------- | --------------------------------- | ------------------------------- |
| **git** | [hknhj](https://github.com/hknhj) | [sanghuniolsida](https://github.com/sanghuniolsida) | [KangJeungHun](https://github.com/KangJeungHun)   |

## 주요 기능
- **🌡️날씨 정보 제공**: 현재 위치의 실시간 날씨, 최고/최저 기온 표시
- **🧥옷차림 추천**: 사용자의 소유 의류를 활용하여 기온과 일정에 적합한 옷차림 추천
- **🗓️일정 연동**: 일정에 따라 옷 스타일 조정
- **🎨사용자 맞춤 경험**: 사용자별 데이터 저장 기능(선택한 옷차림, 옷차림 피드백, 옷 등록, 옷 정보 수정 및 삭제 등)
- **🤖챗봇 연동**: 카카오톡 챗봇을 연결하여 사용자 편의성 개선

## 기술 스택
- **Frontend**: React.js, Vercel
- **Backend**: Spring Boot, MySQL RDS, Nginx
- **API**:
  - OpenWeather API: 실시간 날씨 데이터
  - Google Calendar API: 일정 연동
  - ChatGPT API: 스타일 추천 로직
- **Authentication**: JWT, OAuth 2.0 (Google 로그인)
- **Deployment**: AWS EC2, Vercel
