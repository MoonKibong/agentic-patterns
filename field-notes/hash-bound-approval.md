---
id: hash-bound-approval
date: 2026-11-15
status: raw
related_patterns: [tool-use-contract, durable-session-state]
privacy: synthetic
---

# Hash-Bound Approval

## Task Shape

A synthetic workflow in which an agent prepares a change and a person must approve it before the
workflow continues. The question was how to make sure the person's "yes" applies to exactly what
they were shown, and not to a later version of it.

## Agent Setup

The structure uses roles, not a specific vendor. It applies to any agent that supports skills, MCP
tools, or a harness loop. Claude Code, Codex, and Hermes are examples.

- **Agent**: prepares the item and runs the checks.
- **Approval gate**: a tool or harness step that stores the pending question and records the answer.
- **Human**: reads the question and answers it.

## What Happened

The workflow used these rules:

1. **Approval binds to the content shown.** When the gate asks, it records a content hash of every
   checked file, plus the identity of the approver and the identity of the item. The answer applies
   to those hashes only.
2. **Change invalidates the pending question.** If any checked file or either identity changes
   before the human answers, the gate invalidates the pending question. All checks rerun before the
   question is asked again.
3. **A repeated request is not approval.** If the agent requests approval again and nothing
   changed, the gate asks the same question again with the same hashes. The repeated request is
   never counted as an answer.
4. **Recheck after the answer.** After the human answers, the checks run again. The approval is
   recorded only if the hashes still match.

## Outcome

The approval record could be compared with the current files, so a stale "yes" was detectable
instead of silently carried forward. The cost was extra check runs and occasional re-asking.

**When this is overkill.** The move costs more than it returns for single-author throwaway work,
where the approver and the author are the same person in the same sitting. It also adds little when
the content cannot change between showing and answering, such as a read-only snapshot, or when a
wrong approval is cheap to undo.

Not measured: how often content actually changed during a pending question, how many wrong
approvals this prevented, and how much time the reruns cost.

## Emerging Pattern

This note may later support a pattern idea about binding human approval to content identity. That
idea stays an idea. This note creates no pattern and promotes no pattern.

## Evidence Strength

Single-source observation. It does not show that this move is generally optimal, and it has no
comparison against approvals that are not bound to content.

## Privacy Notes

The note is synthetic. It was written from scratch to keep the reusable structure. It omits the
originating repository, product and agent names tied to it, clients, cost figures, run identifiers,
issue references, private paths, and prompt text.

## Follow-Up

- Collect repeated observations from independent workflows.
- Compare against approvals that are not bound to content on the same tasks.
- Record how often the invalidation path fires in practice.
- Decide which identities and files belong in the bound set.
