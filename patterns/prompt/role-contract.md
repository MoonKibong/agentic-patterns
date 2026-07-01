---
id: role-contract
name: Role Contract
category: prompt
status: draft
applies_to:
  - coding agents
  - multi-agent workflows
  - review
  - delegation
related:
  - context-packet
  - durable-session-state
---

# Role Contract

## Intent

Define an agent role through authority, responsibilities, inputs, outputs, boundaries, and escalation
rules before asking it to act.

## Also Known As

Persona contract, role prompt, delegation contract.

## Problem

Agent prompts often assign a role such as "planner" or "reviewer" without defining what that role is
allowed to decide, what evidence it must produce, or when it should stop. The result is role drift:
planners implement, reviewers rewrite, executors make product decisions, and PM agents hide blockers.

## Context

Use this pattern when work is delegated to a specialized agent, when several agents collaborate, or
when a single agent must switch modes between planning, execution, review, and coordination.

## Forces

- More specific roles reduce ambiguity but can become brittle if over-specified.
- Agents can follow authority boundaries only when those boundaries are explicit.
- Humans need predictable outputs to evaluate agent work.
- Multi-agent workflows fail when agents silently claim each other's responsibilities.

## Solution

Write a compact role contract that includes:

- Mission.
- Authority and non-authority.
- Required inputs.
- Required outputs.
- Interaction rules.
- Escalation triggers.
- Completion criteria.

The contract should describe behavior, not personality.

## Agent Recognition Signals

- The user names a role such as PM, planner, executor, reviewer, analyst, or harness runner.
- A task is being delegated to another agent or session.
- The agent is asked to review, supervise, or coordinate work rather than directly implement.
- Previous attempts showed role drift or unclear ownership.

## Procedure

1. Name the role and its mission.
2. State what the role may decide without asking the user.
3. State what the role must not decide.
4. Define the exact artifacts or response shape it must produce.
5. Define when it should escalate, block, or hand off.
6. Keep the contract close to the task context.

## Outputs

- A reusable role prompt or role section inside a larger prompt.
- Optional role-specific checklists for review, planning, execution, or handoff.

## Stop Conditions

- Stop adding role detail when it no longer changes behavior.
- Escalate if the role needs authority the human has not granted.
- Switch to Durable Session State if role outputs must survive across sessions.

## Example

Synthetic reviewer contract:

```markdown
## Reviewer Role Contract

Mission: review the scoped implementation for correctness, regressions, and missing tests.

Authority:
- You may accept, revise, or block the implementation.
- You may request specific fixes.

Non-authority:
- Do not rewrite the implementation unless explicitly asked.
- Do not expand product scope.

Required output:
- Findings first, severity ordered, with file and line references.
- Verification gaps.
- Verdict: accept, revise, or block.
```

Synthetic planner contract:

```markdown
## Planner Role Contract

Mission: turn the request into a scoped implementation plan.

Authority:
- You may inspect repository files and propose task ordering.
- You may reject a plan if acceptance criteria are not verifiable.

Non-authority:
- Do not edit code.
- Do not decide product scope that the user has not specified.

Required output:
- Scope and non-goals.
- Ordered tasks with acceptance criteria.
- Risks and verification plan.
- Blockers requiring user input.
```

## Failure Modes

- The role contract becomes a long persona story instead of operational boundaries.
- The contract grants too much authority and hides user decisions.
- The contract omits required outputs, making review or handoff hard.
- Multiple role contracts conflict.

## Evidence

Sanitized local multi-agent workflows repeatedly benefit from explicit PM, planner, executor,
reviewer, and harness-runner boundaries. The examples are synthetic role contracts intended to show
the public shape of the pattern without exposing private prompts.

## Related Patterns

- [Context Packet](../context/context-packet.md).
- [Durable Session State](../orchestration/durable-session-state.md).
