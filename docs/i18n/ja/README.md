# Agentic Patterns ウィキ

Agentic Patterns の日本語ウィキへようこそ。

質問から始めてカテゴリ、ドメイン、個別パターンへ進めるよう構成されています。
英語ドキュメントが最終的な基準であり、このドキュメントは現行の公開ドキュメントの日本語ミラーです。

## はじめに

- [プロジェクト概要](project-brief.md): プロジェクトの目的と背景。
- [パターン言語のルーツ](foundations/pattern-language-roots.md): Christopher Alexander、GoF、そして agentic patterns の動機。
- [パターン言語](pattern-language.md): パターンドキュメントの構造と品質基準。
- [Evidence Hygiene（証拠衛生）](evidence-hygiene.md): 非公開ソリューションの詳細を漏らさない例の書き方。
- [Agentic Work トレンド](research/2026-agentic-work-trends.md): なぜコーディングを超えて広がるのか。
- [カタログ](../../../catalog/README.md): 現在のパターン一覧。
- [ロードマップ](roadmap.md): 今後の方向性。
- [コントリビューションガイド](CONTRIBUTING.md): パターンとフィールドノートの追加方法。
- [ローカライズされたクイックスタート](../README.md): 初めて読む人向けの短い翻訳。
- [オープンソース準備](oss/OPEN_SOURCE_READINESS.md): 公開リリースチェックリスト。

## 目標別ナビゲーション

| 目標 | 開始ドキュメント |
| --- | --- |
| プロジェクトを理解する | [プロジェクト概要](project-brief.md) |
| 知的背景を理解する | [パターン言語のルーツ](foundations/pattern-language-roots.md) |
| 再利用可能なパターンを探す | [カタログ](../../../catalog/README.md) |
| エージェントにより良いコンテキストを与える | [コンテキストパケット (Context Packet)](../../../patterns/context/context-packet.md) |
| エージェントの役割を定義する | [ロール契約 (Role Contract)](../../../patterns/prompt/role-contract.md) |
| 長期エージェント作業を調整する | [永続セッション状態 (Durable Session State)](../../../patterns/orchestration/durable-session-state.md) |
| shell、MCP、ブラウザ使用の境界を設定する | [ツール利用契約 (Tool-Use Contract)](../../../patterns/tool/tool-use-contract.md) |
| 画像、執筆、デザイン生成を指示する | [クリエイティブブリーフパケット (Creative Brief Packet)](../../../patterns/context/creative-brief-packet.md) |
| 生成候補を反復改善する | [生成-批評-改善 (Generate-Critique-Refine)](../../../patterns/harness/generate-critique-refine.md) |
| 観察を記録する | [フィールドノートテンプレート](../../../field-notes/_template.md) |

## カテゴリ別ナビゲーション

- [プロンプトパターン](categories/prompt.md)
- [コンテキストパターン](categories/context.md)
- [ハーネスパターン](categories/harness.md)
- [ツールパターン](categories/tool.md)
- [メモリパターン](categories/memory.md)
- [評価パターン](categories/evaluation.md)

## ドメイン別ナビゲーション

- [コーディング](domains/coding.md)
- [画像生成](domains/image-generation.md)
- [執筆と文学生成](domains/writing.md)
- [デザイン生成](domains/design.md)
- [動画とメディア](domains/video-media.md)
- [調査と分析](domains/research-analysis.md)

## エージェントへの案内

- 修正前にリポジトリルートの `AGENTS.md` を読んでください。
- 公開・非公開の境界を守り、非公開パターン名やローカルツール名を公開ドキュメントに追加しないでください。
- パターンファイルを変更した後はリポジトリの検証手順を実行してください。

## コントリビューターへの案内

- [コントリビューションガイド](CONTRIBUTING.md) から始めてください。
- 新しいパターンには [パターンテンプレート](../../../patterns/_template.md) を使用してください。
- 初期の観察には [フィールドノートテンプレート](../../../field-notes/_template.md) を使用してください。
- 公開前に [ライセンス](licensing.md) を確認してください。
- 例やフィールドノートを追加する前に [Evidence Hygiene（証拠衛生）](evidence-hygiene.md) を確認してください。
- ユーザー向けドキュメントを変更する際は [ローカライズされたクイックスタート](../README.md) を確認してください。
