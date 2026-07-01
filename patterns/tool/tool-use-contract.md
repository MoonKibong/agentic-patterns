---
id: tool-use-contract
name: Tool-Use Contract
category: tool
status: draft
applies_to:
  - coding agents
  - shell tools
  - MCP tools
  - browser automation
  - external services
related:
  - role-contract
  - durable-session-state
---

# Tool-Use Contract

## Intent

Make tool use explicit, bounded, and observable before an agent acts through shell commands, browsers,
MCP servers, APIs, or external services.

## Also Known As

Tool boundary, action contract, capability contract.

## Problem

Tools let agents affect real files, services, money, deployments, credentials, or public state. When
tool boundaries are vague, agents may overreach, skip verification, mutate unrelated files, or hide
important side effects in raw command output.

## Context

Use this pattern when an agent can invoke tools that read or write outside pure text generation:
shell, Git, package managers, browsers, MCP connectors, cloud CLIs, issue trackers, or deployment
systems.

## Forces

- Tool access makes agents useful but increases blast radius.
- Asking for approval on every action slows work, but broad permission can hide risky operations.
- Some commands are exploratory; others are state-changing.
- Humans need a summary of tool effects, not just command transcripts.

## Solution

Define a tool-use contract for the task:

- Allowed tools and purposes.
- Read-only versus write actions.
- Approval triggers.
- Forbidden actions.
- Evidence to report after tool use.
- Cleanup or rollback expectations.

For coding work, the contract should also say how to handle dirty worktrees, external dependencies,
network access, generated files, and destructive commands.

## Agent Recognition Signals

- The task requires shell commands, package installation, browser automation, APIs, or MCP tools.
- The agent is about to write files, install dependencies, push code, open PRs, or change remote state.
- The environment has sandbox or approval rules.
- The user asked for autonomous work but did not define boundaries.

## Procedure

1. Identify tools required for the task.
2. Classify each action as read-only, workspace write, external write, or destructive.
3. State which actions are pre-approved by the task.
4. Request explicit approval for actions outside that boundary.
5. Record important tool results in the final answer or durable session state.
6. Report verification commands and residual risks.

## Outputs

- A concise tool-use policy for the task or repository.
- Command and verification summaries.
- Escalation notes for approvals or blocked actions.

## Stop Conditions

- Stop and ask the user before destructive, credential-sensitive, deployment, billing, or scope
  expansion actions.
- Stop if tool output contradicts the task assumptions.
- Switch to Durable Session State for long-running tool-driven workflows.

## Example

Synthetic minimal example:

```markdown
Allowed:
- Read repository files with `rg`, `sed`, and `git diff`.
- Edit files inside the workspace.
- Run local tests.

Requires approval:
- Installing dependencies.
- Pushing branches or creating releases.
- Deleting files outside generated artifacts.

Forbidden:
- Editing shell startup files for PATH changes; use the configured env file instead.
```

Synthetic external-service example:

```markdown
Allowed:
- Read issue details and existing labels.
- Draft a proposed issue comment.

Requires approval:
- Posting comments.
- Closing issues.
- Changing labels or assignees.

Evidence to report:
- Issue URL.
- Proposed or posted comment summary.
- Any remote state changed.

Forbidden:
- Publishing private logs or credentials.
- Triggering deployments.
```

## Failure Modes

- The contract is so restrictive that the agent cannot complete the task.
- The contract is so broad that it no longer protects the user.
- The agent reports commands but not the effect of those commands.
- Approval rules are scattered across prompts and conflict with repository instructions.

## Evidence

Practical agentic coding environments depend on explicit tool boundaries. Sandbox approvals, shell
environment rules, and Git hygiene instructions are recurring public examples of tool-use contracts.
The examples here are synthetic and avoid private service names or internal approval policies.

## Related Patterns

- [Role Contract](../prompt/role-contract.md).
- [Durable Session State](../orchestration/durable-session-state.md).
