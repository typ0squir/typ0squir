# 👋 About Me

**사용자의 업무 흐름을 이해하고, 반복을 줄이는 백엔드 개발자 명민주입니다.**

디자인 전공에서 익힌 사용자 관점을 바탕으로 Spring Boot와 Django를 활용해 데이터 모델링, 인증·인가, 외부 API 연동을 구현해 왔습니다.

기능을 먼저 구현하기보다 누가 어떤 일을 반복하고, 어느 단계에서 불편을 겪는지 파악한 뒤 필요한 기술을 안정적인 서비스 흐름으로 연결하는 개발을 지향합니다.

---

## 🛠 Tech Stack

### Backend

`Java` `Spring Boot` `Python` `Django REST Framework`

### Data

`PostgreSQL` `Redis`

### Integration & Tools

`REST API` `JWT` `OAuth2` `Docker` `Git` `n8n`

---

## 🧩 Projects

### 📣 소상공인 SNS 홍보 자동화 서비스 — 맡케팅

> 매장 정보 확인, 홍보 콘텐츠 제작, Instagram 게시로 흩어진 업무를 하나의 흐름으로 연결한 서비스입니다.

**기간**: 2026.05 ~ 2026.06 | **역할**: Backend Developer

**핵심 기여**

- Toss POS 데이터, 네이버 플레이스 정보, Meta OAuth·Instagram Graph API 연동
- Retry와 Circuit Breaker가 동일 클래스 내부 호출에서 동작하지 않는 원인을 Spring AOP 프록시 구조에서 찾아 외부 호출 Bean 분리
- 외부 API 장애가 전체 서비스로 전파되지 않도록 호출 단위의 보호 로직 구성
- Clova TTS 결과 캐시와 게시 흐름을 구현해 반복 호출과 채널 이동 최소화

**Tech**: `Java` `Spring Boot` `PostgreSQL` `OAuth2` `Instagram Graph API` `Resilience4j` `Docker`

👉 [Project README](https://github.com/typ0squir/matketing)

---

### 🎪 행사장 부스·대기열 운영 플랫폼 — Freeline

> 행사 방문자, 부스 관리자, 행사 주최자의 서로 다른 업무를 하나의 플랫폼에서 지원하는 서비스입니다.

**기간**: 2026.03 | **역할**: Backend Developer

**핵심 기여**

- PostgreSQL 기반 데이터 모델과 REST API 설계
- JWT 인증과 사용자·부스 관리자·행사 주최자 역할별 권한 분리
- 행사장 도면을 R2에 저장하고 FastAPI 분석 결과를 운영자가 검수·저장하는 흐름 구현
- Redis TTL을 이용한 주최자 인증과 엑셀 다운로드·SMTP 메일 기능 구현

**Tech**: `Java` `Spring Boot` `JPA` `PostgreSQL` `Redis` `JWT` `Cloudflare R2` `FastAPI`

👉 [Project README](https://github.com/typ0squir/freeline)

---

### 📚 취향 기반 도서 추천·독서 플랫폼 — Bookspicker

> 도서 추천부터 서재, 전자책 열람, 하이라이트와 리뷰까지 독서 경험을 연결한 서비스입니다.

**기간**: 2025.11 ~ 2025.12 | **역할**: Backend Developer

**핵심 기여**

- Django REST Framework 기반 도서·서재·리뷰·전자책 API 구현
- JWT 인증과 Google OAuth 로그인 연동
- 사용자 독서 활동과 콘텐츠 관계를 반영한 PostgreSQL 데이터 모델링
- EC2·Nginx 환경에 백엔드 배포

**Tech**: `Python` `Django` `Django REST Framework` `PostgreSQL` `JWT` `Google OAuth` `AWS EC2` `Nginx`

👉 [GitHub](https://github.com/typ0squir/bookspicker-backend)

---

### 🕵️ 실시간 멀티플레이 추리 게임 — Suspect X

> 참가자가 영상과 채팅으로 소통하며 제한 시간 안에 사건을 추리하는 실시간 웹 서비스입니다.

**기간**: 2026.01 ~ 2026.02 | **역할**: Frontend Developer

**핵심 기여**

- 대기실 입장·준비·게임 시작·진행 단계의 화면 및 상태 흐름 구현
- SockJS·STOMP 이벤트를 React 상태와 연결해 참여자 상태 동기화
- 타이머, 채팅, 비디오 영역을 게임 단계에 맞춰 제어
- 서버 이벤트 순서와 화면 전환 조건을 분리해 실시간 상태 불일치 최소화

**Tech**: `React` `Vite` `JavaScript` `SockJS` `STOMP` `WebRTC`

👉 [Project README](https://github.com/typ0squir/suspect-x)

---

## 🧪 Proof of Concept

### Drawing Map PoC

전시장 도면 이미지에서 부스 좌표와 크기를 추출하고, 편집 가능한 웹 지도로 변환할 수 있는지 검증했습니다.

👉 [GitHub](https://github.com/typ0squir/drawing-map)

### Instagram Image PoC

SDXL·ControlNet·RunPod를 활용해 상품 사진의 주요 피사체를 유지하면서 SNS 게시용 이미지로 변환하는 파이프라인을 검증했습니다.

👉 [GitHub](https://github.com/typ0squir/images-to-instagramable)

---

## 🤝 Collaboration

### Saving Box Challenge Backend

게임 요소를 활용한 저축 서비스에서 백엔드 기능 개발과 UX/UI 설계에 참여했습니다.

👉 [GitHub](https://github.com/Strangekim/saving_box_challenge_backend)

---

## 📖 Learning

- [TIL](https://github.com/typ0squir/TIL) — Java·Spring·CS 학습 기록
- [Algorithm Study](https://github.com/typ0squir/algorithm-study) — Python 알고리즘 문제 풀이 기록

---

## 🎓 Experience

- 삼성청년SW·AI아카데미(SSAFY) 수료
- SQL 개발자(SQLD) 취득
