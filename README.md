# 🎨 Sync Board (Frontend)

실시간 협업 화이트보드 프론트엔드 프로젝트이다.

여러 사용자가 동시에 접속하여 드로잉, 커서 이동, 채팅 등을 실시간으로 공유할 수 있는 협업 서비스이다.

단순한 그림판이 아니라 **실시간 데이터 동기화와 네트워크 구조 설계**에 초점을 맞춰 구현했다.

<br/><br/>

# 🚀 Tech Stack

## Frontend

- React
- TypeScript
- react-konva
- Zustand
- Tailwind CSS

## Backend

- NestJS
- WebSocket Gateway
- TypeScript

<br/><br/>

# ✨ Key Features

- 실시간 드로잉 동기화 (WebSocket 기반)
- 사용자 커서 위치 공유
- 여러 사용자 동시 접속
- Room 기반 협업 구조
- 실시간 채팅 기능
- 캔버스 객체 선택 / 이동 / 수정

<br/><br/>

# 🏗️ Architecture

```txt
클라이언트 ↔ WebSocket 서버 ↔ 접속 사용자
```

```txt
프론트엔드 (React + Zustand + react-konva)
                │
                │ WebSocket
                ▼
백엔드 서버 (NestJS)
                │
                ├── WebSocket Gateway
                ├── 사용자 연결 관리
                ├── 실시간 이벤트 브로드캐스트
                └── 드로잉 데이터 동기화
```

<br/><br/>

# 🔄 Data Flow

사용자의 드로잉 이벤트를 좌표 데이터로 변환하여 서버로 전송한다.

서버는 동일한 Room에 속한 사용자들에게 이벤트를 broadcast한다.

클라이언트는 수신된 데이터를 기반으로 Canvas를 다시 렌더링하여  
모든 사용자가 동일한 화면을 유지하도록 구현했다.

<br/><br/>

# 🧠 Challenges & Solutions

작성하기

<br/><br/>

# 🚀 Upcoming Features

- 보드 저장 및 불러오기
- Undo / Redo 기능
- 이미지 업로드 기능
- 다중 보드 생성
- 참여자 상태 표시
- 다크 모드 지원
- 모바일 최적화
- PDF / 이미지 export

<br/><br/>

# ⚙️ Environment

- Node.js 20 LTS 이상
- Node.js 22.12.0 버전 사용

<br/><br/>

# ▶️ Getting Started

## 1. Install dependencies

```bash
npm install
```

<br/><br/>

## 2. Run project

```bash
npm run dev
```

<br/><br/>

# 📦 Backend Repository

```txt
sync-board-backend
```

<br/><br/>

# 🎥 Demo

추후 GIF / 영상 추가 예정
