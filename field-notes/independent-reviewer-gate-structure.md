---
id: independent-reviewer-gate-structure
date: 2026-11-15
status: raw
related_patterns: [role-contract, generate-critique-refine]
privacy: synthetic
---

# Independent Reviewer Gate Structure

## Task Shape

A synthetic multi-agent coding workflow: an implementer agent changes a codebase, and an
orchestrator must decide whether the change may proceed. The question was how to structure the
review step so its verdict is trustworthy and the loop cannot run forever.

## Agent Setup

The structure uses roles, not a specific vendor. It applies to any agent that supports skills, MCP
tools, or a harness loop. Claude Code, Codex, and Hermes are examples.

- **Implementer**: edits files and runs checks.
- **Reviewer**: a fresh session with no implementer conversation history, read-only, and a
  different agent or instance from the implementer.
- **Orchestrator**: starts the roles, validates the reviewer reply, counts rounds, and escalates.
- **Human**: receives escalations and gives reasons for exceptions.

## What Happened

The workflow used these rules:

1. **Fresh, read-only, different reviewer.** The reviewer starts without the implementer's
   conversation and is told not to edit files. The reviewer is a different agent or instance.
2. **Closed verdict vocabulary.** The reviewer returns exactly one verdict: `accept`, `revise`, or
   `block`, in lowercase. No other word is a verdict.
3. **Mechanical verdict validation.** The orchestrator checks the verdict field with code, not
   judgment. If the field is missing or outside the vocabulary, the orchestrator rejects the reply
   and re-asks the reviewer. Invalid replies count against a separate retry limit; when it is
   reached, the orchestrator stops and escalates to a human.
4. **Revise-round cap.** The orchestrator counts `revise` verdicts. After a fixed number of `revise`
   verdicts, it stops the loop and escalates to a human. The note does not establish a good value
   for either limit; each workflow chose its own.
5. **Same-agent fallback with a recorded reason.** When no different agent is available, the
   orchestrator may let the implementing agent review only if a human gives a reason and the reason
   is recorded.
6. **Honest limit on read-only.** "Read-only" was a detected property, not an enforced one. The
   orchestrator compared working-tree state before and after the review and flagged changes. The
   operating system or sandbox did not prevent writes.

## Outcome

Review verdicts became checkable: a reply was either a valid verdict or it was re-asked. The cap
stopped endless revise loops and moved the decision to a human. The detection-only read-only check
caught a violation only after it happened, so it is weaker than sandbox enforcement. Whether the
structure improves outcomes over a same-agent review stayed unmeasured.

## Emerging Pattern

This note may later support the "Reviewer Gate" pattern idea (listed under Pattern Ideas in the
prompt category). That idea stays an idea. This note does not create or promote a pattern.

## Evidence Strength

Single-source observation. It does not show that this structure is generally optimal, and it has no
comparison against other review structures.

## Privacy Notes

The note is synthetic. It was written from scratch to keep the reusable structure. It omits the
originating repository, product and agent names tied to it, clients, cost figures, run identifiers,
issue references, private paths, and prompt text.

## Follow-Up

- Collect repeated observations from independent workflows.
- Compare against same-agent review on the same tasks.
- Test whether OS-level or sandbox enforcement of read-only changes results versus detection.
- Record how many `revise` rounds are useful before escalation.
