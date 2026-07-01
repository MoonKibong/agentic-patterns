# Evidence Hygiene

Agentic Patterns는 proprietary solution detail을 노출하지 않고도 유용해야 합니다.

카탈로그는 실제 경험을 기반으로 할 수 있지만, private prompt, harness, repo, customer,
credential, transcript, internal workflow mechanic은 보호해야 합니다.

## 원칙

패턴은 공개하고, private incident는 공개하지 않습니다.

예시는 다음 재사용 구조를 보여주어야 합니다.

- 문제 형태.
- Forces와 tradeoff.
- Procedure.
- Expected output.
- Failure mode.
- Verification style.

예시는 private implementation detail을 보여주면 안 됩니다.

## 안전한 Evidence 유형

- 워크플로 구조를 보존한 synthetic example.
- private identifier를 제거한 sanitized field note.
- open source repository, paper, docs, blog, issue thread 등 public example.
- 식별 정보를 제거한 aggregate observation.

## 공개하지 말 것

- Customer data.
- Credential, token, private URL.
- Private repository name.
- 공개 의도가 없는 internal prompt text.
- Complete proprietary harness logic.
- Private project의 full workflow transcript.
- Product direction, business strategy, unreleased implementation detail.

## Field Note Sanitization

1. 프로젝트 이름을 `web app`, `API service`, `agent runner` 같은 일반 이름으로 바꿉니다.
2. 파일 경로를 `src/billing/service.ts` 같은 대표 경로로 바꿉니다.
3. Credential, hostname, private issue number, private branch name을 제거합니다.
4. Transcript는 직접 인용하지 말고 요약합니다.
5. 패턴과 관련된 success/failure condition은 유지합니다.
6. 예시가 synthetic 또는 sanitized임을 명시합니다.

## Synthetic Example Policy

Synthetic example은 권장됩니다. 실제 private workflow와 일치할 필요는 없지만, 실행 가능한
정도로 구체적이어야 합니다.

좋은 synthetic example:

- 구체적인 file, role, command를 포함합니다.
- 패턴의 forces를 드러냅니다.
- 에이전트가 어떤 output을 내야 하는지 보여줍니다.
- project-specific secret을 피합니다.

나쁜 synthetic example은 "make the code better"처럼 너무 모호합니다.
