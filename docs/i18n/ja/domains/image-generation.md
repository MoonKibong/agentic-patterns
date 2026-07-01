# 画像生成

Image generation は単一のプロンプトを超えるもの——参照、スタイルの一貫性、バリエーション、
批評、選択、下流のデザインやメディア作業への引き継ぎ——が必要な場合に agentic pattern の
恩恵を受けます。

## 共通の Forces

- 曖昧なプロンプトは視覚的にもっともらしくても意図からずれた画像を生成することがあります。
- 参照とスタイルワードが競合することがあります。
- 人間のセンスが中心であり、自動スコアリングの背後に隠すべきではありません。
- 反復はコストがかかるか、元の意図からドリフトする可能性があります。

## 有用なパターン

- [クリエイティブブリーフパケット (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md)
- [生成-批評-改善 (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md)
- [永続セッション状態 (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)
- [ツール利用契約 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)

## 候補パターン

- Reference Board.
- Style Lock.
- Variation Ladder.
- Provenance Ledger.
- Human Approval Gate.
