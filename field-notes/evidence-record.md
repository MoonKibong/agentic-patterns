---
id: evidence-record
date: 2026-11-15
status: raw
related_patterns: [generate-critique-refine, durable-session-state]
privacy: synthetic
---

# Evidence Record

## Task Shape

A synthetic workflow in which an agent adds behavior to a codebase and must show that its checks
mean something. The question was how to keep passing checks from being vacuous and how to keep old
results from being reused after the code changed.

## Agent Setup

The structure uses roles, not a specific vendor. It applies to any agent that supports skills, MCP
tools, or a harness loop. Claude Code, Codex, and Hermes are examples.

- **Implementer**: writes checks and the code that satisfies them, and runs them.
- **Reviewer**: reads the saved evidence and judges whether it supports the claim.
- **Harness**: runs checks and writes results to a file.

## What Happened

The workflow used these rules:

1. **First failure on its own assertion.** Each new check must first fail on its own assertion, not
   on a setup or compile error, before the implementation makes it pass.
2. **Regression label with a baseline.** A check for behavior that already existed is labelled
   regression. A baseline run against the unchanged code backs it, instead of a first failure.
3. **Per-task evidence file.** Results are saved to a per-task evidence file, so the reviewer reads
   the recorded runs and not the implementer's description of them.
4. **Reuse only for unchanged inputs.** An earlier result is reused only when the final inputs it
   covered are unchanged. Otherwise the check reruns.

## Outcome

The record separated two kinds of checks: new checks that had failed on their own assertion, and
regression checks backed by a baseline run. The reviewer had a file to inspect. Neither kind proves
meaningful coverage: a check that fails on its own assertion can still test the wrong behavior, and
a baseline run only shows the behavior existed. Rerunning on changed inputs cost time. The
distinction between new and regression checks needed a judgment call by the implementer in some
cases.

**When this is overkill.** The move costs more than it returns for documentation-only changes,
where there is no behavior to fail. It also costs too much for checks so cheap that recording them
takes longer than rerunning them, or for throwaway scripts nobody will review.

Not measured: how many vacuous checks the first-failure rule caught, and how much time the
recording and reruns added.

## Emerging Pattern

This note may later support a pattern idea about recorded, falsifiable check evidence. That idea
stays an idea. This note creates no pattern and promotes no pattern.

## Evidence Strength

Single-source observation. It does not show that this move is generally optimal, and it has no
comparison against workflows that do not record check evidence.

## Privacy Notes

The note is synthetic. It was written from scratch to keep the reusable structure. It omits the
originating repository, product and agent names tied to it, clients, cost figures, run identifiers,
issue references, private paths, and prompt text.

## Follow-Up

- Collect repeated observations from independent workflows.
- Compare reviewer accuracy with and without a per-task evidence file.
- Define how to tell a new check from a regression check without judgment.
- Record how often reuse was refused because inputs changed.
