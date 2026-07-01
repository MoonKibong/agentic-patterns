# デザイン生成

Design generation にはプロダクトデザイン、インターフェースコンセプト、
design-to-code、ビジュアルシステム、レイアウト探索、アセットの引き継ぎが含まれます。

## 共通の Forces

- デザインの出力は美しさ、使いやすさ、ブランド、制約、実装コストを
  バランス良く扱わなければなりません。
- エージェントは実装や維持が難しい美しいアーティファクトを生成することがあります。
- Design-to-code はビジュアルな意図と技術的な実行の間に厳格な引き継ぎが必要です。
- コストのかかる下流実装の前に人間のレビューが必要です。

## 有用なパターン

- [クリエイティブブリーフパケット (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md)
- [生成-批評-改善 (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md)
- [ツール利用契約 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)
- [永続セッション状態 (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)

## 候補パターン

- Design Constraint Packet.
- Artifact Handoff.
- Implementation Feasibility Review.
- Variation Ladder.
- Human Approval Gate.
