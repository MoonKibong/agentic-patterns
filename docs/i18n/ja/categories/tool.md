# ツールパターン

Tool pattern はエージェントが shell コマンド、ブラウザ、MCP サーバー、API、
パッケージマネージャー、Git、その他の実際の状態に影響を与えられる機能を
どのように使用すべきかを定義します。

エージェントが外部機能を通じて行動しなければならず、影響範囲を明確にする必要がある場合に使用します。

## 現在のパターン

- [ツール利用契約 (Tool-Use Contract)](../../../../patterns/tool/tool-use-contract.md): 許可されたツール、承認トリガー、禁止されたアクション、証拠の期待値を定義します。

## パターンアイデア

- Read-First Tooling.
- Approval Boundary.
- Verification Command.
- External State Guard.

## 関連カテゴリ

- [ハーネスパターン](harness.md)
- [プロンプトパターン](prompt.md)
- [評価パターン](evaluation.md)
