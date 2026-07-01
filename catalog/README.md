# Catalog

This catalog groups agentic patterns by the reusable move they describe.

## Categories

| Category | Purpose |
| --- | --- |
| [`prompt`](../docs/categories/prompt.md) | Reusable instruction and role structures. |
| [`context`](../docs/categories/context.md) | Bounded context packets, memory summaries, and handoff formats. |
| [`harness`](../docs/categories/harness.md) | Planning, execution, review, verification, and critique loops. |
| [`tool`](../docs/categories/tool.md) | MCP, CLI, shell, and tool-use protocols. |
| [`memory`](../docs/categories/memory.md) | Durable state, knowledge preservation, and retrieval patterns. |
| [`evaluation`](../docs/categories/evaluation.md) | Pattern-quality checks, metrics, and comparison methods. |

## Seed Patterns

| Pattern | Category | Status | Summary |
| --- | --- | --- | --- |
| [Context Packet](../patterns/context/context-packet.md) | context | draft | Bound task context into a compact, purpose-shaped packet. |
| [Creative Brief Packet](../patterns/context/creative-brief-packet.md) | context | draft | Bound creative intent, references, constraints, deliverables, and evaluation criteria. |
| [Generate-Critique-Refine](../patterns/harness/generate-critique-refine.md) | harness | draft | Generate candidates, critique with a rubric, refine, and select or escalate. |
| [Durable Session State](../patterns/orchestration/durable-session-state.md) | orchestration | draft | Keep agent workflow state outside transient chat memory. |
| [Role Contract](../patterns/prompt/role-contract.md) | prompt | draft | Define agent role, authority, boundaries, and outputs. |
| [Tool-Use Contract](../patterns/tool/tool-use-contract.md) | tool | draft | Bound tool use before agents affect files, services, or external state. |

## Catalog Rules

- Every listed pattern must have a file in `patterns/`.
- Draft patterns are allowed, but their uncertainty must be visible.
- Accepted patterns should include evidence and at least one realistic example.
- If a pattern becomes too broad, split it into smaller composable patterns.
