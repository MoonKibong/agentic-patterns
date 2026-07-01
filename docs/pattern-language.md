# Pattern Language

This document defines the structure and quality bar for Agentic Patterns entries.

## Definition

An agentic pattern is a named, reusable solution to a recurring problem in human-AI work.

Patterns may describe:

- Prompt structures.
- Context structures.
- Planning or execution harnesses.
- Review and verification loops.
- Agent role contracts.
- MCP/tool protocols.
- Multi-agent coordination moves.
- Memory and state-management practices.

Patterns are not limited to software engineering. Coding is the first strong domain because it has
visible tests, repositories, tools, and review loops, but the same structure applies to image
generation, writing, design, video/media production, research, analysis, and other repeated
human-guided AI workflows.

## Pattern Metadata

Each pattern should start with a small metadata block:

```yaml
---
id: context-packet
name: Context Packet
category: context
status: draft
applies_to:
  - coding agents
  - planning
  - implementation
domains:
  - coding
related:
  - durable-session-state
---
```

The `id` should be stable, lowercase, and hyphenated. `domains` is optional but recommended. It
describes where the pattern is useful, such as `coding`, `image-generation`, `writing`, `design`,
`video-media`, `research-analysis`, or `general`.

## Pattern Sections

Use these sections unless a pattern has a strong reason to differ.

### Intent

One or two sentences describing the reusable move.

### Also Known As

Optional alternate names.

### Problem

The recurring problem this pattern addresses.

### Context

The situation where the pattern applies. Include preconditions and environmental assumptions.

### Forces

The tensions that make the problem non-trivial. Examples:

- More context can help the agent, but too much context can bury the important signal.
- More autonomy can speed execution, but unbounded autonomy can hide risk.
- More agents can parallelize work, but coordination overhead can exceed the benefit.

### Solution

The reusable structure, protocol, prompt, harness, or tool behavior.

### Agent Recognition Signals

Observable signals that should cause an agent to consider the pattern.

### Procedure

Concrete steps a human or agent can follow.

### Outputs

Artifacts the pattern should produce.

### Stop Conditions

When to stop applying the pattern, escalate, or switch patterns.

### Example

A compact realistic example. Synthetic examples are preferred when a real workflow could reveal
private implementation, customer, prompt, or orchestration details.

### Failure Modes

Known ways the pattern can go wrong.

### Evidence

Observed results, field notes, tests, review outcomes, or other support.

Evidence should be safe to publish. Use sanitized summaries, synthetic reproductions, or public
sources. Do not expose private prompts, proprietary harness logic, customer data, private repository
names, credentials, or complete internal transcripts.

### Related Patterns

Patterns that compose with, replace, or conflict with this one.

## Pattern Status

- `draft`: promising but not yet stabilized.
- `candidate`: used successfully more than once and ready for review.
- `accepted`: reviewed and considered part of the catalog.
- `deprecated`: kept for historical reference but no longer recommended.

## Categories

Initial categories:

- `prompt`: reusable instruction structures.
- `context`: reusable context packet structures.
- `harness`: staged workflows for planning, execution, review, and verification.
- `orchestration`: multi-agent and multi-session coordination.
- `tool`: MCP, CLI, script, or environment interaction patterns.
- `memory`: durable knowledge and state patterns.
- `evaluation`: ways to judge whether a pattern worked.

Categories can change as the catalog matures.

## Evidence Hygiene

Pattern examples should teach the reusable shape, not disclose the private incident that inspired
the pattern.

Acceptable evidence:

- Synthetic examples that preserve the forces and procedure.
- Sanitized field notes with private identifiers removed.
- Public references from open source repositories, papers, docs, blog posts, or issue threads.
- Aggregated observations such as "observed across several local coding sessions."

Do not include:

- Private repo names, customer names, private URLs, credentials, or logs.
- Full proprietary prompts, harness internals, or MCP/tool protocols.
- Transcripts that reveal unreleased product direction or internal implementation details.

When in doubt, generalize the scenario and keep the pattern operational.

## Naming Rules

Pattern names should be:

- Short.
- Memorable.
- Operational.
- Specific enough to distinguish the move.

Avoid names that merely describe a goal, such as `Better Coding` or `Good Context`.

## Machine Readability

Pattern files should remain useful as normal Markdown. The metadata block exists so future
maintainers can:

- Build indexes.
- Check missing fields.
- Recommend patterns to agents.
