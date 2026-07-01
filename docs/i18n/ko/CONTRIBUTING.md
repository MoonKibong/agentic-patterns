# 기여하기

Agentic Patterns는 반복 가능한 실천을 함께 쌓아 가는 패턴 카탈로그입니다. 기여는
사람과 AI가 반복되는 작업을 더 쉽게 알아보고, 논의하고, 실행할 수 있게 만들어야
합니다.

## 기여 방법

- [patterns/_template.md](../../../patterns/_template.md)를 사용해 새 패턴을 추가합니다.
- 기존 패턴의 예시, 적용 조건, 실패 모드를 개선합니다.
- 실제 agentic coding 세션에서 얻은 field note를 추가합니다.
- 에이전트가 패턴을 검증, 색인, 추천, 패키징할 수 있는 도구를 만듭니다.
- 더 나은 카탈로그 분류 체계를 제안합니다.

## 패턴을 추가하기 전에

그 항목이 정말 패턴인지 먼저 확인합니다.

- 반복되는 문제를 해결하는가?
- 다른 사람이 비슷한 상황에서 적용할 수 있는가?
- tradeoff가 드러나는가?
- 에이전트가 언제 사용할지 알아볼 수 있는가?
- 최소한의 증거 또는 구체적인 경험이 있는가?

답이 아직 명확하지 않다면 확립된 패턴으로 쓰기보다 field note나 draft pattern으로
기록합니다.

## Field Notes

관찰은 유용하지만 아직 패턴이라고 부르기 이르다면
[field-notes/_template.md](../../../field-notes/_template.md)를 사용합니다.

좋은 field note는 다음을 기록합니다.

- 작업의 형태.
- 에이전트 설정.
- 실제로 일어난 일.
- 개선되거나 실패한 지점.
- 생겨날 수 있는 패턴.
- 패턴을 더 강하게 만들 증거.

## Evidence Hygiene

독점 솔루션의 세부 내용을 기여하지 않습니다. 패턴 증거는 다음 중 하나여야 합니다.

- 문제 구조만 보존한 synthetic example.
- 비공개 세부 정보를 제거한 sanitized field note.
- 공개 저장소, 논문, 블로그 글, issue thread에서 온 공개 사례.
- 비공개 식별자를 제거한 일반화된 관찰.

고객 데이터, credential, private URL, private repo name, 내부 prompt text, 완전한 독점
workflow transcript를 포함하지 않습니다.

## 패턴 작성 절차

1. `patterns/_template.md`를 적절한 category directory로 복사합니다.
2. metadata block을 채웁니다.
3. 패턴을 operational term으로 작성합니다.
4. 최소 하나의 예시를 포함합니다.
5. 알려진 failure mode와 counter-indication을 포함합니다.
6. 관련 패턴을 연결합니다.
7. [catalog/README.md](../../../catalog/README.md)를 갱신합니다.

## 지역화 문서

docs/i18n/의 localized quick start와 wiki mirror는 공개 진입점입니다.
프로젝트 설명, 핵심 category, safety/privacy language, contribution workflow가 바뀌면
지역화 문서도 함께 갱신하거나, pull request에서 번역 갱신이 필요 없는 이유를
명시합니다.

자신 있게 갱신할 수 없는 언어라면 English source change를 작게 유지하고 translation
review를 요청합니다.

## Evidence Standard

초기의 증거는 가벼울 수 있지만 정직해야 합니다.

유용한 증거에는 다음이 포함됩니다.

- 여러 작업에서 반복 관찰된 workflow.
- before/after comparison.
- transcript excerpt 또는 요약된 incident.
- test result, review result, 피한 defect.
- 반복 사용을 견뎌 낸 local convention.

무엇이 개선되었는지 설명하지 않는 "works better" 같은 모호한 주장은 피합니다.

## 문체

유능한 사람과 유능한 에이전트를 대상으로 직접적이고 구체적으로 씁니다. 불확실성에는
겸손해야 합니다.

이 프로젝트는 inspirational prompt trick 목록이 아니라 실용적인 pattern language가
되어야 합니다.
