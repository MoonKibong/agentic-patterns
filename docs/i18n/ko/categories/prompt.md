# 프롬프트 패턴

Prompt pattern은 role, task, constraint, expected output을 위한 재사용 instruction
structure를 정의합니다.

주요 문제가 code나 tool 부족이 아니라 에이전트 행동의 모호함일 때 사용합니다. 즉, 무엇을
최적화할지, 무엇을 결정할 수 있는지, 무엇을 반환해야 하는지 명확히 합니다.

## 현재 패턴

- [역할 계약 (Role Contract)](../../../../patterns/prompt/role-contract.md): agent role, authority, responsibility,
  boundary, output, escalation rule을 정의합니다.

## 패턴 아이디어

- Reviewer Gate.
- Output Contract.
- Assumption Ledger.
- Decision Escalation.

## 관련 카테고리

- [컨텍스트 패턴](context.md)
- [하네스 패턴](harness.md)
- [평가 패턴](evaluation.md)
