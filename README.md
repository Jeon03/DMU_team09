# 프로젝트 ShareStory
![ShareStory 로고](./images/logo.png)

## 📙 프로젝트 개요

**ShareStory**는 *‘공유(Share)’*와 *‘이야기(Story)’*를 결합한 플랫폼으로,  
단순한 중고 거래를 넘어 사용자 간 **경험과 신뢰를 나누는 공간**을 지향합니다.

기존 중고거래 서비스에 **커뮤니티 기능**과 **실시간 경매 시스템**을 통합하여,  
사용자는 단순 거래 외에도 후기 공유, 정보 나눔, 관심사 기반 소통이 가능하며  
이를 통해 **신뢰 기반의 거래 환경**을 제공합니다.

또한, **실시간 입찰 기반 경매 기능**은 플랫폼의 **재미 요소**로 작용하며,  
이용자의 **참여도와 재방문율을 높이는 핵심 기능**입니다.

## ✏️ 프로젝트 소개
![slide_6](https://github.com/user-attachments/assets/58a74599-590a-4136-b860-dbdd8dc648cb)

## 🙍‍♂️ 팀 멤버 소개
| **전여욱 (백엔드, 프론트엔드)** | **김준성 (백엔드)** | **김신성 (프론트엔드)** | **주현서 (백엔드)** |
|:-----------------------------:|:------------------:|:----------------------:|:-------------------:|
| [<img src="https://github.com/rx5460/pophub_front/assets/42200731/e99003c5-26d5-4d09-b548-aeab53c105a5" height="150" width="150"/> <br/> @JeonYeoUk](https://github.com/Jeon03) | [<img src="https://github.com/rx5460/pophub_front/assets/42200731/995e786f-9219-4b11-9944-f1e6ff1df49d" height="150" width="150"/> <br/> @S-ol9](https://github.com/S-ol9) | [<img src="https://github.com/rx5460/pophub_front/assets/42200731/2f9195ee-e54c-4261-862a-d138543a7710" height="150" width="150"/> <br/> @Promark1225](https://github.com/Promark1225) | [<img src="https://github.com/rx5460/pophub_front/assets/42200731/40ace482-4b11-484c-b133-18fdc9767225" height="150" width="150"/> <br/> @rx5460](https://github.com/rx5460) |


## 개발 환경
- **Front-end**:  <img src="https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB" height="25"/>
- **Back-end**:  <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat&logo=spring-boot&logoColor=white" height="25"/>
- **Database**: <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=mysql&logoColor=white" height="25"/> <img src="https://img.shields.io/badge/AWS%20S3-569A31?style=flat&logo=amazon-aws&logoColor=white" height="25"/><img src="https://img.shields.io/badge/Elasticsearch-005571?style=flat&logo=elasticsearch&logoColor=white" height="25"/>
- **배포**: <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white" height="25"/><img src="https://img.shields.io/badge/Amazon%20EC2-FF9900?style=flat&logo=amazon-aws&logoColor=white" height="25"/>
- **협업 툴**: <img src="https://img.shields.io/badge/Notion-000000?style=flat&logo=notion&logoColor=white" height="25"/><img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white" height="25"/><img src="https://img.shields.io/badge/Discord-5865F2?style=flat&logo=discord&logoColor=white" height="25"/>
- **디자인**: <img src="https://img.shields.io/badge/Figma-F24E1E?style=flat&logo=figma&logoColor=white" height="25"/>


## 프로젝트 

### 시스템 구성도
![slide_14](https://github.com/user-attachments/assets/ef4705d8-2909-491e-b1d0-7026d41c1bb8)

### erd
![slide_15](https://github.com/user-attachments/assets/5a3ae012-9aeb-44b6-a22c-65acc93edcf7)


## 🚀 주요 기능 (Core Features)

### 🛍️ 중고거래 기능
- 상품 등록 / 수정 / 삭제 (AWS S3 이미지 업로드, 카카오 지도 위치 설정)
- Elasticsearch 기반 **위치 + 키워드 검색**
- **자동완성** 기능 (titleSuggest + completion 타입)
- 정렬 기능: 최신순 / 조회순 / 관심순
- 분류 기능: 카테고리별, 위치 기반 분류

### 🤝 거래 방식
- 일반 거래: 직거래 / 택배 선택
- 안전거래 (Mock 기반 프로세스)
  - 아임포트 결제 → 송장 등록 → 배송 상태 전환 → 물품 수령 → 포인트 지급
  - 포인트 충전 시스템 포함

### 💬 실시간 채팅
- WebSocket + SockJS + STOMP 기반
- 실시간 채팅 + 읽음 처리 구현
- 채팅방 목록 슬라이드 UI + 안 읽은 메시지 뱃지

### 🔔 알림 시스템
- 📩 이메일 알림: JavaMailSender (송장 등록, 수령 요청 등)
- 🔔 FCM 웹 푸시 알림: 실시간 알림 수신
- 🔄 Context API로 클라이언트 알림 상태 관리

### ❤️ 마이페이지
- 내가 쓴 글 / 댓글 / 좋아요한 글 목록
- 관심상품 슬라이드 UI
- 구매내역 / 판매내역 확인

### 🧠 AI 기능
- GPT API를 통한 **상품 제목 기반 카테고리 추천**

### 🛠 기타 기능
- 소셜 로그인 (Google / Kakao / Naver)
- 이메일 인증 회원가입 (커뮤니티용)
- 게시글 좋아요, 댓글, 대댓글, 신고
- 공지사항 작성 (관리자 전용)

## 사용자별 기능
![image](https://github.com/user-attachments/assets/c427f484-474d-4e82-812a-25e3cbaee58c)

## 프로젝트 계획서 ppt

## 프로젝트 최종 발표 ppt

## 시연 영상
