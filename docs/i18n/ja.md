# Agentic Patterns クイックスタート

Agentic Patterns は、人間が AI をよりよく導くためのパターン言語です。

反復的な AI ワークフローで使えるプロンプト、コンテキストパケット、ハーネス、
ロール契約、ツール利用プロトコル、メモリ、評価ループを整理します。

## スコープ

このプロジェクトは agentic coding から始まりましたが、次の領域も扱います。

- 画像生成
- 執筆と文学生成
- デザイン生成
- 動画とメディア
- 調査と分析

## コアカテゴリ

- `prompt`: 再利用可能な指示とロール構造
- `context`: タスクパケット、クリエイティブブリーフ、メモリ要約
- `harness`: plan/execute/review と generate/critique/refine のループ
- `orchestration`: 複数エージェントや複数セッションの調整
- `tool`: shell、browser、MCP、API、外部ツールの境界
- `memory`: 永続状態と再利用可能な知識
- `evaluation`: パターン適合性チェック、ルーブリック、レビュー方法

## はじめに

- 言語パック入口: [docs/i18n/ja/README.md](ja/README.md)
- ドキュメントホーム: [docs/README.md](../README.md)
- カタログ: [catalog/README.md](../../catalog/README.md)
- パターンテンプレート: [patterns/_template.md](../../patterns/_template.md)
- 公開前にリンクとプライバシー境界を確認してください。

## Evidence Hygiene

例は synthetic、sanitized、public のいずれかにしてください。非公開プロンプト、
非公開ハーネスの詳細、顧客データ、認証情報、private URL、内部リポジトリ名を
公開しないでください。
