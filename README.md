# sync-board-frontend

실시간 협업 화이트보드 프론트엔드 프로젝트.

여러 사용자가 동시에 접속하여 실시간으로 드로잉을 공유할 수 있는 화이트보드 협업 서비스입니다.

단순한 그림판이 아니라, **실시간 데이터 동기화와 네트워크 효율성 문제 해결**에 초점을 맞춰 구현했습니다.

<br/><br/>

# 🚀 Tech Stack

Frontend:

- React
- react-konva
- Zustand
- Tailwind CSS

<br/>

Backend:

- NestJS,
- WebSocket Gateway
- TypeScript

<br/><br/>

## Why react-konva?

Canvas API를 직접 사용하는 대신

객체 기반 제어가 가능한 react-konva를 사용했습니다.

- 드래그
- 선택
- Resize
- Layer 관리

등을 비교적 쉽게 구현하기 위해 선택했습니다.

<br/><br/>

## 추후에 아래 내용을 추가 하고싶으면 raw Canvas API로 진행하기

raw Canvas API = 브라우저 기본 기능 그대로 사용

- 성능 최적화
- viewport 렌더링
- custom engine

<br/><br/>

# ✨ Key Features

- 실시간 드로잉 동기화 (WebSocket 기반)
- 사용자 커서 위치 공유
- 여러 명 동시 접속
- 간단한 실시간 채팅 기능
- Room 기반 협업 (URL로 참여 가능)

<br/><br/>

# ⚙️ Architecture

```
클라이언트 ↔ WebSocket 서버 ↔ 접속 사용자
```

<br/><br/>

```
프론트엔드 (React + Zustand + react-konva)
                │
                │ WebSocket
                ▼
백엔드 서버 (NestJS)
                │
                ├── WebSocket Gateway
                ├── 사용자 연결 관리
                ├── 실시간 이벤트 전송
                └── 드로잉 데이터 동기화
```

<br/><br/>

사용자의 드로잉 이벤트를 좌표 데이터로 변환하여 서버로 전송하고,

서버는 동일한 Room에 속한 사용자들에게 이를 broadcast합니다.

클라이언트는 수신한 데이터를 기반으로 Canvas에 다시 렌더링하여

모든 사용자가 동일한 화면을 유지하도록 구현했습니다.

<br/><br/>

# Challenges & Solutions

작성하기

<br/><br/>

# 🚀 Upcoming Features

- 보드 저장 및 불러오기
- Undo / Redo 기능
- 이미지 업로드 기능
- 다중 보드 생성
- 참여자 상태 표시
- 다크 모드 지원
- 모바일 환경 최적화
- PDF / 이미지 내보내기

<br/><br/>

# Environment

- Node.js 20 LTS 이상
- node 22.12.0 사용중

<br/><br/>

# Getting Started

```
npm run dev
```
