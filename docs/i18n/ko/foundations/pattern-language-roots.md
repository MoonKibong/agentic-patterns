# 패턴 언어의 뿌리

Agentic Patterns는 prompt trick 모음이 아닙니다. 더 깊은 모델은 pattern-language 전통에서
옵니다. 반복되는 문제에 이름을 붙이고, 그 문제를 어렵게 만드는 forces를 설명하며,
재사용 가능한 solution core를 기록하고, 그 해법을 사람과 도구가 함께 말할 수 있게 만드는
것입니다.

## Christopher Alexander

Christopher Alexander와 동료들은 *A Pattern Language: Towns, Buildings, Construction*,
*The Timeless Way of Building* 같은 작업을 통해 건축과 도시 설계의 pattern-language 전통을
발전시켰습니다. 그들의 패턴은 도시, 건물, 방에서 반복되는 문제와, 기계적으로 복사하는 것이
아니라 재사용 가능한 해법을 함께 설명했습니다.

이 프로젝트에서 중요한 것은 건축이라는 도메인 자체가 아닙니다. 중요한 것은 pattern
language의 사회적, 인지적 기능입니다.

- 패턴은 반복되는 design situation에 이름을 붙입니다.
- 상황을 어렵게 만드는 forces와 tradeoff를 기록합니다.
- 고정된 script가 아니라 solution shape를 설명합니다.
- 전문가와 비전문가가 design decision을 이야기할 수 있게 합니다.
- 패턴들이 서로 결합되어 더 큰 설계를 만드는 언어가 됩니다.

고립된 tip의 catalog는 아직 language가 아닙니다. Pattern language는 패턴들이 서로를
부르고, 제약하고, 커뮤니티가 반복 작업을 이야기할 shared words를 가질 때 유용해집니다.

## GoF Design Patterns

Software design-pattern movement는 이 아이디어를 object-oriented software에 적용했습니다.
Gang of Four의 *Design Patterns: Elements of Reusable Object-Oriented Software*는 Factory
Method, Adapter, Composite, Decorator, Observer, Strategy 같은 이름 붙은 반복 해법을
카탈로그화하면서 software engineer에게 pattern format을 널리 알렸습니다.

GoF catalog가 여기서 중요한 이유:

- 패턴은 design review의 communication tool이 되었습니다.
- Pattern name은 복잡한 design discussion을 압축했습니다.
- 재사용 구조와 one-off implementation detail을 분리했습니다.
- Tradeoff와 applicability가 engineering judgment의 일부가 되었습니다.
- Shared vocabulary가 team collaboration을 개선했습니다.

Agentic workflow가 GoF category를 그대로 복사해야 한다는 뜻은 아닙니다. 반복 practice는
이름 붙이고, 구조화하고, 비판하고, 가르칠 때 더 강력해진다는 뜻입니다.

## Agentic Work에 Pattern Language가 필요한 이유

Agentic coding은 이 필요를 가장 먼저 분명히 드러냈습니다. 개발자는 같은 질문을 반복해서
다시 만납니다.

- 에이전트에 어떤 context를 줘야 하는가?
- 언제 plan before acting이 필요한가?
- 어떤 tool을 어떤 approval boundary로 사용할 수 있는가?
- reviewer나 critique loop는 언제 비용을 정당화하는가?
- chat compaction, handoff, restart 후에도 어떤 state가 살아남아야 하는가?

같은 질문은 coding 밖에서도 나타납니다.

- Image generation에는 brief, reference, variation control, critique, selection이 필요합니다.
- Writing에는 voice, outline, continuity, critique, revision이 필요합니다.
- Design generation에는 constraint, feasibility review, artifact handoff, human approval이 필요합니다.
- Video/media work에는 storyboard, continuity ledger, render gate, provenance가 필요합니다.
- Research에는 source ledger, claim check, citation anchor, review loop가 필요합니다.

그래서 이 프로젝트는 "agentic coding"만이 아니라 "human-guided AI work"를 말합니다. Coding은
첫 번째 성숙한 도메인이지만 underlying pattern language는 더 넓습니다.

## Memetic Operational Knowledge로서의 패턴

패턴은 실용적인 의미에서 memetic합니다. 전달되고, 수정되고, 재결합될 수 있는 compact
cultural unit입니다. 좋은 패턴은 커뮤니티가 원래 발견 과정을 반복하지 않고도 유용한 해법을
기억하게 합니다.

Agentic pattern은 사람과 AI system 사이를 매개하기 때문에 특히 memetic합니다. 사람에게만
무엇을 하라고 말하는 것이 아니라, AI agent가 무엇을 인식하고, 선택하고, 실행할 수 있는지도
형성합니다.

이 프로젝트에서 패턴은 다음 질문에 답해야 합니다.

- 반복되는 상황은 무엇인가?
- 무엇이 어렵게 만드는가?
- 어떤 reusable move가 도움이 되는가?
- 어떤 evidence나 example이 있는가?
- 언제 사용하지 말아야 하는가?
- 에이전트가 어떻게 인식하고 적용할 수 있는가?

## Human Judgment Remains Central

AI system은 강력한 pattern matcher이지만 목표를 소유하지 않습니다. 인간은 purpose, taste,
memory, social context, ethical judgment, 그리고 pattern을 깨야 할 때를 결정하는 능력을
제공합니다.

Agentic Patterns의 목표는 human judgment를 자동화해서 없애는 것이 아닙니다. 인간 판단의
재사용 가능한 부분을 충분히 legible하게 만들어 사람과 agent가 더 잘 협력하게 하는 것입니다.

## Source Notes

- Christopher Alexander, Sara Ishikawa, Murray Silverstein, et al., *A Pattern Language: Towns,
  Buildings, Construction*, Oxford University Press, 1977.
- Christopher Alexander, *The Timeless Way of Building*, Oxford University Press, 1979.
- Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides, *Design Patterns: Elements of Reusable
  Object-Oriented Software*, Addison-Wesley, 1994.
- Hillside Group과 Pattern Languages of Programs community는 writer's workshop과 pattern
  conference를 통해 software-pattern 전통을 이어갔습니다.

Public entry points:

- [A Pattern Language](https://en.wikipedia.org/wiki/A_Pattern_Language)
- [Pattern language](https://en.wikipedia.org/wiki/Pattern_language)
- [Design Patterns](https://en.wikipedia.org/wiki/Design_Patterns)
- [The Hillside Group](https://en.wikipedia.org/wiki/The_Hillside_Group)
- [Pattern Languages of Programs](https://en.wikipedia.org/wiki/Pattern_Languages_of_Programs)
