# Evidence Hygiene

Agentic Patterns 应在不暴露专有解决方案细节的前提下发挥价值。

目录可以根植于实践，同时保护 private prompt、harness、repo、customer、credential、transcript 和 internal workflow mechanic。

## 原则

公开模式，不公开私有事件。

示例应展示以下可复用结构：

- 问题形态。
- Forces 与 tradeoff。
- Procedure。
- Expected output。
- Failure mode。
- Verification style。

示例不应暴露私有实现细节。

## 安全的 Evidence 类型

- 保留工作流结构的 synthetic example。
- 移除 private identifier 的 sanitized field note。
- 来自 open source repository、paper、docs、blog post 或 issue thread 的 public example。
- 不含识别信息的聚合观察。

## 不得公开

- Customer data。
- Credential、token 或 private URL。
- Private repository name。
- 未打算公开的 internal prompt text。
- 完整的 proprietary harness logic。
- 私有项目的 full workflow transcript。
- 产品方向、商业策略或未发布的实现细节。

## Field Note 清洗方法

1. 将项目名替换为 `web app`、`API service`、`agent runner` 等通用名称。
2. 将文件路径替换为 `src/billing/service.ts` 等代表性路径。
3. 移除 credential、hostname、private issue number 和 private branch name。
4. 对 transcript 进行摘要，而非逐字引用。
5. 保留与模式相关的成功或失败条件。
6. 注明示例为 synthetic 或 sanitized。

## Synthetic Example 政策

鼓励使用 synthetic example。示例应具体到足以指导行动，但无需与真实的私有工作流对应。

好的 synthetic example：

- 包含具体的 file、role 或 command。
- 体现模式的 forces。
- 展示代理应输出什么。
- 避免项目特定的 secret。

糟糕的 synthetic example 过于模糊，无法执行，例如"让代码更好"或"使用更好的 prompt"。
