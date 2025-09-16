| **항목** | **내용** |
| --- | --- |
| 프로젝트명 | ProMate: 프로젝트를 자주 하지만 초기 세팅과 기준이 부족한 대학생 팀을 위해, 사용자의 목표·팀 구성·기간·도구 선호를 학습하고 수업·마감 등의 맥락을 반영하여, Notion 워크스페이스와 README·협업 규칙을 일관된 구조로 자동 생성하고 원클릭 Export로 배포해 주는 AI 기반 프로젝트 협업 스캐폴딩 서비스. |
| 프로젝트 키워드 | 자동화, 협업, 생산성 |
| 트랙 | 산학 |
| 프로젝트멤버 | 김서연, 지연경, 조수아 |
| 팀지도교수 | 오유란 교수님 |
| 무엇을 만들고자 하는가 | AI 기반 프로젝트 협업 플랫폼, 지능형 일정 관리 도구, 팀 맞춤형 재사용 기능 |
| 고객 | [페르소나]
이름: ooo
나이: 21
성별: 여
배경: 현재 교내 해커톤에서 5명 팀의 팀장을 맡고 있으며, 빠른 실행력은 있지만 매번 환경 세팅과 일정 관리에서 어려움을 겪음.
사용자 요구:
- **프로젝트 초기 세팅의 부담**: 해커톤은 제한 시간이 짧아(48시간~1주일) 즉시 개발에 들어가야 함. 프로젝트 협업 진행을 위해 notion, github, slack등 문서나 틀이 필요하지만 초기에 세팅하는데 시간이 많이 소요되고 의견과 템플릿이 다양해서 정형화 하는데 어려움을 겪음.
- **일정 조율의 어려움**: 팀원들이 서로 다른 수업·아르바이트 일정으로 해커톤 준비 회의 참석률이 낮음.일정이 꼬이면 발표 준비나 개발 마감이 지연됨.
- **산출물 관리와 협업 규칙 부재**: 해커톤은 발표자료, 시연영상, GitHub Repo, Notion 기록 등 산출물이 다양하게 요구됨.빠듯한 일정 속에서 문서화 작업이 소홀해지거나 규칙 없이 진행되는 경우가 많음. |
| Pain Point | **1.시간 낭비:** 제한된 프로젝트 시간내에 초반 환경 세팅(Notion, GitHub, Slack 등)에 많은 시간이 소요됨.정작 개발과 아이디어 구현에 집중할 시간이 줄어듦.
2. **협업 혼선**팀원마다 선호하는 협업 툴·템플릿이 달라 합의 과정에서 불필요한 논쟁 발생.일정이 겹쳐 회의가 제대로 진행되지 않아 **역할 분담이 모호**해지고 진행 속도가 느려짐.
3.**문서화 부족**발표자료·시연영상·Repo·기록 등 필수 산출물이 많음에도 불구하고,
시간 압박으로 인해 문서화가 소홀해지고 결과물이 **체계적으로 관리되지 않음**.
4. **팀장 부담 집중**일정 조율, 환경 세팅, 산출물 관리 책임이 대부분 팀장에게 집중되어 **업무 과중**과 **심리적 압박**이 발생. |
| 사용할 소프트웨어 패키지의 명칭과 핵심기능/용도, 사용시나리오 | 1. **Spring Boot
핵심 기능/용도**: Java 기반 백엔드 프레임워크, REST API 및 서버 애플리케이션 구축
**사용 시나리오**:프로젝트 관리용 API 서버 구현Notion·GitHub·Google Calendar·Discord API 연동 관리사용자/프로젝트 데이터 저장 및 인증 처리
2. **FastAPI (Python)
핵심 기능/용도**: 경량 웹 프레임워크, AI 모델 서버 및 데이터 처리 담당
**사용 시나리오**:LLM API(OpenAI 등) 호출로 README, 협업 규칙, 문서 초안 자동 생성일정 자동화 로직 및 데이터 전처리AI 기반 추천(스케줄, 태스크 배정) 처리
3.**JPA (Java Persistence API)핵심 기능/용도**:ORM(Object Relational Mapping) 기반 데이터 영속성 관리SQL을 직접 작성하지 않고 객체(Entity) 중심으로 DB 제어
**사용 시나리오**:팀원, 일정, 작업(Task) 등의 데이터 모델 정의 및 관리협업 규칙, 로그, 템플릿 등 프로젝트 데이터 영속화Spring Boot와 결합해 데이터 계층 자동화
4. **Notion API
핵심 기능/용도**: Notion 워크스페이스 자동 생성 및 업데이트
**사용 시나리오**:프로젝트 대시보드 자동 구축 (칸반, 캘린더, 회의록 DB)진행 상황/회고록 자동 업데이트
6. **GitHub API
핵심 기능/용도**: 저장소 관리, 협업 자동화
**사용 시나리오**:README.md 자동 업데이트Issue 및 Label 생성 자동화팀원 간 코드 협업 흐름 관리
7. **Google Calendar API
핵심 기능/용도**: 캘린더 동기화 및 일정 관리 자동화
**사용 시나리오**:마일스톤 및 마감일 캘린더 자동 등록팀원 개인 일정과 팀 프로젝트 일정 통합
8. **Slack API / Discord API
핵심 기능/용도**: 협업용 메신저 플랫폼 자동화
**사용 시나리오**:작업 완료·마감 임박 알림 전송신규 팀원 온보딩 및 역할 자동 배정주요 이벤트 발생 시 팀 채널 공지
9. **Next.js (App Router, RSC)
핵심 기능/용도:** React 기반 프론트엔드 프레임워크, SSR/SSG/ISR·RSC·Server Actions·API Routes, SEO 메타데이터**사용 시나리오:** 초기 로딩 속도 개선, OAuth 콜백 처리, 서버 액션으로 폼 제출/내보내기 마법사 구현, 프로젝트/문서 공유용 OG 태그 자동화

[프론트엔드]
**TypeScript & 코드 품질 체인(ESLint, Prettier, Husky, lint-staged, Commitlint)
핵심 기능/용도:** 정적 타입·일관된 코드 스타일·프리커밋 검증·표준 커밋 메시지**사용 시나리오:** PR 품질 게이트, 린팅/포맷 자동화, 릴리즈 노트 자동 생성 기반의 커밋 규약 유지 |
| 사용할 소프트웨어 패키지의 명칭과 URL | **Spring Boot** – https://spring.io/projects/spring-boot
**JPA (Java Persistence API)** – https://jakarta.ee/specifications/persistence/
**FastAPI** – https://fastapi.tiangolo.com/
**LangChain** – https://www.langchain.com/
**Notion API** – https://developers.notion.com/
**GitHub API** – https://docs.github.com/en/rest
**Google Calendar API** – https://developers.google.com/calendar
**Slack API** – https://api.slack.com/
**Discord API** – https://discord.com/developers/docs/intro
Next.js — https://nextjs.org
TypeScript — https://www.typescriptlang.org |
| 팀그라운드룰 | https://github.com/cse2348/2025_MatchaTonic/blob/main/GroundRule.md |
| 최종수정일 | 2025.09.16 |
