# 工具模式

Tool pattern 定义代理如何使用 shell command、browser、MCP server、API、package manager、Git 等可能影响真实状态的能力。

当代理必须通过外部能力行动，且需要明确限定影响范围时，请使用工具模式。

## 当前模式

- [工具使用契约 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)：定义 allowed tool、approval trigger、forbidden action 和 evidence expectation。

## 模式构想

- Read-First Tooling。
- Approval Boundary。
- Verification Command。
- External State Guard。

## 相关分类

- [工作流模式](harness.md)
- [提示模式](prompt.md)
- [评估模式](evaluation.md)
