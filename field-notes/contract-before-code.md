---
id: contract-before-code
date: 2026-11-15
status: raw
related_patterns: [context-packet, role-contract, durable-session-state]
privacy: synthetic
---

# Contract Before Code

## Task Shape

A synthetic workflow in which an agent implements tasks derived from an approved requirements
document. The question was how to stop implementation from starting on a task whose scope nobody
had agreed, or whose scope came from requirements that later changed.

## Agent Setup

The structure uses roles, not a specific vendor. It applies to any agent that supports skills, MCP
tools, or a harness loop. Claude Code, Codex, and Hermes are examples.

- **Contract author**: an agent that drafts the task contract from the requirements.
- **Implementer**: an agent that writes code, only after the start check passes.
- **Human**: reviews and approves the task contract.
- **Start check**: a harness step that looks for an approved contract before implementation.

## What Happened

The workflow used these rules:

1. **Contract first, approved by a person.** Before any implementation, the contract author writes
   a task contract (scope, acceptance checks, exclusions). A person approves it.
2. **Bound to a requirements version.** The contract records the specific approved requirements
   version it was written against.
3. **No contract, no start.** The start check refuses to begin implementation when no approved
   contract exists for the task. The refusal names the missing contract.
4. **A new requirements version makes the contract stale.** When the requirements version changes,
   the contract is stale. It must be revised and approved again before implementation continues.

How the approval itself is bound to content is a separate move; see
[Hash-Bound Approval](hash-bound-approval.md).

## Outcome

Implementation could not begin from an unapproved or outdated scope, and the refusal gave the
implementer a concrete next step. The cost was one extra document and one extra approval per task.

**When this is overkill.** The move costs more than it returns for exploratory spikes, where the
goal is to learn what the scope should be. It is also heavy for one-line fixes, and it has nothing
to bind to when the work has no separate requirements document.

Not measured: how many scope errors the contract caught, how often a requirements change made a
contract stale, and the time spent writing contracts.

## Emerging Pattern

This note may later support a pattern idea about gating implementation on an approved task
contract. That idea stays an idea. This note creates no pattern and promotes no pattern.

## Evidence Strength

Single-source observation. It does not show that this move is generally optimal, and it has no
comparison against starting implementation directly from the requirements.

## Privacy Notes

The note is synthetic. It was written from scratch to keep the reusable structure. It omits the
originating repository, product and agent names tied to it, clients, cost figures, run identifiers,
issue references, private paths, and prompt text.

## Follow-Up

- Collect repeated observations from independent workflows.
- Compare against implementation started directly from requirements.
- Record how stale contracts were detected and how long re-approval took.
- Test whether a lighter contract works for small tasks.
