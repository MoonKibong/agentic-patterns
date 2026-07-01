---
id: generate-critique-refine
name: Generate-Critique-Refine
category: harness
status: draft
applies_to:
  - creative generation
  - writing
  - design
  - image generation
  - video generation
domains:
  - image-generation
  - writing
  - design
  - video-media
  - research-analysis
related:
  - creative-brief-packet
---

# Generate-Critique-Refine

## Intent

Generate candidate artifacts, critique them against an explicit rubric, refine the strongest
candidate, and either select, continue, or escalate to a human decision.

## Also Known As

Draft-critique-revise, reflection loop, variation-review loop.

## Problem

Single-pass generation often produces plausible artifacts that miss the actual goal. Creative and
knowledge work also involves taste, tradeoffs, and exploration, so the first output should often be
treated as a candidate rather than a final answer.

## Context

Use this pattern for writing, image generation, design concepts, video scenes, research summaries,
marketing copy, and other workflows where multiple candidates can be compared against a rubric.

## Forces

- More iterations can improve quality but increase cost and drift risk.
- Diverse candidates help exploration but can make selection harder.
- Automated critique is useful, but human taste may be the final authority.
- Without a rubric, refinement can chase arbitrary preferences.

## Solution

Run a bounded loop:

1. Generate several candidates from a brief.
2. Critique each candidate against a rubric.
3. Select one or combine useful parts.
4. Refine only against the critique and brief.
5. Stop, repeat within a budget, or escalate to human review.

The critique should be separate from the generation instruction when the task is high-stakes or
creative taste matters.

## Agent Recognition Signals

- The user asks for options, concepts, drafts, variations, or alternatives.
- The output is subjective but can still be evaluated against criteria.
- The task has cost or quality reasons to review before finalizing.
- A creative brief packet or rubric is available.

## Procedure

1. Read or create the creative brief packet.
2. Set an iteration budget and candidate count.
3. Generate candidates with controlled variation.
4. Critique each candidate using the rubric.
5. Select, combine, or reject candidates.
6. Refine the chosen direction.
7. Report the final artifact plus rationale and remaining risks.

## Outputs

- Candidate artifacts or descriptions.
- Critique table or scored rubric.
- Refined artifact.
- Selection rationale.
- Escalation note if human judgment is required.

## Stop Conditions

- Stop when the candidate satisfies the rubric within the iteration budget.
- Stop when critique repeats the same unresolved issue.
- Escalate when brand, taste, rights, likeness, safety, or budget decisions exceed agent authority.

## Example

Synthetic design example:

```markdown
Brief: create onboarding hero concepts for a focused writing app.

Generate:
- Concept A: quiet desk photo with notebook.
- Concept B: abstract document fragments.
- Concept C: split-screen before/after writing flow.

Critique:
- A best matches calm tone and leaves space for UI copy.
- B is attractive but too generic.
- C explains product value but feels like marketing.

Refine:
- Produce a final prompt based on A with slightly warmer lighting and no visible brand logos.
```

Synthetic research example:

```markdown
Brief: summarize three papers for a non-specialist product team.

Generate:
- Draft summaries.

Critique:
- Check whether each claim has a cited source.
- Flag jargon and missing limitations.

Refine:
- Rewrite for clarity and add a limitations paragraph.
```

## Failure Modes

- The loop runs without a budget.
- Critique invents requirements not present in the brief.
- Refinement loses the best part of the original candidate.
- The agent treats subjective taste as objectively solved.

## Evidence

Public agentic workflow discussions and multimodal generation systems repeatedly use candidate
generation, critique, refinement, and human selection to improve output quality while keeping human
judgment in the loop.

## Related Patterns

- [Creative Brief Packet](../context/creative-brief-packet.md).
