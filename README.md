**사용자의 업무 흐름을 이해하고, 반복을 줄이는 백엔드 개발자 명민주입니다.**

Spring Boot와 Django를 기반으로 데이터 모델링, 인증·인가, 외부 API 연동을 구현해 왔습니다. 역할별 권한과 예외 상황, 운영 과정까지 고려하며 실제 사용 환경에서 안정적으로 작동하는 백엔드를 고민합니다.

기능을 구현하는 데 그치지 않고 사용자의 반복 업무와 병목을 파악해, 데이터와 API로 더 효율적인 서비스 흐름을 만드는 개발을 지향합니다.

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

> 매장 정보를 손쉽게 입력하고, 이를 기반으로 홍보 콘텐츠 제작, Instagram 게시, 피드백 제공까지 흩어진 업무를 하나의 흐름으로 연결한 서비스입니다.

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

> 일반 사용자에게 다중 대기열 서비스를 제공해 대기 시간을 줄이고, 부스 관리자, 행사 주최자의 대기열 관리 업무를 하나의 플랫폼에서 지원하는 서비스입니다.

**기간**: 2026.03 ~ 2026.04 | **역할**: Backend Developer

**핵심 기여**

- PostgreSQL 기반 데이터 모델과 REST API 설계
- JWT 인증과 사용자·부스 관리자·행사 주최자 역할별 권한 분리
- 행사장 도면을 R2에 저장하고 FastAPI 분석 결과를 운영자가 검수·저장하는 흐름 구현
- Redis TTL을 이용한 부스 관리자 가입과 엑셀 다운로드·SMTP 메일 기능 구현

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

👉 [Project README](https://github.com/typ0squir/bookspicker-backend)

---

### 🕵️ 실시간 멀티플레이 추리 게임 — Suspect X

> 참가자가 영상과 채팅으로 소통하며 제한 시간 안에 사건을 추리하는 실시간 웹 서비스입니다.

**기간**: 2026.01 ~ 2026.02 | **역할**: Frontend Developer

**핵심 기여**

- 대기실 입장·준비·게임 시작·진행 단계의 화면 및 상태 흐름 구현
- SockJS·STOMP 이벤트를 React 상태와 연결해 참여자 상태 동기화
- 서버 이벤트 순서와 화면 전환 조건을 분리해 실시간 상태 불일치 최소화

**Tech**: `React` `Vite` `JavaScript` `SockJS` `STOMP` `WebRTC`

👉 [Project README](https://github.com/typ0squir/suspect-x)

---

## 🧪 Proof of Concept

프로젝트에 핵심 기술을 적용하기 전, 구현 가능성과 외부 서비스 연동 방식을 작은 단위로 검증한 실험입니다.

### Instagram Image Generation PoC

**Related Project**: [맡케팅](https://github.com/typ0squir/matketing)

SDXL·ControlNet·RunPod를 활용해 상품 사진의 주요 피사체를 유지하면서 Instagram 게시용 이미지로 변환할 수 있는지 검증했습니다. 맡케팅의 홍보 콘텐츠 생성 기능을 구현하기 전, 이미지 생성 방식과 외부 생성 파이프라인의 적용 가능성을 확인하기 위해 제작했습니다.

👉 [GitHub](https://github.com/typ0squir/images-to-instagramable)

### Toss POS Integration PoC

**Related Project**: [맡케팅](https://github.com/typ0squir/matketing)

맡케팅의 온보딩 과정에서 사용자의 매장 Toss POS를 서비스와 연결하고, 메뉴명과 가격 정보를 불러올 수 있는지 검증했습니다. 검증한 연동은 결제 데이터를 수집하고 Instagram 게시물 지표와 비교해, 매장 운영자에게 홍보 활동에 대한 피드백을 제공하는 기능으로 확장했습니다.

👉 [GitHub](https://github.com/typ0squir/toss-pos-integration-poc)

### Venue Map Extraction PoC

**Related Project**: [Freeline](https://github.com/typ0squir/freeline)

전시장 도면 이미지에서 부스 영역의 좌표와 크기를 추출하고, 분석 결과를 편집 가능한 웹 지도로 변환할 수 있는지 검증했습니다. Freeline의 행사장 도면 분석·검수 기능을 구현하기 전, 이미지 분석 결과의 형태와 운영자 편집 흐름을 확인하기 위해 제작했습니다.

👉 [GitHub](https://github.com/typ0squir/venue-map-extraction-poc)

---

## 📖 Learning

- [TIL](https://github.com/typ0squir/TIL) — Java·Spring·CS 학습 기록
- [Algorithm Study](https://github.com/typ0squir/algorithm-study) — 알고리즘 문제 풀이 기록

---

## 📜 Certifications

* **2026.04** SQL 개발자(SQLD) 취득
* **2026.04** TOEIC Speaking IM3 취득

---

## 🎓 Education & Training

* **2025.07 ~ 2026.06** 삼성청년SW·AI아카데미(SSAFY) 14기 수료
* **2021.03 ~ 2025.08** 고려사이버대학교 디자인학부 졸업

