# 2026 Agentic Work Trends

이 노트는 agentic coding과 인접한 creative workflow에 대한 공개 신호를 요약합니다. Gemini
research output은 intake로 사용했지만, 이 문서에는 공개적으로 검증 가능하거나 research lead로
명시할 수 있는 내용만 기록합니다.

## Executive Summary

Agentic coding은 human-guided AI work의 초기 pattern library로 가장 구체적인 영역입니다.
Repository, shell, test, code review, sandbox, pull request가 context와 verification을
눈에 보이게 만들기 때문입니다. 같은 primitive는 image generation, writing, design,
video/media, research workflow에도 나타납니다.

- bounded context packet과 brief
- role-specific agent 또는 subagent
- tool-use protocol
- generate-critique-refine loop
- plan-execute-verify-review loop
- durable state와 handoff artifact
- provenance와 citation tracking
- human approval gate
- safety와 governance wrapper

따라서 catalog는 reusable primitive를 중심으로 구성하고, domain page는 그 primitive가 coding,
image generation, writing, design, video/media, research에 어떻게 적용되는지 보여주어야 합니다.

## Verified Source Notes

| Source | Date | Relevance |
| --- | --- | --- |
| [OpenAI, Introducing Codex](https://openai.com/index/introducing-codex/) | 2025 | Sandboxed software task delegation, repo context, test execution, PR-style workflow. |
| [OpenAI Agents SDK Docs](https://openai.github.io/openai-agents-python/) | 2025-2026 | Agents, handoffs, guardrails, tracing, tools. |
| [Anthropic Claude Code Subagents](https://docs.anthropic.com/en/docs/claude-code/sub-agents) | 2025-2026 | Task-specific subagents, separate context windows, custom prompts, tool permissions. |
| [Anthropic Claude Code Hooks](https://docs.anthropic.com/en/docs/claude-code/hooks) | 2025-2026 | Agent behavior around deterministic control points. |
| [Model Context Protocol Introduction](https://modelcontextprotocol.io/introduction) | 2025-2026 | Tools and context exposed to language models through standard protocol. |
| [Google A2A Protocol](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) | 2025 | Agent-to-agent interoperability and delegation. |
| [arXiv: The 2025 AI Agent Index](https://arxiv.org/abs/2602.17753) | 2026 | Agent systems and evaluation/deployment patterns. |
| [arXiv: VideoAgent](https://arxiv.org/abs/2606.23327) | 2026 | Agentic decomposition for video editing workflow. |
| [HKUDS ViMax](https://github.com/HKUDS/ViMax) | 2026 | Agentic video generation research lead. |

## Trend: Context Engineering Becomes A Product Surface

Agentic system은 chat history가 아니라 structured input으로 context를 다루기 시작했습니다.
Coding agent는 repository file, instruction, issue text, test, environment state를 사용합니다.
Creative system에는 reference, style constraint, continuity anchor, audience, deliverable,
evaluation criteria가 필요합니다.

Catalog impact:

- [Context Packet](../../../../patterns/context/context-packet.md)을 general pattern으로 유지합니다.
- Creative domain에는 [Creative Brief Packet](../../../../patterns/context/creative-brief-packet.md)을 사용합니다.
- Future pattern: `Reference Board`, `Source Ledger`, `Context Compactor`.

## Trend: Agents Are Wrapped In Harnesses

중요한 변화는 model이 강해진 것만이 아니라, model이 planning, execution, critique,
verification, guardrail, tracing, approval gate로 감싸진다는 점입니다. Coding에서는
plan-execute-test-review로, creative work에서는 brief-generate-critique-refine-select로 나타납니다.

Catalog impact:

- Software와 verifiable work에는 explicit verification과 review loop가 필요합니다.
- Creative/exploratory work에는 [Generate-Critique-Refine](../../../../patterns/harness/generate-critique-refine.md).
- Future pattern: `Rubric Review`, `Human Approval Gate`, `Guardian Gate`.

## Trend: Tool Protocols And Agent Interoperability Matter

MCP와 agent-to-agent protocol은 agentic workflow가 explicit capability boundary에 의존한다는
점을 보여줍니다. Tool과 external system은 discoverable, bounded, auditable, safe해야 합니다.

Catalog impact:

- [Tool-Use Contract](../../../../patterns/tool/tool-use-contract.md)을 유지합니다.
- Future pattern: `Capability Manifest`, `Approval Boundary`, `Sandbox Gate`.

## Trend: Creative Work Needs Artifact Lifecycle Patterns

Image, writing, design, video workflow는 brief, reference, outline, style board, candidate image,
storyboard, scene plan, critique table, final asset 같은 intermediate artifact를 생성합니다.
이 artifact에는 handoff, provenance, versioning, human approval이 필요합니다.

Catalog impact:

- Core catalog를 성급하게 쪼개기보다 domain page를 추가합니다.
- Future pattern: `Artifact Handoff`, `Provenance Ledger`, `Variation Ladder`, `Style Lock`,
  `Continuity Ledger`.

## Source Hygiene

Generated citation은 기본적으로 검증된 것으로 취급하지 않습니다.

- Primary source와 official docs를 우선합니다.
- Unverified item은 lead로 표시합니다.
- Private workflow는 citation으로 사용하지 않습니다.
- Proprietary method가 드러날 수 있으면 synthetic example을 사용합니다.
