# パターン言語のルーツ

Agentic Patterns はプロンプトトリックの集まりではありません。より深いモデルは
pattern-language の伝統から来ています。反復する問題に名前をつけ、その問題を難しくする
forces を説明し、再利用可能な解法の核心を記録し、その解法を人間とツールが共に
語れるものにすることです。

## Christopher Alexander

Christopher Alexander と共同研究者たちは *A Pattern Language: Towns, Buildings, Construction*
や *The Timeless Way of Building* などの作業を通じて、建築と都市設計の pattern-language の
伝統を発展させました。彼らのパターンは都市、建物、部屋における反復する問題と、
機械的にコピーするのではなく再利用できる解法を共に説明しました。

このプロジェクトで重要なのは建築というドメイン自体ではありません。重要なのは
pattern language の社会的・認知的機能です。

- パターンは反復する設計状況に名前をつけます。
- 状況を難しくする forces とトレードオフを記録します。
- 固定されたスクリプトではなく解法の形を説明します。
- 専門家と非専門家が設計上の決定について話せるようにします。
- パターンが互いに組み合わさって言語になり、より大きな設計が小さな名前のついた
  手法から構築できます。

その最後の点が重要です。孤立したティップのカタログはまだ言語ではありません。
パターン言語はパターンが互いを呼び出し、制約し、コミュニティが反復する作業のための
共有された言葉を持つようになって初めて有用になります。

## GoF Design Patterns

ソフトウェアデザインパターン運動はこのアイデアをオブジェクト指向ソフトウェアに
適用しました。Gang of Four の *Design Patterns: Elements of Reusable Object-Oriented
Software* は Factory Method、Adapter、Composite、Decorator、Observer、Strategy などの
名前のついた反復解法をカタログ化することで、ソフトウェアエンジニアにパターン形式を
広く知らしめました。

GoF カタログがここで重要なのはいくつかの実用的な貢献のためです。

- パターンは設計レビューのためのコミュニケーションツールになりました。
- パターン名は複雑な設計議論を圧縮しました。
- 再利用可能な構造と一度限りの実装詳細を分離しました。
- トレードオフと適用可能性がエンジニアリング判断の一部になりました。
- 共有された語彙がチーム間の協力を改善しました。

教訓は agentic ワークフローが GoF カテゴリをコピーすべきということではありません。
教訓は反復する実践に名前をつけ、構造化し、批評し、教えることでより強力になるということです。

## なぜ Agentic Work にパターン言語が必要か

Agentic coding はこの必要性を最初に明確にしました。開発者は同じワークフローの
問いを繰り返し再発見します。

- エージェントにどんなコンテキストを渡すべきか?
- いつエージェントが行動前に計画すべきか?
- どのツールをどんな承認境界で使えるか?
- レビュアーや批評ループはいつコストに見合うか?
- チャットの圧縮、引き継ぎ、再起動を経てどんな状態が生き残らなければならないか?

同じ問いはコーディングの外でも現れます。

- 画像生成にはブリーフ、参照、バリエーション制御、批評、選択が必要です。
- 執筆には声、アウトライン、一貫性、批評、改訂が必要です。
- デザイン生成には制約、実現可能性レビュー、アーティファクトの引き継ぎ、人間の承認が必要です。
- Video/media 作業にはストーリーボード、継続性台帳、レンダーゲート、出典が必要です。
- リサーチにはソース台帳、主張チェック、引用アンカー、レビューループが必要です。

だからこそこのプロジェクトは「agentic coding」だけでなく「human-guided AI work」を
語ります。Coding は最初の成熟したドメインですが、基礎となるパターン言語はより広いのです。

## Memetic Operational Knowledge としてのパターン

パターンは実用的な意味で memetic です。伝達され、修正され、再結合できる
コンパクトな文化的単位です。良いパターンはコミュニティが元の発見プロセスを
繰り返すことなく有用な解法を記憶できるようにします。

Agentic pattern は人間と AI システムの間を媒介するため特に memetic です。
人間に何をすべきか指示するだけでなく、AI エージェントが何を認識し、
選択し、実行できるかも形成します。

このプロジェクトでパターンは以下の問いに答えるべきです。

- 反復する状況とは何か?
- 何が難しくしているか?
- どんな再利用可能な手法が助けになるか?
- どんな証拠や例があるか?
- いつ使うべきでないか?
- エージェントはどのように認識して適用できるか?

## 人間の判断が中心であり続ける

AI システムは強力なパターンマッチャーですが、目標を所有しません。人間は目的、
センス、記憶、社会的コンテキスト、倫理的判断、そしてパターンを破るべき時を
決定する能力を提供します。

Agentic Patterns の目的は人間の判断を自動化してなくすことではありません。
人間の判断の再利用可能な部分を十分に legible（読み取りやすく）にして、
人間とエージェントがより良く協力できるようにすることです。

## 出典ノート

- Christopher Alexander, Sara Ishikawa, Murray Silverstein, et al., *A Pattern Language: Towns,
  Buildings, Construction*, Oxford University Press, 1977.
- Christopher Alexander, *The Timeless Way of Building*, Oxford University Press, 1979.
- Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides, *Design Patterns: Elements of Reusable
  Object-Oriented Software*, Addison-Wesley, 1994.
- Hillside Group と Pattern Languages of Programs コミュニティは writers' workshop と
  pattern conference を通じてソフトウェアパターンの伝統を継続しました。

公開エントリポイント:

- [A Pattern Language](https://en.wikipedia.org/wiki/A_Pattern_Language)
- [Pattern language](https://en.wikipedia.org/wiki/Pattern_language)
- [Design Patterns](https://en.wikipedia.org/wiki/Design_Patterns)
- [The Hillside Group](https://en.wikipedia.org/wiki/The_Hillside_Group)
- [Pattern Languages of Programs](https://en.wikipedia.org/wiki/Pattern_Languages_of_Programs)
