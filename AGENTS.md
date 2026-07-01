# AGENTS.md

This repository is a knowledge base for agentic coding patterns. Treat it as a pattern catalog
and language-design project, not as an application runtime.

## Mission

Help humans and AI agents identify, name, evaluate, and reuse effective patterns for agentic
coding and related human-AI work.

The repository should support four audiences:

- Humans looking for repeatable agentic workflows.
- Contributors writing or refining pattern entries.
- Coding agents selecting a pattern for a task.
- Future maintainers who index, validate, or recommend patterns.

## Operating Principles

- Prefer reusable pattern language over one-off advice.
- Preserve the distinction between observation, inference, and recommendation.
- Describe failure modes and counter-indications as seriously as benefits.
- Make patterns agent-operable: include recognition signals, inputs, steps, outputs, and stop
  conditions.
- Keep pattern files small enough to be used as context by coding agents.
- Do not add a pattern just because it sounds plausible. Record evidence, examples, or at least
  the conditions under which it was observed to work.
- Use concrete examples from real workflows when possible, but remove secrets, private URLs,
  credentials, and project-specific confidential details.
- Prefer synthetic examples that preserve the reusable structure without exposing proprietary
  prompts, private harness logic, customer data, repo names, or workflow transcripts.
- Do not narrow the project to coding. Coding is the first strong domain, but patterns should also
  cover repeated human-guided AI work in image generation, writing, design, video/media, research,
  and analysis.
- Favor pattern composition over giant universal prompts.
- Avoid claiming that a pattern is generally optimal unless the evidence supports that scope.

## Pattern Quality Bar

Every non-draft pattern should answer:

- What recurring problem does it solve?
- In what context does it apply?
- What forces or tradeoffs shape the solution?
- What exact prompt, context, harness, protocol, or tool behavior is reused?
- How does an agent decide to apply it?
- What evidence supports it?
- What are the known failure modes?
- What patterns does it combine with or conflict with?

Use [patterns/_template.md](patterns/_template.md) for new entries.

## Repository Topology

- `docs/`: project framing, pattern language, decisions, and design notes.
- `docs/README.md`: wiki-style documentation home; keep this useful for first-time readers.
- `docs/_sidebar.md`: sidebar-style navigation for humans and future GitHub Wiki or docs tooling.
- `docs/domains/`: domain pages mapping patterns to coding, image generation, writing, design,
  video/media, and research workflows.
- `docs/research/`: trend notes and public-source research summaries.
- `catalog/`: catalog taxonomy and curated indexes.
- `patterns/`: individual pattern entries, grouped by domain.
- `field-notes/`: concrete observations from agentic coding sessions.
- `schemas/`: machine-readable draft schemas for pattern files.
- `.github/`: contribution templates for public GitHub collaboration.

## Editing Rules

- Keep Markdown readable in plain text.
- Use relative links between repository documents.
- When adding major docs or categories, update `docs/README.md` and `docs/_sidebar.md`.
- Prefer short examples over long transcripts.
- Mark draft patterns clearly with `status: draft`.
- Do not introduce generated boilerplate that contributors will have to maintain without purpose.
- Prefer adding field notes when evidence is not yet strong enough to justify a new pattern.
- Field notes must be sanitized before commit. Do not preserve private implementation details just
  because they were useful evidence.
- When changing pattern files, run the repository validation checks if Python 3 is available.

## Review Stance

When reviewing changes, prioritize:

1. Ambiguous or over-broad pattern claims.
2. Missing applicability or stop conditions.
3. Missing failure modes.
4. Examples that cannot actually be followed by a human or agent.
5. Unclear distinction between a pattern, a template, a tool, and a one-off technique.

## Naming

Pattern names should be short, memorable, and operational. Prefer names that describe the reusable
move, such as `Context Packet`, `Reviewer Gate`, or `Durable Session State`, over vague names such
as `Better Prompting`.
