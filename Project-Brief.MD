| **항목** | **내용** |
| --- | --- |
| **프로젝트명** | **ProMate**: 프로젝트를 자주 하지만 초기 세팅과 기준이 부족한 대학생 팀을 위해, 사용자의 목표·팀 구성·기간·도구 선호를 학습하고 수업·마감 등의 맥락을 반영하여, Notion 워크스페이스와 README·협업 규칙을 일관된 구조로 자동 생성하고 원클릭 Export로 배포해 주는 AI 기반 프로젝트 협업 스캐폴딩 서비스 |
| **프로젝트 키워드** | 자동화, 협업, 생산성 |
| **트랙** | 산학 |
| **프로젝트 멤버** | 김서연, 지연경, 조수아 |
| **팀 지도교수** | 오유란 교수님 |
| **무엇을 만들고자 하는가** | - AI 기반 프로젝트 협업 플랫폼<br>- 지능형 일정 관리 도구<br>- 팀 맞춤형 재사용 기능 |
| **고객** | [페르소나]<br>이름: ooo<br>나이: 21<br>성별: 여<br>배경: 교내 해커톤에서 5명 팀의 팀장을 맡고 있으며, 빠른 실행력은 있지만 매번 환경 세팅과 일정 관리에서 어려움을 겪음.<br><br>**사용자 요구**<br>- 프로젝트 초기 세팅의 부담: 해커톤은 제한 시간이 짧아 즉시 개발에 들어가야 하나, Notion·GitHub·Slack 등 세팅이 오래 걸림.<br>- 일정 조율의 어려움: 팀원 일정이 달라 회의 참석률 저조 → 마감 지연 발생.<br>- 산출물 관리와 협업 규칙 부재: 발표자료·시연영상·Repo·기록 등 문서화 부족, 규칙 없는 진행.<br> |
| **Pain Point** | 1. **시간 낭비**: 초기 세팅에 많은 시간이 소요 → 개발/아이디어 집중 시간 부족<br>2. **협업 혼선**: 협업 툴/템플릿 선호가 달라 합의 과정에서 충돌, 역할 분담 불명확<br>3. **문서화 부족**: 발표자료·시연영상·Repo·기록 관리 부족<br>4. **팀장 부담 집중**: 일정·세팅·산출물 관리가 팀장에 집중 → 과중/심리적 압박 |
| **사용할 소프트웨어 패키지의 명칭과 핵심기능/용도, 사용시나리오** | 1. **Spring Boot**<br>핵심 기능/용도: Java 기반 백엔드 프레임워크, REST API 및 서버 구축<br>사용 시나리오: API 서버 구현, Notion·GitHub·Google Calendar·Discord API 연동, 사용자/프로젝트 데이터 관리<br><br>2. **FastAPI (Python)**<br>핵심 기능/용도: 경량 웹 프레임워크, AI 모델 서버<br>사용 시나리오: LLM 호출, 일정 자동화 로직, AI 추천 처리<br><br>3. **JPA (Java Persistence API)**<br>핵심 기능/용도: ORM 기반 데이터 영속성 관리<br>사용 시나리오: 팀원, 일정, 작업 데이터 모델 정의 및 영속화, Spring Boot와 결합<br><br>4. **Notion API**<br>핵심 기능/용도: 워크스페이스 자동 생성/업데이트<br>사용 시나리오: 대시보드 구축, 회의록/진행 상황 업데이트<br><br>5. **GitHub API**<br>핵심 기능/용도: 저장소 관리/협업 자동화<br>사용 시나리오: README 업데이트, Issue/Label 자동 생성<br><br>6. **Google Calendar API**<br>핵심 기능/용도: 일정 동기화/자동화<br>사용 시나리오: 마일스톤/마감일 등록, 개인/팀 일정 통합<br><br>7. **Slack API / Discord API**<br>핵심 기능/용도: 협업 메신저 자동화<br>사용 시나리오: 알림 전송, 온보딩 자동화, 이벤트 공지<br><br>8. **Next.js (App Router, RSC)**<br>핵심 기능/용도: React 기반 프론트엔드, SSR/SSG/RSC 지원<br>사용 시나리오: 초기 로딩 최적화, OAuth 콜백 처리, 서버 액션 기반 제출/마법사 구현, OG 태그 자동화<br><br>9. **TypeScript & 코드 품질 체인 (ESLint, Prettier, Husky, lint-staged, Commitlint)**<br>핵심 기능/용도: 정적 타입, 코드 스타일 통일, 프리커밋 검증<br>사용 시나리오: PR 품질 관리, 린팅/포맷 자동화, 릴리즈 노트 자동 생성 |
| **사용할 소프트웨어 패키지의 명칭과 URL** | - [Spring Boot](https://spring.io/projects/spring-boot)<br>- [JPA](https://jakarta.ee/specifications/persistence/)<br>- [FastAPI](https://fastapi.tiangolo.com/)<br>- [Notion API](https://developers.notion.com/)<br>- [GitHub API](https://docs.github.com/en/rest)<br>- [Google Calendar API](https://developers.google.com/calendar)<br>- [Slack API](https://api.slack.com/)<br>- [Discord API](https://discord.com/developers/docs/intro)<br>- [Next.js](https://nextjs.org)<br>- [TypeScript](https://www.typescriptlang.org) |
| **팀 그라운드룰** | [GroundRule.md](https://github.com/cse2348/2025_MatchaTonic/blob/main/GroundRule.md) |
| **최종 수정일** | 2025.09.16 |
