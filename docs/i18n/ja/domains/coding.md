# コーディング

Coding は Agentic Patterns のシードドメインです。リポジトリ、ファイル、テスト、
シェル、issue、プルリクエスト、CI、レビュー結果などのアーティファクトが
明確に見えるためです。

## 共通の Forces

- エージェントには十分なリポジトリコンテキストが必要ですが、無関係なファイルに埋もれてはいけません。
- ツール使用はローカルまたはリモートの状態を変更する可能性があります。
- レビューとテストは欠陥を見つけられますが、ワークフローの一部になった場合のみです。
- 長期タスクには永続的な状態と再開可能な引き継ぎが必要です。

## 有用なパターン

- [コンテキストパケット (Context Packet)](../../../../patterns/context/context-packet.md)
- [ロール契約 (Role Contract)](../../../../patterns/prompt/role-contract.md)
- [ツール利用契約 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md)
- [永続セッション状態 (Durable Session State)](../../../../patterns/orchestration/durable-session-state.md)

## 候補パターン

- Human Approval Gate.
- Guardian Gate.
- Provenance Ledger.
- Verification Ladder.
- Context Compactor.
