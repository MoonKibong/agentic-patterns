---
id: task-slicing-instead-of-orchestrator
date: 2026-11-15
status: raw
related_patterns: [context-packet, durable-session-state]
privacy: synthetic
---

# Task Slicing Instead Of An Orchestrator

## Task Shape

A synthetic multi-step software project. The question was whether to hand the whole job to a
multi-agent orchestrator or to cut the job into small tasks that one agent session handles at a
time.

## Agent Setup

The structure uses roles, not a specific vendor. It applies to any agent that supports skills, MCP
tools, or a harness loop. Claude Code, Codex, and Hermes are examples.

- **Planner**: a person or agent that cuts the work into tasks and lists prerequisites.
- **Implementer**: one agent session per task.
- **Human**: reorders, splits, and accepts tasks.

## What Happened

The workflow used these rules:

1. **One day or less per task.** Multi-step work is split into tasks sized at one day or less.
2. **Explicit prerequisites and order.** Each task lists its prerequisites. The order is skeleton
   first, then code standards, then features.
3. **Split from the main line.** A task found to be too big is split into smaller tasks. Each
   smaller task restarts from the main line, not from the unfinished work of the big one.
4. **Chosen instead of an orchestrator.** This slicing was chosen instead of delegating the whole
   job to a multi-agent orchestrator.

## Outcome

Each session had a small, checkable scope and a known starting point. The tradeoff: slicing moves
coordination work to the person who orders and splits tasks, while an orchestrator moves it to
software that can run work in parallel. Both have costs, and no comparison was made between them.

**When this is overkill.** The move costs more than it returns when tasks are already smaller than
a day, because the planning overhead exceeds the work. It also fits poorly where an orchestrator's
parallelism is the point, such as many independent tasks that should run at the same time.

Not measured: total elapsed time, rework rate, and how often a split task needed another split.

## Emerging Pattern

This note may later support a pattern idea about sizing and ordering tasks with explicit
prerequisites. That idea stays an idea. This note creates no pattern and promotes no pattern.

## Evidence Strength

Single-source observation. It does not show that this move is generally optimal, and it does not
show that slicing is better or worse than orchestration.

## Privacy Notes

The note is synthetic. It was written from scratch to keep the reusable structure. It omits the
originating repository, product and agent names tied to it, clients, cost figures, run identifiers,
issue references, private paths, and prompt text.

## Follow-Up

- Collect repeated observations from independent workflows.
- Compare against an orchestrated run on the same project.
- Record how often tasks exceeded one day and how they were split.
- Test whether the prerequisite order holds for other project types.
