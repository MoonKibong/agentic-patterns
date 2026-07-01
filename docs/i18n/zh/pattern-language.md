# 模式语言

本文档定义 Agentic Patterns 条目的结构与质量标准。

## 定义

Agentic pattern 是 human-AI work 中反复出现问题的命名可复用解法。

模式可以描述：

- Prompt structure。
- Context structure。
- Planning 或 execution harness。
- Review 与 verification loop。
- Agent role contract。
- MCP/tool protocol。
- Multi-agent coordination move。
- Memory 与 state-management practice。

模式不限于软件工程。Coding 因为具有明确的 test、repository、tool 和 review loop，适合作为第一个领域。但同样的结构也适用于 image generation、writing、design、video/media production、research 和 analysis。

## Pattern Metadata

每个模式应以小型 metadata block 开头：

```yaml
---
id: context-packet
name: Context Packet
category: context
status: draft
applies_to:
  - coding agents
  - planning
  - implementation
domains:
  - coding
related:
  - durable-session-state
---
```

`id` 应稳定、lowercase 且使用连字符格式。`domains` 为可选项，但建议填写。示例：`coding`、`image-generation`、`writing`、`design`、`video-media`、`research-analysis`、`general`。

## Pattern Sections

除非模式有充分理由，否则请使用以下章节。

### Intent

用一两句话描述可复用的操作。

### Also Known As

如有其他名称，在此列出。

### Problem

本模式解决的反复出现的问题。

### Context

模式适用的情境、前提条件和环境假设。

### Forces

使问题变得困难的张力与 tradeoff。

### Solution

可复用的 structure、protocol、prompt、harness 或 tool behavior。

### Agent Recognition Signals

代理应考虑使用本模式的可观察信号。

### Procedure

人类或代理可遵循的具体步骤。

### Outputs

模式应产出的制品。

### Stop Conditions

何时停止应用模式、何时升级处理、何时切换到其他模式。

### Example

简洁且贴近实际的示例。若真实工作流可能暴露私有 implementation、customer、prompt 或 orchestration 细节，则优先使用 synthetic example。

### Failure Modes

模式可能出错的已知方式。

### Evidence

观察结果、field note、test、review outcome 或其他公开支撑材料。

Evidence 必须可安全公开。使用 sanitized summary、synthetic reproduction 或 public source，不得暴露 private prompt、proprietary harness logic、customer data、private repo name、credential 或 internal transcript。

### Related Patterns

与本模式组合使用、相互替代或存在冲突的模式。

## Pattern Status

- `draft`：有潜力但尚未稳定。
- `candidate`：已成功使用多次，可供审查。
- `accepted`：经过审查，已成为目录的一部分。
- `deprecated`：保留作历史参考，不再推荐使用。

## Categories

- `prompt`：可复用的 instruction structure。
- `context`：context packet structure。
- `harness`：planning、execution、review、verification workflow。
- `orchestration`：multi-agent、multi-session coordination。
- `tool`：MCP、CLI、script、environment interaction pattern。
- `memory`：durable knowledge 与 state pattern。
- `evaluation`：判断模式是否有效的方法。

## Evidence Hygiene

模式示例应传授可复用的结构，而非披露激发该模式的私有事件。

可接受：

- 保留 forces 和 procedure 的 synthetic example。
- 移除 private identifier 的 sanitized field note。
- 来自 open source repository、paper、docs、blog、issue thread 的 public reference。
- 以"在多个本地 coding session 中观察到"等方式表述的聚合观察。

不得包含：

- private repo name、customer name、private URL、credential、log。
- 完整的 proprietary prompt、harness internal 或 MCP/tool protocol。
- 暴露未发布产品方向或内部实现细节的 transcript。

如有疑问，请将场景一般化，并保持模式的可操作性。

## 命名规则

模式名称应：

- 简短。
- 易于记忆。
- 具有可操作性。
- 足够具体，能区分该操作。

避免仅描述目标的名称，例如 `Better Coding` 或 `Good Context`。

## 机器可读性

模式文件应保持为正常 Markdown，metadata block 的存在是为了让未来的维护者能够：

- 构建索引。
- 检查缺失字段。
- 向代理推荐模式。
