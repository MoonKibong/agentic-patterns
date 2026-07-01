# Agentic Patterns 维基

Agentic Patterns 简体中文维基入口。

从问题出发，依次进入分类、领域、具体模式，逐步深入。
英文文档是最终权威，本文档是当前公开文档的简体中文镜像。

## 从这里开始

- [项目概述](project-brief.md): 项目的目的与背景。
- [模式语言的根源](foundations/pattern-language-roots.md): Christopher Alexander、GoF，以及 agentic patterns 的动机。
- [模式语言](pattern-language.md): 模式文档的结构与质量标准。
- [证据卫生](evidence-hygiene.md): 如何在不泄露私有解决方案的前提下撰写示例。
- [Agentic Work 趋势](research/2026-agentic-work-trends.md): 为何这不仅限于编程。
- [目录](../../../catalog/README.md): 当前模式列表。
- [路线图](roadmap.md): 项目的未来方向。
- [贡献指南](CONTRIBUTING.md): 如何添加模式和字段笔记。
- [本地化快速开始](../README.md): 面向初次读者的简短翻译。
- [开源准备](oss/OPEN_SOURCE_READINESS.md): 公开发布检查清单。

## 按目标浏览

| 目标 | 起始文档 |
| --- | --- |
| 理解项目 | [项目概述](project-brief.md) |
| 理解知识背景 | [模式语言的根源](foundations/pattern-language-roots.md) |
| 查找可复用模式 | [目录](../../../catalog/README.md) |
| 为代理提供更好的上下文 | [上下文包 (Context Packet)](../../../patterns/context/context-packet.md) |
| 定义代理角色 | [角色契约 (Role Contract)](../../../patterns/prompt/role-contract.md) |
| 协调长期代理工作 | [持久会话状态 (Durable Session State)](../../../patterns/orchestration/durable-session-state.md) |
| 限制 shell、MCP 或浏览器的使用范围 | [工具使用契约 (Tool-Use Contract)](../../../patterns/tool/tool-use-contract.md) |
| 指导图像、写作或设计生成 | [创意简报包 (Creative Brief Packet)](../../../patterns/context/creative-brief-packet.md) |
| 迭代优化生成候选 | [生成-批评-优化 (Generate-Critique-Refine)](../../../patterns/harness/generate-critique-refine.md) |
| 记录观察 | [字段笔记模板](../../../field-notes/_template.md) |

## 按分类浏览

- [提示模式](categories/prompt.md)
- [上下文模式](categories/context.md)
- [工作流模式](categories/harness.md)
- [工具模式](categories/tool.md)
- [记忆模式](categories/memory.md)
- [评估模式](categories/evaluation.md)

## 按领域浏览

- [编程](domains/coding.md)
- [图像生成](domains/image-generation.md)
- [写作与文学创作](domains/writing.md)
- [设计生成](domains/design.md)
- [视频与媒体](domains/video-media.md)
- [研究与分析](domains/research-analysis.md)

## 代理使用须知

- 修改仓库前请阅读仓库根目录的 `AGENTS.md`。
- 遵守公开/私有边界，不得将私有模式名称或本地工具名称添加到公开文档。
- 修改模式文件后运行仓库验证流程。

## 贡献者须知

- 从[贡献指南](CONTRIBUTING.md)开始。
- 新模式请使用[模式模板](../../../patterns/_template.md)。
- 早期观察请使用[字段笔记模板](../../../field-notes/_template.md)。
- 公开发布前请确认[许可协议](licensing.md)。
- 添加示例或字段笔记前请阅读[证据卫生](evidence-hygiene.md)。
- 更改面向用户的文档时请查看[本地化快速开始](../README.md)。

## 侧边栏

简体中文侧边栏位于 [_sidebar.md](_sidebar.md)。
