# 도구 패턴

Tool pattern은 agent가 shell command, browser, MCP server, API, package manager, Git 등 실제
state에 영향을 줄 수 있는 capability를 사용하는 방법을 정의합니다.

에이전트가 외부 capability를 사용해야 하고 blast radius를 명확히 해야 할 때 사용합니다.

## 현재 패턴

- [도구 사용 계약 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md): allowed tool, approval trigger,
  forbidden action, evidence expectation을 정의합니다.

## 패턴 아이디어

- Read-First Tooling.
- Approval Boundary.
- Verification Command.
- External State Guard.

## 관련 카테고리

- [하네스 패턴](harness.md)
- [프롬프트 패턴](prompt.md)
- [평가 패턴](evaluation.md)
