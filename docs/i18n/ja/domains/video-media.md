# 動画とメディア

Video と media のワークフローは出力がマルチステップ、マルチアセット、コストが高く、
継続性に敏感であるため、agentic な構造の必要性が特に大きくなります。

## 共通の Forces

- ストーリー、ショット構成、キャラクターの継続性、音声、タイミング、スタイルが
  整合されている必要があります。
- 高品質なクリップのレンダリングはコストがかかります。
- 小さな上流の変更が下流のアセットを無効化することがあります。
- スクリプト、ストーリーボード、キーフレーム、最終レンダーの各段階で
  人間の承認が必要になる場合があります。

## 有用なパターン

- [クリエイティブブリーフパケット (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md)
- [生成-批評-改善 (Generate-Critique-Refine)](../../../../patterns/harness/generate-critique-refine.md)
- [永続セッション状態 (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)
- [ロール契約 (Role Contract)](../../../../patterns/prompt/role-contract.md)
- [ツール利用契約 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)

## 候補パターン

- Storyboard Gate.
- Asset Handoff.
- Continuity Ledger.
- Render Budget Gate.
- Provenance Ledger.
