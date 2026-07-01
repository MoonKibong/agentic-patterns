# Agentic Patterns

**A pattern language for human-guided AI work.**

Agentic Patterns is an open knowledge project for reusable prompts, context structures,
harnesses, role contracts, and operating protocols that help humans direct AI agents toward better
outcomes.

The working title is intentionally short:

> **Agentic Patterns: A Pattern Language for Human-Guided AI Work**

The subtitle can carry the practical scope:

> Reusable prompts, context, and harnesses for repeated agentic work.

## Motivation

After months of vibe coding and agentic coding practice, many of us keep returning to the
same questions:

- What prompt shape works for this class of task?
- What context does the agent need, and what context only distracts it?
- When should work be wrapped in a planning, execution, review, or test harness?
- How do we know whether a workflow is effective, efficient, and repeatable?

The premise of this project is that strong answers often become patterns.

Like software design patterns, agentic patterns give names to repeatable solutions. They help
people communicate about recurring problems, compare approaches, and transfer hard-won practice
without forcing everyone to rediscover the same workflow from scratch.

Patterns are also memetic. Human culture is built from transmissible patterns: rituals,
recipes, stories, protocols, tools, and languages. AI systems are powerful pattern matchers, but
humans remain the source of goals, taste, abstraction, memory, and judgment. This project is for
making those human capabilities more legible and reusable when working with AI agents.

## Objectives

1. Build a catalog of agentic patterns covering reusable prompts, context structures, harnesses,
   role contracts, memory practices, and tool-use protocols.
2. Define a pattern language for each catalog area, inspired by software design patterns but
   adapted to agentic coding environments.
3. Provide agent-readable pattern documents so agents such as Claude Code, Codex, Gemini, and
   future coding agents can reason about useful patterns for a task.
4. Create an open contribution space where better practitioners can add, critique, test, and
   refine a shared body of knowledge.

## What Counts As A Pattern?

An agentic pattern is a named, reusable solution to a recurring problem in human-AI work.

It should describe:

- The situation where it applies.
- The forces and tradeoffs that make the problem non-trivial.
- The context, prompt, harness, role, or protocol to use.
- Evidence that the pattern works, including known failure modes.
- How an agent can recognize when to apply or avoid it.

Good patterns are not magic prompts. They are compact operational knowledge.

## Repository Map

```text
.
├── AGENTS.md                         # Instructions for AI agents working in this repo
├── CONTRIBUTING.md                   # Human contribution guide
├── field-notes/                      # Observations from real agentic work
├── catalog/README.md                 # Catalog taxonomy and index
├── docs/
│   ├── README.md                     # Wiki-style documentation home
│   ├── _sidebar.md                   # Wiki-style navigation sidebar
│   ├── categories/                   # Category landing pages
│   ├── domains/                      # Domain landing pages
│   ├── foundations/                  # Pattern-language background and motivation
│   ├── research/                     # Trend research and source notes
│   ├── project-brief.md              # Refined project framing and naming notes
│   ├── evidence-hygiene.md           # How to use examples without leaking private work
│   ├── licensing.md                  # License options and recommendation
│   ├── pattern-language.md           # Pattern entry structure and quality bar
│   └── roadmap.md                    # Seed-stage roadmap
├── patterns/
│   ├── _template.md                  # Canonical pattern template
│   ├── context/creative-brief-packet.md
│   ├── context/context-packet.md
│   ├── harness/generate-critique-refine.md
│   ├── orchestration/durable-session-state.md
│   ├── prompt/role-contract.md
│   └── tool/tool-use-contract.md
└── schemas/pattern.schema.json       # Draft machine-readable pattern schema
```

## Browse The Docs

Start with the [documentation home](docs/README.md). It provides wiki-style navigation by audience,
task, and pattern category.

Localized quick starts are available in [docs/i18n/](docs/i18n/).

## Starter Catalog

- [Context Packet](patterns/context/context-packet.md): provide bounded, task-shaped context
  instead of dumping everything into the agent window.
- [Creative Brief Packet](patterns/context/creative-brief-packet.md): package creative intent,
  constraints, references, deliverables, and evaluation criteria for generative work.
- [Generate-Critique-Refine](patterns/harness/generate-critique-refine.md): generate candidates,
  critique against a rubric, refine, and select or escalate.
- [Durable Session State](patterns/orchestration/durable-session-state.md): keep multi-agent
  work state in files or a database rather than relying on chat memory.
- [Role Contract](patterns/prompt/role-contract.md): define an agent role through authority,
  inputs, outputs, boundaries, and escalation rules.
- [Tool-Use Contract](patterns/tool/tool-use-contract.md): make tool use explicit, observable,
  and bounded before an agent acts through shell, browser, MCP, or external services.

## Validate

Before publication, maintainers run a private review and validation workflow. Public readers do not
need local tooling to use the wiki.

## Use With An Agent

Use the pattern files as a public language for planning, reviewing, and discussing human-guided AI
work. Agent-specific command surfaces and executable pattern-selection tools are maintained
separately.

## Scope

The seed catalog started from agentic coding, but the project scope is broader: repeated
human-guided AI work where context, prompts, tools, loops, memory, and review can be named and
reused. See [Agentic Work Trends](docs/research/2026-agentic-work-trends.md) and the domain pages
for [coding](docs/domains/coding.md), [image generation](docs/domains/image-generation.md),
[writing](docs/domains/writing.md), [design](docs/domains/design.md), and
[video/media](docs/domains/video-media.md).

## Evidence Hygiene

Pattern examples should be synthetic, sanitized, or explicitly public. Do not include proprietary
prompts, private harness details, customer data, credentials, internal repo names, or confidential
workflow transcripts. See [Evidence Hygiene](docs/evidence-hygiene.md).

## Design Influences

This project is inspired by:

- [Christopher Alexander's pattern language tradition](docs/foundations/pattern-language-roots.md).
- The Gang of Four design-pattern catalog format.
- Prompt-pattern catalogs from prompt engineering research and practice.
- Practical agent workflow experiments with context packets, roles, tools, durable state, and review
  loops.

## Status

This repository is in seed stage. The first goal is to collect a small number of high-quality
patterns with clear applicability, examples, and failure modes before expanding the catalog.

## License

Agentic Patterns uses a split license. See [LICENSE](LICENSE) and
[docs/licensing.md](docs/licensing.md).

- Documentation and pattern catalog: Creative Commons Attribution 4.0.
- Code and schemas: MIT.
