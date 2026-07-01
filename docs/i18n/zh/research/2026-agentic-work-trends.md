# 2026 Agentic Work 趋势

本笔记汇总了 agentic coding 及相邻 creative workflow 的近期公开信号。以 Gemini 的研究输出作为素材来源，但仅在内容安全、有价值且来自公开可验证来源或明确标注为研究线索时，才记录于此。

## 执行摘要

Agentic coding 正在成为 human-guided AI work 中最具体的早期模式库：repository、shell、test、code review、sandbox 和 pull request 使 context 和 verification 清晰可见。同样的基础原语也出现在 image generation、writing、design、video/media 和 research workflow 中：

- bounded context packet 和 brief
- role-specific agent 或 subagent
- tool-use protocol
- generate-critique-refine loop
- plan-execute-verify-review loop
- durable state 和 handoff artifact
- provenance 和 citation tracking
- human approval gate
- safety 和 governance wrapper

目录因此应围绕可复用的基础原语组织，而领域页面则展示这些原语如何应用于 coding、image generation、writing、design、video/media 和 research。

## 已验证来源

| 来源 | 日期 | 相关性 |
| --- | --- | --- |
| [OpenAI, Introducing Codex](https://openai.com/index/introducing-codex/) | 2025 | Sandboxed 软件任务委派、repo context、test execution、PR 风格工作流。 |
| [OpenAI Agents SDK Docs](https://openai.github.io/openai-agents-python/) | 2025-2026 | Agents、handoffs、guardrails、tracing、tools。 |
| [Anthropic Claude Code Subagents](https://docs.anthropic.com/en/docs/claude-code/sub-agents) | 2025-2026 | 任务专用 subagent、独立 context window、自定义 prompt、tool permission。 |
| [Anthropic Claude Code Hooks](https://docs.anthropic.com/en/docs/claude-code/hooks) | 2025-2026 | 代理行为的确定性控制点。 |
| [Model Context Protocol Introduction](https://modelcontextprotocol.io/introduction) | 2025-2026 | 通过标准协议向语言模型暴露 tool 和 context。 |
| [Google A2A Protocol](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) | 2025 | Agent 间互操作与委派。 |
| [arXiv: The 2025 AI Agent Index](https://arxiv.org/abs/2602.17753) | 2026 | Agent 系统与评估/部署模式调研。 |
| [arXiv: VideoAgent](https://arxiv.org/abs/2606.23327) | 2026 | 视频编辑工作流的 agentic 分解。 |
| [HKUDS ViMax](https://github.com/HKUDS/ViMax) | 2026 | 基于文本/故事输入的 agentic 视频生成研究线索。 |

## 趋势：Context Engineering 成为产品层面

Agentic 系统越来越多地将 context 视为结构化输入，而非聊天历史。Coding agent 使用 repository file、instruction、issue text、test 和 environment state。Creative 系统则需要等效的 brief：reference、style constraint、continuity anchor、audience、deliverable 和 evaluation criteria。

目录影响：

- 将 [上下文包 (Context Packet)](../../../../patterns/context/context-packet.md) 作为通用模式保留。
- 为 creative domain 添加 [创意简报包 (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md)。
- 考虑未来的 `Reference Board`、`Source Ledger` 和 `Context Compactor` 模式。

## 趋势：代理被包裹在 Harness 中

重要的转变不仅仅是模型变得更强。有用的系统将模型包裹在 planning、execution、critique、verification、guardrail、tracing 和 approval gate 中。在 coding 中体现为 plan-execute-test-review，在 creative work 中体现为 brief-generate-critique-refine-select。

目录影响：

- 为软件和其他可验证工作保留显式的 review 和 verification loop。
- 为 creative 和探索性工作添加 [生成-批评-优化 (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md)。
- 未来模式：`Rubric Review`、`Human Approval Gate`、`Guardian Gate`。

## 趋势：Tool Protocol 和 Agent 互操作性日益重要

MCP 和 agent-to-agent protocol 表明，agentic workflow 越来越依赖明确的能力边界。Tool 和外部系统必须可被发现、有界、可审计且安全。

目录影响：

- 保留 [工具使用契约 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)。
- 未来模式：`Capability Manifest`、`Approval Boundary`、`Sandbox Gate`。

## 趋势：Creative Work 需要制品生命周期模式

Image、writing、design 和 video workflow 会生成中间制品：brief、reference、outline、style board、candidate image、storyboard、scene plan、critique table 和 final asset。这些制品需要 handoff、provenance、versioning 和 human approval。

目录影响：

- 优先添加领域页面，而非过早拆分核心目录。
- 未来模式：`Artifact Handoff`、`Provenance Ledger`、`Variation Ladder`、`Style Lock`、`Continuity Ledger`。

## 来源卫生

Gemini 的研究输出包含有用的线索，但本仓库不应默认将生成的引用视为已验证。对于公开文档：

- 优先使用 primary source 和官方文档。
- 未验证的条目标注为 lead。
- 不引用私有工作流。
- 若公开 evidence 可能暴露专有方法，则使用 synthetic example。
