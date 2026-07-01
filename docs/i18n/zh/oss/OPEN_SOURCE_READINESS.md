# 开源准备

本文档记录 Agentic Patterns 的推荐公开发布默认值。

## 任务评估

Verdict：`REVISE`，直到翻译版快速开始和完整维基镜像经过人工审查。

主要风险：本项目灵感来自真实的 agentic workflow，因此公开文档必须避免暴露 proprietary prompt、private harness detail、customer data、private repo name 和 internal workflow transcript。

## 定位

Agentic Patterns 是一种用于 human-guided AI work 的 pattern language。它不是 prompt 集合，也不是 vendor-specific agent framework。Coding 是第一个成熟的领域，但目录也涵盖 image generation、writing、design、video/media、research 和 analysis。

## 许可协议

- Documentation、pattern catalog、prompt 和 field note：CC BY 4.0。
- Code、schema 和已批准的 software artifact：MIT。

## 发布阶段

首个公开 release 以 `v0.1.0` seed catalog 发布。不将 draft pattern 表述为经过验证的最佳实践。

## Evidence 与隐私政策

要求使用 synthetic、sanitized 或明确公开的示例。将 private prompt、customer data、private URL 或 proprietary workflow detail 的意外泄露视为安全敏感事件。

## CI

对于以 Markdown 为主的公开仓库，CI 在公开验证器获批后可从 markdown lint 和 link check 开始。

## 贡献

PR 必须包含：用户可见的 doc 或模式变更摘要、verification command、evidence/privacy impact、i18n impact 以及相关 issue 链接。

## 发布检查清单

1. 确认 license 文件。
2. 确认 `README.md`、`CONTRIBUTING.md`、`SECURITY.md`、`CODE_OF_CONDUCT.md`、`CHANGELOG.md`、`RELEASE.md` 均已就位。
3. 确认 issue 和 PR template 存在。
4. 运行已批准的 public review 和 validation check。
5. 审查 `docs/i18n/` 快速开始和维基镜像。
6. 搜索 private term、private URL、credential 和 internal repo name。
7. 以 seed-stage language 创建 GitHub release。
