# 模式语言的根源

Agentic Patterns 不是一个 prompt 技巧集合。它更深层的模型来自 pattern-language 传统：为反复出现的问题命名，描述使其困难的 forces，记录可复用的核心解法，并使该解法能够在人类与工具之间传播。

## Christopher Alexander

Christopher Alexander 和同事通过 *A Pattern Language: Towns, Buildings, Construction* 和 *The Timeless Way of Building* 等著作，发展了建筑和城市设计的 pattern-language 传统。他们的模式描述了城镇、建筑和房间中反复出现的问题，以及可以复用而非机械复制的解法。

对本项目而言，重要的不是建筑这个领域本身，而是 pattern language 的社会与认知功能：

- 模式为反复出现的设计情境命名。
- 记录使情境变得困难的 forces 和 tradeoff。
- 描述解法形态，而非固定脚本。
- 让专家与非专家都能讨论设计决策。
- 模式组合成语言，使更大的设计可以由更小的命名操作构建而成。

最后一点至关重要。孤立技巧的目录还不是语言。当模式相互引用、相互约束，并让社区拥有讨论重复工作的共同词汇时，pattern language 才真正变得有用。

## GoF Design Patterns

软件设计模式运动将这一理念应用于面向对象软件。Gang of Four 的 *Design Patterns: Elements of Reusable Object-Oriented Software* 通过收录 Factory Method、Adapter、Composite、Decorator、Observer、Strategy 等命名的可复用解法，将模式格式广泛传播给软件工程师。

GoF 目录在这里有几点实践价值：

- 模式成为 design review 的沟通工具。
- 模式名称压缩了复杂的设计讨论。
- 可复用结构与一次性实现细节得以分离。
- Tradeoff 和适用性成为工程判断的一部分。
- 共同词汇改善了团队协作。

这并不意味着 agentic workflow 应该照搬 GoF 的分类。真正的启示是：反复实践一旦被命名、结构化、批评和传授，就会变得更加有力。

## Agentic Work 为何需要 Pattern Language

Agentic coding 最先使这种需求变得清晰可见。开发者反复遇到同样的问题：

- 代理应该接收什么上下文？
- 何时需要在行动前先规划？
- 哪些工具可以使用，approval boundary 是什么？
- reviewer 或 critique loop 何时值得投入？
- 哪些状态必须在 chat compaction、handoff 或重启后得以保留？

同样的问题在编程之外同样出现：

- Image generation 需要 brief、reference、variation control、critique 和 selection。
- Writing 需要 voice、outline、continuity、critique 和 revision。
- Design generation 需要 constraint、feasibility review、artifact handoff 和 human approval。
- Video/media work 需要 storyboard、continuity ledger、render gate 和 provenance。
- Research 需要 source ledger、claim check、citation anchor 和 review loop。

这就是为什么本项目使用"human-guided AI work"，而不仅仅是"agentic coding"。Coding 是第一个成熟的领域，但 underlying pattern language 的范围更广。

## 作为 Memetic Operational Knowledge 的模式

模式在实用意义上是 memetic 的：它们是可以传播、修改和重组的紧凑文化单元。好的模式让社区无需重复原始发现过程，就能记住有用的解法。

Agentic pattern 因为在人类与 AI 系统之间进行调解，所以特别具有 memetic 特性。它们不仅告诉人类该做什么，还塑造 AI 代理能够识别、选择和执行的内容。

在本项目中，模式应帮助回答：

- 反复出现的情境是什么？
- 是什么使其变得困难？
- 哪种可复用操作有所帮助？
- 有哪些 evidence 或示例支撑它？
- 何时不应使用它？
- 代理如何识别并应用它？

## 人类判断始终处于核心位置

AI 系统是强大的模式匹配器，但并不拥有目标。人类提供目的、品味、记忆、社会情境、伦理判断，以及决定何时应该打破模式的能力。

Agentic Patterns 的目标因此不是自动化并取代人类判断，而是让人类判断中可复用的部分足够清晰，使人类与代理能够更好地协作。

## 参考资料

- Christopher Alexander, Sara Ishikawa, Murray Silverstein, et al., *A Pattern Language: Towns, Buildings, Construction*, Oxford University Press, 1977.
- Christopher Alexander, *The Timeless Way of Building*, Oxford University Press, 1979.
- Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides, *Design Patterns: Elements of Reusable Object-Oriented Software*, Addison-Wesley, 1994.
- Hillside Group 和 Pattern Languages of Programs 社区通过 writer's workshop 和 pattern conference 延续了软件模式传统。

公开参考入口：

- [A Pattern Language](https://en.wikipedia.org/wiki/A_Pattern_Language)
- [Pattern language](https://en.wikipedia.org/wiki/Pattern_language)
- [Design Patterns](https://en.wikipedia.org/wiki/Design_Patterns)
- [The Hillside Group](https://en.wikipedia.org/wiki/The_Hillside_Group)
- [Pattern Languages of Programs](https://en.wikipedia.org/wiki/Pattern_Languages_of_Programs)
