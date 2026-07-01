---
id: context-packet
name: Context Packet
category: context
status: draft
applies_to:
  - coding agents
  - planning
  - implementation
  - review
related:
  - durable-session-state
---

# Context Packet

## Intent

Package the minimum useful task context into a bounded, structured artifact before asking an agent
to plan, implement, or review.

## Also Known As

Context bundle, task packet, handoff packet.

## Problem

Agents often fail because they receive either too little context or an unfiltered dump of everything
near the task. Missing context causes wrong assumptions. Excess context hides the relevant signal and
encourages the agent to optimize for incidental details.

## Context

Use this pattern when a task is non-trivial, crosses files or tools, depends on prior decisions, or
will be handed between agents.

## Forces

- More context increases recall but can reduce focus.
- Humans know the goal and constraints, but agents need those constraints made explicit.
- Chat history is convenient but fragile as a source of truth.
- Handoff quality matters more when planning, implementation, and review happen in separate turns
  or separate agents.

## Solution

Create a short structured context packet that contains only what the next agent role needs:

- Objective.
- Scope and non-goals.
- Relevant files, commands, tools, or external references.
- Constraints and invariants.
- Current state.
- Expected outputs.
- Verification expectations.
- Open questions or known risks.

The packet should be small enough to paste into a model context and durable enough to store as a file.

## Agent Recognition Signals

- The user asks for a multi-step change.
- The task references prior work, hidden assumptions, or a broad codebase.
- More than one agent or session will touch the work.
- The agent is about to summarize, delegate, or resume work.

## Procedure

1. Restate the task objective in one sentence.
2. Identify in-scope and out-of-scope areas.
3. List only the files, docs, commands, and decisions needed for the next step.
4. Add verification expectations.
5. Add unresolved questions only if they affect execution.
6. Store or send the packet before planning or execution begins.

## Outputs

- A Markdown context packet.
- Optional links to source files, plans, issues, or previous handoffs.

## Stop Conditions

- Stop adding context when new details do not change the next action.
- Escalate if a required decision, credential, or environment dependency is missing.
- Switch to Durable Session State if the work spans multiple sessions or agents.

## Example

Synthetic minimal example:

```markdown
## Objective
Add server-side validation for invoice due dates.

## Scope
In scope: API validation and tests.
Out of scope: UI copy changes, database migrations.

## Relevant Files
- `src/invoices/validators.ts`
- `src/invoices/routes.ts`
- `tests/invoices/validation.test.ts`

## Constraints
- Due date cannot be earlier than issue date.
- Existing accepted invoices must not be revalidated.

## Verification
- Run `npm test -- invoices`.
- Add a regression test for same-day due dates.
```

Synthetic handoff example:

```markdown
## Objective
Resume a partially completed refactor of notification delivery.

## Current State
- Email delivery was moved behind `NotificationSender`.
- SMS delivery still calls the provider directly.
- Tests pass for email, but SMS tests have not been updated.

## Scope
In scope: finish SMS migration and update tests.
Out of scope: provider retry policy and UI notification settings.

## Important Constraints
- Preserve existing delivery metrics.
- Do not change public API response shapes.

## Next Agent Output
- Patch summary.
- Tests run.
- Any behavior intentionally left unchanged.
```

## Failure Modes

- The packet becomes a second full specification instead of a compact operational artifact.
- The packet omits the user's real success criteria.
- The packet freezes early assumptions and is not updated after discoveries.

## Evidence

Sanitized local practice repeatedly shows that explicit task packets improve planning, handoff, and
review quality, especially when paired with durable session files. The examples above are synthetic
and preserve the reusable context shape without exposing private project details.

## Related Patterns

- [Durable Session State](../orchestration/durable-session-state.md).
