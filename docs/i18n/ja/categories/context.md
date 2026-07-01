# コンテキストパターン

Context pattern は agentic work に必要な情報のパッケージング、削減、保持、
引き継ぎの方法を定義します。

エージェントが正しく行動するには十分な情報が必要ですが、ファイル、履歴、ログ、
チャット全体をそのまま渡すと重要なシグナルが埋もれてしまいます。

## 現在のパターン

- [コンテキストパケット (Context Packet)](../../../../patterns/context/context-packet.md): 計画、実行、レビュー、引き継ぎの前に境界のあるタスクコンテキストを提供します。
- [クリエイティブブリーフパケット (Creative Brief Packet)](../../../../patterns/context/creative-brief-packet.md): クリエイティブな意図、制約、参照、成果物、評価基準をまとめます。

## パターンアイデア

- Handoff Summary.
- Constraint Header.
- Evidence Bundle.
- Resume Capsule.

## 関連カテゴリ

- [プロンプトパターン](prompt.md)
- [メモリパターン](memory.md)
