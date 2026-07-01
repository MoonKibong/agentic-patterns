# Contributing

Agentic Patterns is intended to become a shared catalog of reusable practice. Contributions should
make repeated human-AI work easier to recognize, discuss, and execute.

## Ways To Contribute

- Add a new pattern using [patterns/_template.md](patterns/_template.md).
- Improve an existing pattern's examples, applicability, or failure modes.
- Add field notes from real agentic coding sessions.
- Build tools that validate, index, recommend, or package patterns for agents.
- Propose better catalog taxonomy.

## Before Adding A Pattern

Ask whether the entry is really a pattern:

- Does it solve a recurring problem?
- Can another person apply it in a similar situation?
- Are the tradeoffs visible?
- Can an agent recognize when to use it?
- Is there at least some evidence or concrete experience behind it?

If the answer is not yet clear, add a field note or draft pattern instead of presenting it as
established.

## Field Notes

Use [field-notes/_template.md](field-notes/_template.md) when an observation is useful but not yet
stable enough to become a pattern.

Good field notes record:

- The task shape.
- The agent setup.
- What happened.
- What improved or failed.
- Which pattern may be emerging.
- What evidence would make the pattern stronger.

## Evidence Hygiene

Do not contribute proprietary solution details. Pattern evidence should be one of:

- Synthetic examples that preserve the structure of the problem.
- Sanitized field notes with private details removed.
- Public examples from open repositories, papers, blog posts, or issue threads.
- Generalized observations stated without private identifiers.

Never include customer data, credentials, private URLs, private repo names, internal prompt text, or
complete proprietary workflow transcripts.

## Pattern Entry Process

1. Copy `patterns/_template.md` into the relevant category directory.
2. Fill in the metadata block.
3. Write the pattern in operational terms.
4. Include at least one example.
5. Include known failure modes and counter-indications.
6. Link related patterns.
7. Update [catalog/README.md](catalog/README.md).

## Localized Documentation

The localized quick starts in [docs/i18n/](docs/i18n/) are public entry points. When changing the
project description, core categories, safety/privacy language, or contribution workflow, update the
localized quick starts or state in the pull request why no translation update is needed.

If you cannot confidently update a language, keep the English source change small and ask for
translation review.

## Evidence Standard

Evidence can be lightweight at first, but it should be honest.

Useful evidence includes:

- A repeated workflow observed across multiple tasks.
- A before/after comparison.
- A transcript excerpt or summarized incident.
- A test result, review result, or defect avoided.
- A local convention that survived repeated use.

Avoid vague claims such as "works better" without explaining what improved.

## Tone

Write for capable humans and capable agents. Be direct, specific, and humble about uncertainty.

This project should not become a list of inspirational prompt tricks. It should become a practical
pattern language.
