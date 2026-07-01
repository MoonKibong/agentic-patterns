---
id: creative-brief-packet
name: Creative Brief Packet
category: context
status: draft
applies_to:
  - image generation
  - writing
  - design generation
  - video generation
domains:
  - image-generation
  - writing
  - design
  - video-media
related:
  - context-packet
  - generate-critique-refine
---

# Creative Brief Packet

## Intent

Package creative intent, constraints, references, deliverables, and evaluation criteria into a
bounded brief before asking an AI system or agent to generate artifacts.

## Also Known As

Creative packet, art brief, generation brief, content brief.

## Problem

Creative generation often fails when the model receives only a loose prompt. The output may be
technically impressive but misaligned with audience, tone, style, format, continuity, brand, or
human taste. Dumping many references into context can also blur the actual creative direction.

## Context

Use this pattern when generating or iterating on images, writing, layouts, video scenes, marketing
copy, product concepts, story worlds, or other creative artifacts where intent and constraints matter.

## Forces

- Creative freedom is useful, but uncontrolled variation can break continuity.
- References help, but too many references can produce incoherent hybrids.
- Human taste is hard to automate, so the brief must expose where judgment is needed.
- Different tools need different formats, but the same core creative constraints recur.

## Solution

Create a compact creative brief packet with:

- Objective and audience.
- Desired artifact type and format.
- Style, tone, mood, or aesthetic direction.
- Reference materials and how to use them.
- Hard constraints and prohibited elements.
- Continuity anchors such as characters, world rules, palette, voice, layout, or seed notes.
- Evaluation rubric.
- Human approval points.

The packet should be synthetic or sanitized when derived from private work.

## Agent Recognition Signals

- The user asks for image, design, writing, video, brand, narrative, or media generation.
- The task needs consistency across multiple outputs.
- The task includes references, style constraints, audience constraints, or approval gates.
- The agent is about to run a generate-critique-refine loop.

## Procedure

1. State the creative objective and intended audience.
2. Define the output format and deliverables.
3. Record style, tone, mood, and reference constraints.
4. Add continuity anchors that must persist across variations.
5. Define the review rubric and human approval points.
6. Use the brief as the source of truth for generation and critique.

## Outputs

- A reusable creative brief packet.
- Optional reference list, style board, storyboard, outline, or asset index.

## Stop Conditions

- Stop expanding the brief when new details no longer affect generation or evaluation.
- Escalate when taste, brand, legal, likeness, copyright, or audience decisions are unresolved.
- Switch to Durable Session State if the work spans multiple sessions or many artifacts.

## Example

Synthetic image-generation brief:

```markdown
## Objective
Generate three concept images for a quiet productivity app onboarding screen.

## Audience
Independent professionals who prefer calm, practical tools.

## Format
- 16:9 image concepts.
- No text inside the image.

## Style
- Clean editorial photography feel.
- Natural light, soft contrast, restrained color.
- Avoid cartoon, fantasy, neon, and exaggerated gradients.

## Continuity Anchors
- Same desk, notebook, and laptop across all variations.
- Palette: charcoal, off-white, muted green accent.

## Review Rubric
- Communicates focus without looking corporate.
- Leaves clear negative space for future UI copy.
- No visible brand logos.
```

Synthetic writing brief:

```markdown
## Objective
Draft a short speculative story opening about a city that archives memories as public maps.

## Voice
Literary but direct. Concrete sensory details. No lore dump.

## Constraints
- 700 to 900 words.
- First person.
- End with a decision, not a twist.

## Review Rubric
- Strong opening image.
- Clear emotional stake.
- World rules implied through action.
```

## Failure Modes

- The brief becomes a vague mood board without operational constraints.
- The brief over-constrains the model and removes useful exploration.
- References are included without saying how they should influence the output.
- Human approval points are omitted, causing expensive or misaligned downstream generation.

## Evidence

Synthetic examples and public creative-tool workflows show the same recurring need: generation
quality improves when intent, constraints, references, and review criteria are separated from a
single overloaded prompt.

## Related Patterns

- [Context Packet](./context-packet.md).
- [Generate-Critique-Refine](../harness/generate-critique-refine.md).
