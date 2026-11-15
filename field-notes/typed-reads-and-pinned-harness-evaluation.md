---
id: typed-reads-and-pinned-harness-evaluation
date: 2026-11-15
status: raw
related_patterns: [tool-use-contract]
privacy: synthetic
---

# Typed Reads And Pinned Harness Evaluation

## Task Shape

A synthetic orchestrated coding workflow, plus an evaluation of that workflow's harness. Two
separate problems appeared: reading agent replies reliably, and comparing harness results over time.

## Agent Setup

The note describes roles, not a specific vendor. It applies to any agent that supports skills, MCP
tools, or a harness loop. Claude Code, Codex, and Hermes are examples.

- **Orchestrator**: reads agent output and decides the next step.
- **Agents**: implement or review work and report back.
- **Evaluator**: runs the harness on a task set and compares results.

## What Happened

**Observation 1: regex over free-text replies.** The orchestrator parsed agent replies with regular
expressions. When agents changed their wording, patterns stopped matching and the orchestrator
misread or missed status. Each fix added another pattern.

**Observation 2: the harness changed during its own evaluation.** While the harness was under
evaluation, it was edited mid-test. Results from before and after the edit came from different
harnesses, so they could not be compared.

## Outcome

Recommendations from the two observations:

- **Use typed reads.** Ask for structured output, or read a typed field or state record, then
  validate it against a closed schema. Reject or re-ask when validation fails. Do not infer state
  from prose.
- **Pin the component under test.** For the whole evaluation run, fix the version or commit of the
  harness, the prompts, and the model. Record which version was pinned. Apply harness changes only
  between runs and treat each as a new run.

Whether these changes reduced misreads or made comparisons reliable was not measured here.

## Emerging Pattern

Possible future pattern ideas: Typed Agent Report (a typed record validated against a closed
schema), and Pinned Evaluation Subject (a fixed, recorded version of the component under test).
This note creates no pattern.

## Evidence Strength

Single-source observation. It does not show that either practice is generally optimal.

## Privacy Notes

The note is synthetic. It was written from scratch to keep the reusable structure. It omits the
originating repository, product and agent names tied to it, clients, cost figures, run identifiers,
issue references, private paths, and prompt text.

## Follow-Up

- Collect repeated observations of wording drift breaking text parsing.
- Compare a typed-read workflow against a regex workflow on the same tasks.
- Observe evaluations that pin and evaluations that do not, and compare result comparability.
- Decide which version fields (harness, prompts, model) are the minimum to record.
