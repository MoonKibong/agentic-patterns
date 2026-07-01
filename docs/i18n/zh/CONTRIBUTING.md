# 贡献指南

Agentic Patterns 旨在成为可复用实践的共享目录。贡献应让人类与 AI 的重复性工作更易于识别、讨论和执行。

## 贡献方式

- 使用 [patterns/_template.md](../../../patterns/_template.md) 添加新模式。
- 改进现有模式的示例、适用条件或失败模式。
- 添加来自真实 agentic coding session 的 field note。
- 构建能够验证、索引、推荐或打包模式供代理使用的工具。
- 提出更好的目录分类方案。

## 添加模式前

确认该条目是否真的是一个模式：

- 它是否解决了反复出现的问题？
- 其他人能否在类似情境中应用它？
- Tradeoff 是否清晰可见？
- 代理能否识别何时使用它？
- 背后是否有最低限度的 evidence 或具体经验？

如果答案尚不明确，请以 field note 或 draft pattern 的形式记录，而非作为已确立的模式呈现。

## Field Notes

若观察有价值但尚未稳定到可称为模式，请使用 [field-notes/_template.md](../../../field-notes/_template.md)。

好的 field note 应记录：

- 任务形态。
- 代理设置。
- 实际发生的事情。
- 改进或失败的地方。
- 可能正在形成的模式。
- 能让模式更有力的 evidence。

## Evidence Hygiene

不得贡献专有解决方案细节。模式 evidence 必须是以下之一：

- 仅保留问题结构的 synthetic example。
- 移除私有细节的 sanitized field note。
- 来自公开仓库、论文、博客文章或 issue thread 的公开案例。
- 不含私有标识符的一般化观察。

不得包含客户数据、credential、private URL、private repo name、内部 prompt text 或完整的专有 workflow transcript。

## 模式撰写流程

1. 将 `patterns/_template.md` 复制到对应的 category 目录。
2. 填写 metadata block。
3. 以 operational term 撰写模式。
4. 至少包含一个示例。
5. 包含已知的 failure mode 和反适用情况。
6. 关联相关模式。
7. 更新 [catalog/README.md](../../../catalog/README.md)。

## 本地化文档

docs/i18n/ 中的本地化快速开始和维基镜像是公开入口。当项目描述、核心分类、安全/隐私语言或贡献工作流发生变化时，请同步更新本地化文档，或在 pull request 中说明为何无需更新翻译。

若无法自信地更新某种语言，请尽量减小英文源变更的范围，并请求翻译审查。

## Evidence 标准

初期的 evidence 可以较为轻量，但必须诚实。

有用的 evidence 包括：

- 在多个任务中反复观察到的 workflow。
- Before/after comparison。
- Transcript excerpt 或摘要事件。
- Test result、review result 或避免的缺陷。
- 经过反复使用而沉淀下来的本地惯例。

避免使用诸如"效果更好"之类的模糊说法，而不解释具体改进了什么。

## 写作风格

面向有能力的人类和有能力的代理写作。保持直接、具体，对不确定性保持谦逊。

本项目不应成为励志性 prompt 技巧列表，而应成为实用的 pattern language。
