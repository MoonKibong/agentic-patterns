# Security Policy

Agentic Patterns is primarily a documentation and pattern-language project, but it discusses prompts,
tools, agents, generated artifacts, and workflow practices that can expose private information or
cause unsafe automation when copied blindly.

## Supported Versions

Until the first stable public release, only the latest commit on the default branch is supported.

## What To Report Privately

Do not file a public issue for:

- leaked credentials, private URLs, customer data, or internal repository names
- proprietary prompt, harness, MCP, or workflow details accidentally committed to the repo
- examples that could expose a private implementation or unpublished product strategy
- tool-use guidance that would enable unsafe destructive actions without human approval
- prompt-injection, data-exfiltration, or unsafe-agent recommendations in catalog entries

## Reporting

Report privately to the maintainer or through GitHub private vulnerability reporting once enabled.

Please include:

- affected file or URL
- why the content is sensitive or unsafe
- suggested safe replacement, if available
- whether the issue is already public elsewhere

The maintainer should acknowledge confirmed reports within 7 days and either remove, sanitize, or
replace the affected material.
