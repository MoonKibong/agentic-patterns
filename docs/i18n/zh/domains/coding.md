# 编程

Coding 是 Agentic Patterns 的种子领域，因为它具有明确的制品：repository、file、test、shell、issue、pull request、CI 和 review verdict。

## 常见压力

- 代理需要足够的 repository context，但不能被无关文件淹没。
- Tool use 可能改变本地或远程状态。
- Review 和 test 只有成为工作流的一部分才能捕获缺陷。
- 长期运行的任务需要 durable state 和可恢复的 handoff。

## 有用的模式

- [上下文包 (Context Packet)](../../../../patterns/context/context-packet.md)
- [角色契约 (Role Contract)](../../../../patterns/prompt/role-contract.md)
- [工具使用契约 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)
- [持久会话状态 (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)

## 候选模式

- Human Approval Gate。
- Guardian Gate。
- Provenance Ledger。
- Verification Ladder。
- Context Compactor。
