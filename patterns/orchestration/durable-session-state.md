---
id: durable-session-state
name: Durable Session State
category: orchestration
status: draft
applies_to:
  - multi-agent workflows
  - long-running tasks
  - cross-repo tasks
  - resumable coding sessions
related:
  - context-packet
---

# Durable Session State

## Intent

Keep important agent workflow state in durable artifacts instead of relying only on chat history or
terminal scrollback.

## Also Known As

File-backed state, order ledger, session ledger, persistent handoff.

## Problem

Agentic coding work often spans multiple turns, tools, terminals, agents, and repositories. If state
lives only in chat, it is easy to lose the current plan, accepted scope, review findings, commands
run, or pending user decisions.

## Context

Use this pattern when work is long-running, delegated across agents, resumed later, or coordinated
across repositories.

## Forces

- Chat is fast but ephemeral.
- Durable state adds maintenance overhead but improves resumability and accountability.
- Multi-agent work needs shared truth, not private memory in each agent window.
- State artifacts can become stale if they are not updated when reality changes.

## Solution

Create explicit state artifacts for the workflow. They may be Markdown files, JSON files, SQLite
tables, issues, or another durable store.

At minimum, track:

- Original request and scope.
- Current plan.
- Assignments or roles.
- Handoffs.
- Review findings and verdicts.
- Commands run and verification evidence.
- Open decisions and blockers.
- Final outcome.

The storage format can be simple. The important property is that agents treat it as source of truth.

## Agent Recognition Signals

- The task may continue after context compaction, restart, or interruption.
- More than one agent is involved.
- There are user decisions or review findings that must not be lost.
- Cross-repo sequencing or branch state matters.

## Procedure

1. Create a session directory, issue, database row, or equivalent durable record.
2. Write the original request and current scope.
3. Update plan, handoff, review, and log artifacts when state changes.
4. Make agents read the current state before acting.
5. Close the session with changed files, verification, risks, and next owner.

## Outputs

- Durable state records such as `ORDER.md`, `PLAN.md`, `HANDOFF.md`, `REVIEW.md`, and `LOG.md`.
- Or equivalent database-backed records.

## Stop Conditions

- Stop updating the session when the task is accepted, intentionally parked, or blocked with a clear
  resume trigger.
- Archive or close stale state so future agents do not treat old notes as active truth.

## Example

Synthetic minimal example:

```text
.agentic/session/
├── ORDER.md
├── PLAN.md
├── HANDOFF.md
├── REVIEW.md
└── LOG.md
```

The executor updates `HANDOFF.md` after implementation. The reviewer writes findings to
`REVIEW.md`. The PM closes the session only after verification and review are complete.

Synthetic larger workflow:

```text
session/
├── request.md          # original user request and non-goals
├── plan.md             # accepted task sequence
├── assignments.md      # planner, executor, reviewer, harness runner
├── log.md              # commands run and important observations
├── review.md           # findings and verdict
└── closeout.md         # final state, risks, and next owner
```

The state files are intentionally generic. A private implementation might use Markdown, SQLite,
issues, or another store, but the reusable pattern is that agents read and update shared durable
state before acting.

## Failure Modes

- Agents write decorative state files but continue acting from memory.
- The state model is too heavy for the task.
- Old blockers remain in the file after being resolved.
- Multiple agents update the same file without coordination.

## Evidence

Sanitized local multi-agent workflow practice converged on durable session state after repeated
experience with handoff loss, unclear next actions, and fragile chat-only coordination. The examples
use generic file names and do not reveal private orchestration mechanics.

## Related Patterns

- [Context Packet](../context/context-packet.md).
