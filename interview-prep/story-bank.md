# Story Bank — Master STAR+R Stories

This file accumulates your best interview stories over time. Each evaluation (Block F) adds new stories here. Instead of memorizing 100 answers, maintain 5-10 deep stories that you can bend to answer almost any behavioral question.

## How it works

1. Every time `/career-ops oferta` generates Block F (Interview Plan), new STAR+R stories get appended here
2. Before your next interview, review this file — your stories are already organized by theme
3. The "Big Three" questions can be answered with stories from this bank:
   - "Tell me about yourself" → combine 2-3 stories into a narrative
   - "Tell me about your most impactful project" → pick your highest-impact story
   - "Tell me about a conflict you resolved" → find a story with a Reflection

## Stories

### [Architecture] 프리셋 기반 멀티 SaaS 아키텍처
**Source:** Report #017 — 인크로스 — Front-end개발 4-6년
**S:** 악어디지털에서 여러 SaaS 서비스를 동시에 운영해야 했음
**T:** 신규 서비스를 빠르게 출시할 수 있는 구조 필요
**A:** 공통 컴포넌트 라이브러리 + 프리셋 기반 멀티 서비스 구조 구축
**R:** WinApp·Unify 등 신규 서비스를 기존 구조 확장만으로 빠르게 출시
**Reflection:** 공통화의 경계 설정이 핵심 — 과한 추상화는 오히려 비용. 도메인이 갈리는 지점에서 분기
**Best for questions about:** 시스템 설계, 재사용성, 확장 가능한 아키텍처, 트레이드오프 판단

### [Performance] Mingo 썸네일 응답 65% 개선
**Source:** Report #017 — 인크로스 — Front-end개발 4-6년
**S:** 그리드뷰 썸네일 동시 요청으로 로딩 지연 발생
**T:** API 응답 속도 개선
**A:** p-limit으로 동시 요청 제한 + imageCache Store 도입
**R:** API 응답 3.5s → 1.2s (65% 개선)
**Reflection:** 측정 먼저, 최적화는 그다음. 캐시 무효화 시점 설계가 캐시 도입보다 어려움
**Best for questions about:** 성능 최적화, 측정 기반 개선, 정량 성과

### [Build/Infra] Vite 4→5/7 마이그레이션
**Source:** Report #017 — 인크로스 — Front-end개발 4-6년
**S:** 레거시 빌드 환경의 느린 빌드·배포
**T:** 빌드/배포 시간 단축
**A:** Vite 단계적 업데이트 + 의존성 캐싱·메모리 튜닝, 데모 라우트 제외로 번들 최적화
**R:** 빌드 1m30s → 45s (50%↓), CI 배포 4~5분 단축
**Reflection:** 메이저 버전 점프는 한 번에 하지 않고 단계적으로 — breaking change 격리가 안전
**Best for questions about:** 빌드 최적화, 개발 인프라, 점진적 마이그레이션

### [AI Workflow] CLAUDE.md·MCP 워크플로우 팀 도입
**Source:** Report #017 — 인크로스 — Front-end개발 4-6년
**S:** 팀의 AI 도구 활용이 개인 단위로 산발적
**T:** 팀 표준 AI 협업 환경 구축
**A:** CLAUDE.md 컨벤션 문서화, GitLab MCP 셋업, MR 리뷰 자동화 스킬 도입
**R:** 코드 리뷰 프로세스 표준화 (사전조건·셀프리뷰·v-html XSS 기준)
**Reflection:** 도구 도입보다 컨벤션 합의가 먼저 — AI가 따를 규칙이 명확해야 효과
**Best for questions about:** AI 개발 도구, 팀 생산성, 프로세스 개선, 리더십

### [Migration] 레거시 마이그레이션 (Angular→Vue, yarn→pnpm)
**Source:** Report #017 — 인크로스 — Front-end개발 4-6년
**S:** 레거시 시스템 유지보수 난이도 증가
**T:** 개발 생산성 회복
**A:** Angular→Vue+TS 마이그레이션, yarn classic→pnpm 10 전환
**R:** 개발 생산성·빌드 환경 현대화
**Reflection:** 마이그레이션은 기능 동결 구간 협상이 절반 — 비즈니스와의 타이밍 합의가 중요
**Best for questions about:** 레거시 개선, 기술 의사결정, 이해관계자 협업

### [Operations] SSE 공통 래퍼 패턴 설계
**Source:** Report #017 — 인크로스 — Front-end개발 4-6년
**S:** 프로젝트 추출 기능의 실시간 진행률·중복 요청 문제
**T:** 안정적인 실시간 처리 구조 필요
**A:** 공통 SSE 래퍼 + AbortController 기반 중복 요청 제어 패턴 설계
**R:** 재사용 가능한 실시간 처리 패턴 확보
**Reflection:** 운영 이슈를 1회성 패치가 아닌 재사용 패턴으로 승격시키면 같은 류 이슈가 사라짐
**Best for questions about:** 운영 이슈 해결, 비동기 처리, 패턴 설계
