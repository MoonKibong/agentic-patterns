# 2026 Agentic Work Trends

このノートは agentic coding と隣接するクリエイティブワークフローに関する最近の公開シグナルを
要約します。Gemini のリサーチ出力を intake として使用しましたが、このドキュメントには
公開ソースから検証可能か、リサーチリードとして明示できる内容のみを記録します。

## Executive Summary

Agentic coding は human-guided AI work のための初期パターンライブラリとして最も具体的な
領域になりつつあります。リポジトリ、シェル、テスト、コードレビュー、サンドボックス、
プルリクエストがコンテキストと検証を可視化するからです。同じプリミティブは画像生成、
執筆、デザイン、video/media、リサーチのワークフローにも現れています。

- 境界のあるコンテキストパケットとブリーフ
- ロール固有のエージェントまたはサブエージェント
- ツール利用プロトコル
- generate-critique-refine ループ
- plan-execute-verify-review ループ
- 永続状態と引き継ぎアーティファクト
- 出典と引用追跡
- 人間の承認ゲート
- 安全性とガバナンスのラッパー

カタログは再利用可能なプリミティブを中心に整理し、ドメインページでそれらのプリミティブが
コーディング、画像生成、執筆、デザイン、video/media、リサーチにどのように適用されるかを
示すべきです。

## 検証済みソースノート

| Source | Date | Relevance |
| --- | --- | --- |
| [OpenAI, Introducing Codex](https://openai.com/index/introducing-codex/) | 2025 | ソフトウェアエンジニアリングのためのクラウドタスク実行を提示。サンドボックス化されたタスク委任、リポジトリコンテキスト、テスト実行、PR スタイルのワークフローを強調。 |
| [OpenAI Agents SDK Docs](https://openai.github.io/openai-agents-python/) | 2025-2026 | エージェント、引き継ぎ、ガードレール、トレーシング、ツールをファーストクラスのプリミティブとして文書化。 |
| [Anthropic Claude Code Subagents](https://docs.anthropic.com/en/docs/claude-code/sub-agents) | 2025-2026 | 個別のコンテキストウィンドウ、カスタムプロンプト、ツール権限を持つタスク固有のサブエージェントを説明。 |
| [Anthropic Claude Code Hooks](https://docs.anthropic.com/en/docs/claude-code/hooks) | 2025-2026 | 承認ゲートとツールガバナンスに有用な、エージェント動作に関する決定論的なコントロールポイントを示す。 |
| [Model Context Protocol Introduction](https://modelcontextprotocol.io/introduction) | 2025-2026 | MCP をアプリケーションが言語モデルにツールとコンテキストを公開するための標準的な方法として位置付ける。 |
| [Google A2A Protocol](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) | 2025 | エージェント間の相互運用性と委任への関心の高まりを示す。 |
| [arXiv: The 2025 AI Agent Index](https://arxiv.org/abs/2602.17753) | 2026 | AI エージェントシステムを調査し、エージェント機能とデプロイメントパターンの評価の必要性を強調。 |
| [arXiv: VideoAgent](https://arxiv.org/abs/2606.23327) | 2026 | ビデオ編集ワークフローのための agentic 分解を実証。 |
| [HKUDS ViMax](https://github.com/HKUDS/ViMax) | 2026 | テキスト/ストーリー入力からの agentic ビデオ生成の公開リポジトリ。メディアパイプラインのリサーチリードとして有用。 |

## Trend: Context Engineering が製品サーフェスになる

Agentic システムはコンテキストをチャット履歴ではなく構造化された入力として
扱い始めています。コーディングエージェントはリポジトリファイル、指示、issue テキスト、
テスト、環境状態を使用します。クリエイティブシステムには同等のブリーフが必要です:
参照、スタイル制約、継続性アンカー、対象者、成果物、評価基準。

カタログへの影響:

- [Context Packet](../../../../patterns/context/context-packet.md) を一般パターンとして維持します。
- クリエイティブドメインには [Creative Brief Packet](../../../../patterns/context/creative-brief-packet.md) を追加します。
- 将来のパターン: `Reference Board`、`Source Ledger`、`Context Compactor`。

## Trend: エージェントはハーネスでラップされる

重要な変化はモデルが強くなっただけではありません。有用なシステムはモデルを
計画、実行、批評、検証、ガードレール、トレーシング、承認ゲートでラップします。
コーディングでは plan-execute-test-review として、クリエイティブ作業では
brief-generate-critique-refine-select として現れます。

カタログへの影響:

- ソフトウェアとその他の検証可能な作業には明示的なレビューと検証ループを維持します。
- クリエイティブおよび探索的な作業には [Generate-Critique-Refine](../../../../patterns/harness/generate-critique-refine.md) を追加します。
- 将来のパターン: `Rubric Review`、`Human Approval Gate`、`Guardian Gate`。

## Trend: ツールプロトコルとエージェント相互運用性が重要になる

MCP とエージェント間プロトコルは agentic ワークフローが明示的な機能境界に
ますます依存していることを示しています。ツールと外部システムは発見可能で、
境界があり、監査可能で、安全に使用できる必要があります。

カタログへの影響:

- [Tool-Use Contract](../../../../patterns/tool/tool-use-contract.md) を維持します。
- 将来のパターン: `Capability Manifest`、`Approval Boundary`、`Sandbox Gate`。

## Trend: クリエイティブ作業にアーティファクトライフサイクルパターンが必要になる

画像、執筆、デザイン、ビデオのワークフローは中間アーティファクトを生成します:
ブリーフ、参照、アウトライン、スタイルボード、候補画像、ストーリーボード、
シーンプラン、批評テーブル、最終アセット。これらのアーティファクトには引き継ぎ、
出典、バージョン管理、人間の承認が必要です。

カタログへの影響:

- コアカタログを早まって分割するのではなくドメインページを追加します。
- 将来のパターン: `Artifact Handoff`、`Provenance Ledger`、`Variation Ladder`、
  `Style Lock`、`Continuity Ledger`。

## Source Hygiene（ソース衛生）

Gemini のリサーチ出力には有用なリードが含まれていましたが、このリポジトリは
生成された引用をデフォルトで検証済みとして扱うべきではありません。
公開ドキュメントのために:

- 一次ソースと公式ドキュメントを優先する
- 未検証の項目はリードとしてマークする
- 非公開ワークフローを引用しない
- 公開証拠が独自の手法を明かす可能性がある場合は synthetic example を使用する
