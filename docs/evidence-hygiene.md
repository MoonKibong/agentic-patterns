# Evidence Hygiene

Agentic Patterns should be useful without exposing proprietary solution details.

The catalog can be grounded in practice while still protecting private prompts, harnesses, repos,
customers, credentials, transcripts, and internal workflow mechanics.

## Rule

Publish the pattern, not the private incident.

Examples should reveal the reusable structure:

- Problem shape.
- Forces and tradeoffs.
- Procedure.
- Expected outputs.
- Failure modes.
- Verification style.

Examples should not reveal private implementation details.

## Safe Evidence Types

- Synthetic examples that preserve the structure of the workflow.
- Sanitized field notes with private identifiers removed.
- Public examples from open source repositories, papers, docs, blog posts, or issue threads.
- Aggregated observations stated without identifying details.

## Do Not Publish

- Customer data.
- Credentials, tokens, or private URLs.
- Private repository names.
- Internal prompt text that is not meant to be public.
- Complete proprietary harness logic.
- Full workflow transcripts from private projects.
- Product direction, business strategy, or unreleased implementation details.

## How To Sanitize A Field Note

1. Replace project names with generic names such as `web app`, `API service`, or `agent runner`.
2. Replace file paths with representative paths such as `src/billing/service.ts`.
3. Remove credentials, hostnames, private issue numbers, and private branch names.
4. Summarize transcripts instead of quoting them.
5. Keep the pattern-relevant failure or success condition.
6. Add a note that the example is synthetic or sanitized.

## Synthetic Example Policy

Synthetic examples are encouraged. They should be realistic enough to guide action, but they do not
need to correspond to an actual private workflow.

A good synthetic example:

- Has concrete files, roles, or commands.
- Exercises the pattern's forces.
- Shows what the agent should output.
- Avoids project-specific secrets.

Bad synthetic examples are too vague to execute, such as "make the code better" or "use a better
prompt."
