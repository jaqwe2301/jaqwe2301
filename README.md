<div align="center">

# 김민혁 | Frontend Developer

React와 TypeScript를 기반으로  
**사용자 흐름과 서버 상태를 안정적으로 연결하는 프론트엔드 개발자**입니다.

더 나은 구조가 보이면 내가 만든 코드도 고집하지 않고 다시 설계하며,  
기능 구현뿐 아니라 **유지보수 범위와 서비스 운영까지 함께 고민합니다.**

<br />

[![Blog](https://img.shields.io/badge/Blog-mini--frontend.tistory.com-555555?style=flat-square&logo=tistory&logoColor=white)](https://mini-frontend.tistory.com/)
[![GitHub](https://img.shields.io/badge/GitHub-jaqwe2301-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/jaqwe2301)
[![Email](https://img.shields.io/badge/Email-jaqwe2301%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:jaqwe2301@gmail.com)

</div>

---

## About Me

- React · TypeScript 기반 웹 프론트엔드를 개발합니다.
- B2B2C SaaS 서비스의 초기 개발부터 상용화까지 프론트엔드를 단독으로 담당한 경험이 있습니다.
- 인증, 비동기 상태, 실시간 통신처럼 여러 화면과 서버 상태가 맞물리는 문제를 구조화하는 데 관심이 있습니다.
- 필요하다면 기존 구현을 다시 검토하고, 유지보수하기 좋은 구조로 전환합니다.

---

## Career

### B2B2C SaaS Frontend Developer
**2024.05 ~ 2025.08 · 프론트엔드 단독 개발**

`TypeScript` `Next.js` `React` `TanStack Query` `Redux` `Tiptap` `Tailwind CSS`

- iOS Safari · 카카오톡 인앱 브라우저에서 발생한 NICE 본인인증 500 오류를 추적하고, **Next.js Route Handler에서 GET · POST 콜백을 모두 처리하도록 구조를 변경**
- DOM을 직접 제어하던 자체 에디터의 예외 처리와 동기화 한계를 확인하고, **Tiptap 기반 문서 모델 + 커스텀 Extension 7개 구조로 전환**
- 한 화면의 여러 AI 요청이 하나의 로딩 상태를 공유하던 문제를 **항목 단위 비동기 상태로 분리**해 병렬 요청과 논블로킹 UI 구현
- Kakao Maps에서 실제 위치와 탐색 위치의 상태를 분리하고, 줌 레벨 · 디바이스 크기에 따른 마커 크기 조정 등 지도 탐색 경험 개선

---

## Featured Projects

### YAMOYO

> 팀 프로젝트 시작에 필요한 결정을 투표와 게임으로 빠르게 끝내는 팀 초기 세팅 서비스

**2025.12 ~ 2026.05 · SWYP 웹 12기 최종 1위(대상)**

`React 19` `TypeScript` `Vite` `Zustand` `TanStack Query` `WebSocket (STOMP)` `Tailwind CSS` `Firebase FCM`

- **fetch 기반 API 클라이언트**를 구성해 인증 · 에러 · 응답 파싱을 공통 계층에서 처리
- API · WebSocket 계층은 인증 예외를 신호로만 발행하고, **AuthGuard가 라우팅을 전담하는 이벤트 기반 인증 흐름**으로 역할 분리
- 여러 인증 예외가 동시에 발생할 때 우선순위를 비교해 **토큰 갱신과 화면 이동이 중복 실행되지 않도록 제어**
- STOMP + SockJS 기반 실시간 통신에서 연결과 구독을 공통 부모로 이동하고 연결 관리 객체를 재사용해, **페이지 전환 · 재렌더링 시 발생하던 연결 끊김과 중복 구독 문제 해결**
- FCM 메시지를 서버 상태 변경 신호로 사용해 **TanStack Query 캐시를 갱신하고 팀룸 화면을 최신 상태로 동기화**
- SSR · SEO 이점이 제한적인 서비스 특성과 개발 일정을 고려해 **Next.js에서 Vite 기반 React로 전환**, 빌드 시간을 약 1분에서 20초 후반대로 단축
- ESLint · Prettier · Husky · lint-staged를 팀 컨벤션으로 구성해 커밋 단계에서 코드 스타일 자동 검사

**FE 2 · BE 3 · DE 3 · PM 1**  
개인 커밋 **381 / 전체 591** · 머지 PR **39 / 전체 71**

[Repository](https://github.com/yamoyo/yamoyo_FE) · [Service](https://yamoyo.kr) · [Development Blog](https://mini-frontend.tistory.com/)

<br />

### 행운행 · 진행 중

> 버스 정류장을 방문하며 클로버를 수집하는 위치 기반 모바일 웹 서비스

`Next.js` `TypeScript` `MapLibre GL` `TanStack Query` `Zustand` `Jest` `React Testing Library`

- MapLibre GL과 OpenStreetMap을 활용한 모바일 지도 화면 구현
- 위치 권한 허용 · 거부 상황을 고려한 사용자 위치 및 fallback 흐름 설계
- 전국 버스 정류장 데이터를 프론트엔드에서 활용할 수 있도록 분할 · 가공
- 사용자 좌표를 기준으로 **가까운 버스 정류장을 탐색하는 로직과 테스트 코드 작성**
- Jest · React Testing Library를 활용해 위치 · 거리 계산 등 핵심 도메인 로직 검증
- GitHub Actions 기반 CI와 PR 중심 개발 환경 구성

[Repository](https://github.com/Haeng-Un-Haeng/haengunhaeng-frontend)


<br />

### 모던 리액트 Deep Dive · 스터디

> 『모던 리액트 Deep Dive』를 기반으로 React와 Next.js의 동작 원리를 학습하고 정리한 스터디

**2026.05 ~ 2026.06 · 7주**

`JavaScript` `React` `Next.js` `SSR` `State Management` `Web Vitals`

- JavaScript 동등 비교부터 React 렌더링, Hooks, SSR, 상태 관리, Next.js, 코드 품질과 웹 성능 지표까지 **7주 동안 매주 학습 내용을 Markdown으로 정리하고 PR로 공유**
- `React.memo`, `useLayoutEffect`와 브라우저 paint 과정처럼 책에서 간단히 다룬 주제를 추가로 조사해 보완
- Pages Router와 App Router의 차이, React Server Component와 SSR의 차이 등 **현재 사용하는 Next.js 기준으로 내용을 다시 비교 · 정리**
- 상태 관리 라이브러리의 `subscribe` 구조를 YAMOYO에서 구현한 Event Bus와 비교하는 등, **학습한 개념을 실제 프로젝트 코드와 연결해 이해**

[Repository](https://github.com/DeepDive-FE/DeepDive-React)

<br />

### DORO EDU

> 교육 기관과 대학생 전문 강사를 연결하고, 강의 신청 · 배정 · 관리를 지원하는 모바일 애플리케이션

`React Native` `JavaScript` `Expo` `Firebase` `React Navigation` `Notifee`

- 2인 프론트엔드 팀으로 React Native · Expo 기반 모바일 애플리케이션 개발
- JWT 기반 로그인 세션을 구성하고 사용자 유형에 따라 **일반 강사 · 관리자 기능과 API 흐름을 분리**
- Firebase Messaging과 Notifee를 활용해 **백그라운드뿐 아니라 앱 실행 중에도 알림을 확인할 수 있는 푸시 알림 흐름 구현**
- 로그아웃 직후 토큰이 제거된 상태에서 Home 화면 API가 호출되며 발생하던 오류를 추적해, **불필요한 Navigation 이동 · 스택 초기화 로직을 제거하여 해결**
- 알림 조작 기능, 비밀번호 찾기 오류 수정, 관리자 마이페이지 등 서비스 운영에 필요한 기능 개선

[Repository](https://github.com/DOROEDU/Doro-Front)

---

## Tech Stack

### Main

<p>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/React-149ECA?style=flat-square&logo=react&logoColor=white" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/TanStack%20Query-FF4154?style=flat-square&logo=reactquery&logoColor=white" />
  <img src="https://img.shields.io/badge/Zustand-443E38?style=flat-square&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" />
</p>

### Experience

<p>
  <img src="https://img.shields.io/badge/Redux-764ABC?style=flat-square&logo=redux&logoColor=white" />
  <img src="https://img.shields.io/badge/React%20Native-20232A?style=flat-square&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/Tiptap-0D0D0D?style=flat-square&logoColor=white" />
  <img src="https://img.shields.io/badge/STOMP%20%2F%20WebSocket-010101?style=flat-square&logo=socketdotio&logoColor=white" />
  <img src="https://img.shields.io/badge/MapLibre%20GL-396CB2?style=flat-square&logo=maplibre&logoColor=white" />
  <img src="https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white" />
  <img src="https://img.shields.io/badge/Storybook-FF4785?style=flat-square&logo=storybook&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white" />
</p>

---

<div align="center">

문제를 해결한 과정과 기술 선택의 이유를 기록합니다.

[Blog](https://mini-frontend.tistory.com/) · [GitHub](https://github.com/jaqwe2301)

</div>
