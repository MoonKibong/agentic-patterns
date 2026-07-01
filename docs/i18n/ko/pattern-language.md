# 패턴 언어

이 문서는 Agentic Patterns 항목의 구조와 품질 기준을 정의합니다.

## 정의

Agentic pattern은 human-AI work에서 반복되는 문제에 대한 이름 붙은 재사용 해법입니다.

패턴은 다음을 설명할 수 있습니다.

- Prompt structure.
- Context structure.
- Planning 또는 execution harness.
- Review와 verification loop.
- Agent role contract.
- MCP/tool protocol.
- Multi-agent coordination move.
- Memory와 state-management practice.

패턴은 software engineering에 한정되지 않습니다. Coding은 test, repository, tool,
review loop가 명확하기 때문에 첫 도메인으로 적합합니다. 하지만 같은 구조는 image
generation, writing, design, video/media production, research, analysis에도 적용됩니다.

## Pattern Metadata

각 패턴은 작은 metadata block으로 시작합니다.

```yaml
---
id: context-packet
name: Context Packet
category: context
status: draft
applies_to:
  - coding agents
  - planning
  - implementation
domains:
  - coding
related:
  - durable-session-state
---
```

`id`는 안정적이고 lowercase hyphen 형식이어야 합니다. `domains`는 선택 항목이지만
권장됩니다. 예: `coding`, `image-generation`, `writing`, `design`, `video-media`,
`research-analysis`, `general`.

## Pattern Sections

특별한 이유가 없다면 다음 섹션을 사용합니다.

### Intent

재사용 가능한 움직임을 한두 문장으로 설명합니다.

### Also Known As

다른 이름이 있으면 적습니다.

### Problem

이 패턴이 해결하는 반복 문제입니다.

### Context

패턴이 적용되는 상황, 전제 조건, 환경 가정입니다.

### Forces

문제를 non-trivial하게 만드는 긴장입니다. 예시:

- Context가 많으면 에이전트에 도움이 되지만, 너무 많으면 중요한 signal이 묻힐 수 있습니다.
- Autonomy가 크면 실행이 빨라지지만, 무제한 autonomy는 risk를 숨길 수 있습니다.
- Agent가 많으면 작업을 병렬화하지만, coordination overhead가 이점을 초과할 수 있습니다.

### Solution

재사용되는 structure, protocol, prompt, harness, tool behavior입니다.

### Agent Recognition Signals

에이전트가 이 패턴을 고려해야 하는 관찰 가능한 신호입니다.

### Procedure

사람 또는 에이전트가 따를 수 있는 구체적인 단계입니다.

### Outputs

패턴 적용 후 생성되어야 하는 아티팩트입니다.

### Stop Conditions

언제 멈추고, escalate하고, 다른 패턴으로 전환해야 하는지입니다.

### Example

짧고 현실적인 예시입니다. 실제 워크플로가 private implementation, customer, prompt,
orchestration detail을 노출할 수 있다면 synthetic example을 선호합니다.

### Failure Modes

패턴이 잘못 적용되는 방식입니다.

### Evidence

관찰 결과, field note, test, review outcome, public source 등입니다.

Evidence는 공개 가능해야 합니다. Sanitized summary, synthetic reproduction, public source를
사용하고 private prompt, proprietary harness logic, customer data, private repo name,
credential, internal transcript를 노출하지 않습니다.

### Related Patterns

함께 쓰이거나 충돌하거나 대체되는 패턴입니다.

## Pattern Status

- `draft`: 가능성은 있지만 안정화되지 않음.
- `candidate`: 여러 번 성공적으로 사용되었고 review 준비됨.
- `accepted`: review를 거쳐 catalog 일부로 인정됨.
- `deprecated`: 역사적 참고용으로 남기지만 더 이상 권장하지 않음.

## Categories

초기 카테고리:

- `prompt`: 재사용 가능한 instruction structure.
- `context`: context packet structure.
- `harness`: planning, execution, review, verification workflow.
- `orchestration`: multi-agent, multi-session coordination.
- `tool`: MCP, CLI, script, environment interaction pattern.
- `memory`: durable knowledge와 state pattern.
- `evaluation`: 패턴이 작동했는지 판단하는 방법.

카탈로그가 성숙하면서 카테고리는 바뀔 수 있습니다.

## Evidence Hygiene

패턴 예시는 private incident 자체가 아니라 재사용 가능한 구조를 가르쳐야 합니다.

허용:

- forces와 procedure를 보존한 synthetic example.
- private identifier를 제거한 sanitized field note.
- open source repository, paper, docs, blog, issue thread 등 public reference.
- "여러 local coding session에서 관찰됨"과 같은 aggregate observation.

금지:

- private repo name, customer name, private URL, credential, log.
- full proprietary prompt, harness internal, MCP/tool protocol.
- unreleased product direction 또는 internal implementation detail이 드러나는 transcript.

의심스러우면 시나리오를 일반화하고 패턴을 operational하게 유지합니다.

## Naming Rules

패턴 이름은 다음과 같아야 합니다:

- 짧게.
- 기억하기 쉽게.
- Operational하게.
- 해당 move를 구분할 수 있을 만큼 구체적으로.

`Better Coding`이나 `Good Context`처럼 단순히 목표만 설명하는 이름은 피합니다.

## Machine Readability

패턴 파일은 일반 Markdown으로서 유용하게 유지되어야 합니다. Metadata block은 향후 maintainer가
다음을 할 수 있도록 존재합니다:

- Index 빌드.
- 누락된 field 확인.
- 에이전트에게 패턴 추천.
