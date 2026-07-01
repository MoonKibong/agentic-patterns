# Agentic Patterns 빠른 시작

Agentic Patterns는 사람이 AI를 더 잘 지휘하기 위한 패턴 언어입니다.

반복되는 AI 작업에 사용할 수 있는 프롬프트, 컨텍스트 패킷, 하네스, 역할 계약,
도구 사용 규칙, 메모리 방식, 평가 루프를 수집합니다.

## 범위

이 프로젝트는 agentic coding에서 출발했지만 다음 영역도 다룹니다.

- 이미지 생성
- 글쓰기와 문학 생성
- 디자인 생성
- 비디오와 미디어
- 리서치와 분석

## 핵심 카테고리

- `prompt`: 재사용 가능한 지시문과 역할 구조
- `context`: 작업 패킷, 크리에이티브 브리프, 메모리 요약
- `harness`: plan/execute/review 및 generate/critique/refine 루프
- `orchestration`: 멀티 에이전트와 멀티 세션 조정
- `tool`: shell, browser, MCP, API, 외부 도구 사용 경계
- `memory`: 지속 가능한 상태와 재사용 지식
- `evaluation`: 패턴 적합성 검사, 루브릭, 리뷰 방식

## 시작하기

- 전체 한국어 위키: [docs/i18n/ko/README.md](ko/README.md)
- 문서 홈: [docs/README.md](../README.md)
- 카탈로그: [catalog/README.md](../../catalog/README.md)
- 패턴 템플릿: [patterns/_template.md](../../patterns/_template.md)
- 공개 전 link와 privacy boundary를 검토합니다.

## Evidence Hygiene

예시는 synthetic, sanitized, public 중 하나여야 합니다. 비공개 프롬프트, 비공개
하네스 세부사항, 고객 데이터, credentials, private URL, 내부 저장소 이름을 공개하지
마세요.
