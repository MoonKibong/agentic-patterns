# 코딩

Coding은 Agentic Patterns의 seed domain입니다. Repository, file, test, shell, issue, pull
request, CI, review verdict 같은 아티팩트가 명확하기 때문입니다.

## 공통 압력

- 에이전트는 충분한 repository context가 필요하지만 irrelevant file에 묻히면 안 됩니다.
- Tool use는 local 또는 remote state를 바꿀 수 있습니다.
- Review와 test는 workflow 일부가 될 때만 defect를 잡습니다.
- Long-running task는 durable state와 resumable handoff가 필요합니다.

## 유용한 패턴

- [컨텍스트 패킷 (Context Packet)](../../../../patterns/context/context-packet.md)
- [역할 계약 (Role Contract)](../../../../patterns/prompt/role-contract.md)
- [도구 사용 계약 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)
- [지속 세션 상태 (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)

## 후보 패턴

- Human Approval Gate.
- Guardian Gate.
- Provenance Ledger.
- Verification Ladder.
- Context Compactor.
