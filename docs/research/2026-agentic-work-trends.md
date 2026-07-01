# 2026 Agentic Work Trends

This note summarizes recent public signals around agentic coding and adjacent creative workflows. It
uses Gemini's research output as an intake, but only records claims here when they are safe, useful,
and either verified from public sources or clearly framed as research leads.

## Executive Summary

Agentic coding is becoming the most concrete early pattern library for human-guided AI work:
repositories, shells, tests, code review, sandboxes, and pull requests make context and verification
visible. The same primitives are appearing in image generation, writing, design, video/media, and
research workflows:

- bounded context packets and briefs
- role-specific agents or subagents
- tool-use protocols
- generate-critique-refine loops
- plan-execute-verify-review loops
- durable state and handoff artifacts
- provenance and citation tracking
- human approval gates
- safety and governance wrappers

The catalog should therefore stay organized around reusable primitives, while domain pages show how
those primitives apply to coding, image generation, writing, design, video/media, and research.

## Verified Source Notes

| Source | Date | Relevance |
| --- | --- | --- |
| [OpenAI, Introducing Codex](https://openai.com/index/introducing-codex/) | 2025 | Codex presents cloud-task execution for software engineering, reinforcing sandboxed task delegation, repo context, test execution, and PR-style workflows. |
| [OpenAI Agents SDK Docs](https://openai.github.io/openai-agents-python/) | 2025-2026 | Documents agents, handoffs, guardrails, tracing, and tools as first-class primitives. |
| [Anthropic Claude Code Subagents](https://docs.anthropic.com/en/docs/claude-code/sub-agents) | 2025-2026 | Describes task-specific subagents with separate context windows, custom prompts, and tool permissions. |
| [Anthropic Claude Code Hooks](https://docs.anthropic.com/en/docs/claude-code/hooks) | 2025-2026 | Shows deterministic control points around agent behavior, useful for approval gates and tool governance. |
| [Model Context Protocol Introduction](https://modelcontextprotocol.io/introduction) | 2025-2026 | Frames MCP as a standard way for applications to expose tools and context to language models. |
| [Google A2A Protocol](https://developers.googleblog.com/en/a2a-a-new-era-of-agent-interoperability/) | 2025 | Shows growing interest in agent-to-agent interoperability and delegation. |
| [arXiv: The 2025 AI Agent Index](https://arxiv.org/abs/2602.17753) | 2026 | Surveys AI agent systems and reinforces the need for evaluating agent capabilities and deployment patterns. |
| [arXiv: VideoAgent](https://arxiv.org/abs/2606.23327) | 2026 | Demonstrates agentic decomposition for video editing workflows. |
| [HKUDS ViMax](https://github.com/HKUDS/ViMax) | 2026 | Public repository for agentic video generation from text/story inputs, useful as a research lead for media pipelines. |

## Trend: Context Engineering Becomes A Product Surface

Agentic systems increasingly treat context as structured input rather than chat history. Coding
agents use repository files, instructions, issue text, tests, and environment state. Creative
systems need equivalent briefs: references, style constraints, continuity anchors, audience,
deliverables, and evaluation criteria.

Catalog impact:

- Keep [Context Packet](../../patterns/context/context-packet.md) as the general pattern.
- Add [Creative Brief Packet](../../patterns/context/creative-brief-packet.md) for creative domains.
- Consider future `Reference Board`, `Source Ledger`, and `Context Compactor` patterns.

## Trend: Agents Are Wrapped In Harnesses

The important shift is not only stronger models. Useful systems wrap models with planning,
execution, critique, verification, guardrails, tracing, and approval gates. In coding this appears as
plan-execute-test-review. In creative work it appears as brief-generate-critique-refine-select.

Catalog impact:

- Keep explicit review and verification loops for software and other verifiable work.
- Add [Generate-Critique-Refine](../../patterns/harness/generate-critique-refine.md) for creative and
  exploratory work.
- Add future `Rubric Review`, `Human Approval Gate`, and `Guardian Gate` patterns.

## Trend: Tool Protocols And Agent Interoperability Matter

MCP and agent-to-agent protocols show that agentic workflows increasingly depend on explicit
capability boundaries. Tools and external systems must be discoverable, bounded, audited, and safe to
use.

Catalog impact:

- Keep [Tool-Use Contract](../../patterns/tool/tool-use-contract.md).
- Add future `Capability Manifest`, `Approval Boundary`, and `Sandbox Gate` patterns.

## Trend: Creative Work Needs Artifact Lifecycle Patterns

Image, writing, design, and video workflows generate intermediate artifacts: briefs, references,
outlines, style boards, candidate images, storyboards, scene plans, critique tables, and final assets.
Those artifacts need handoff, provenance, versioning, and human approval.

Catalog impact:

- Add domain pages rather than splitting the core catalog too early.
- Add future `Artifact Handoff`, `Provenance Ledger`, `Variation Ladder`, `Style Lock`, and
  `Continuity Ledger` patterns.

## Source Hygiene

Gemini's research output included useful leads, but this repository should not treat generated
citations as verified by default. For public documentation:

- prefer primary sources and official docs
- mark unverified items as leads
- do not cite private workflows
- use synthetic examples when public evidence would reveal proprietary methods
