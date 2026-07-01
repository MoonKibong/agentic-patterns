# 图像生成

当用户需要的不只是单个 prompt，还涉及 reference、style continuity、variation、critique、selection 以及向下游设计或媒体工作的移交时，图像生成便能从 agentic pattern 中受益。

## 常见压力

- 宽泛的 prompt 会生成视觉上合理但方向偏差的图像。
- Reference 和 style word 可能相互冲突。
- Human taste 是核心，不应被 automatic scoring 所掩盖。
- 迭代可能代价高昂，或逐渐偏离原始意图。

## 有用的模式

- [创意简报包 (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md)
- [生成-批评-优化 (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md)
- [持久会话状态 (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)
- [工具使用契约 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)

## 候选模式

- Reference Board。
- Style Lock。
- Variation Ladder。
- Provenance Ledger。
- Human Approval Gate。
