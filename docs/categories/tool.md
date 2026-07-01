# Tool Patterns

Tool patterns define how agents should use shell commands, browsers, MCP servers, APIs, package
managers, Git, and other capabilities that can affect real state.

Use tool patterns when the agent must act through external capabilities and the blast radius needs to
be explicit.

## Current Patterns

- [Tool-Use Contract](../../patterns/tool/tool-use-contract.md): define allowed tools, approval
  triggers, forbidden actions, and evidence expectations.

## Pattern Ideas

- Read-First Tooling.
- Approval Boundary.
- Verification Command.
- External State Guard.

## Related Categories

- [Harness Patterns](harness.md)
- [Prompt Patterns](prompt.md)
- [Evaluation Patterns](evaluation.md)
