# Coding

Coding is the seed domain for Agentic Patterns because it exposes clear artifacts: repositories,
files, tests, shells, issues, pull requests, CI, and review verdicts.

## Common Forces

- Agents need enough repository context without drowning in irrelevant files.
- Tool use can mutate local or remote state.
- Review and tests can catch defects, but only when made part of the workflow.
- Long-running tasks need durable state and resumable handoffs.

## Useful Patterns

- [Context Packet](../../patterns/context/context-packet.md)
- [Role Contract](../../patterns/prompt/role-contract.md)
- [Tool-Use Contract](../../patterns/tool/tool-use-contract.md)
- [Durable Session State](../../patterns/orchestration/durable-session-state.md)

## Candidate Patterns

- Human Approval Gate.
- Guardian Gate.
- Provenance Ledger.
- Verification Ladder.
- Context Compactor.
