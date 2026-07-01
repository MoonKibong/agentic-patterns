# Open Source Readiness

This document records recommended public-release defaults for Agentic Patterns.

## Task Evaluation

Verdict: `REVISE` until licensing is finalized and translated quick starts have a human review pass.

Scope: repository docs, pattern catalog, GitHub templates, i18n, contribution workflow, and public
positioning.

Primary risk: the project is inspired by real agentic workflows, so public docs must avoid exposing
proprietary prompts, private harness details, customer data, private repo names, and internal
workflow transcripts.

## Positioning

Best call: present Agentic Patterns as a pattern language for human-guided AI work, not as a prompt
collection. Coding is the first mature domain, but the catalog also covers image generation, writing,
design, video/media, research, and analysis.

## License

Current decision:

- Documentation, pattern catalog, prompts, and field notes: CC BY 4.0.
- Code, schemas, and approved software artifacts: MIT.

## Release Stage

Best call: publish the first public release as `v0.1.0` with seed-stage language. Avoid presenting
draft patterns as validated best practices.

## Evidence And Privacy Policy

Best call: require synthetic, sanitized, or explicitly public examples. Treat accidental leakage of
private prompts, customer data, private URLs, or proprietary workflow details as security-sensitive.

## CI

For this Markdown-first public repo, CI can start with markdown linting and link checks once public
validators are approved.

## Contributions

Require PRs to include:

- summary of user-visible docs or pattern changes
- verification commands
- evidence/privacy impact
- i18n impact
- links to related issues

## Publishing Checklist

1. Finalize license files.
2. Confirm `README.md`, `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `CHANGELOG.md`, and
   `RELEASE.md` are present.
3. Confirm issue and PR templates exist.
4. Run the approved public review and validation checks.
5. Review `docs/i18n/` quick starts.
6. Search for private terms, private URLs, credentials, and internal repo names.
7. Create a GitHub release with seed-stage language.

## Decision Checklist

| Item | Best call | Status |
| --- | --- | --- |
| Product promise | Pattern language for human-guided AI work | Documented |
| License | CC BY 4.0 docs + MIT code | Present |
| README | Scope, catalog, validation, evidence hygiene | Present |
| Changelog | Keep a Changelog style with `Unreleased` | Present |
| Contributing | Pattern, evidence, i18n expectations | Present |
| Security | Private leakage and unsafe automation reports | Present |
| Code of conduct | Lightweight maintainer-enforced policy | Present |
| Issue templates | Pattern proposal present; more templates recommended | Partial |
| PR template | Summary, validation, i18n, privacy impact | Present |
| CI | Public markdown/link checks | Not yet present |
| Release process | Seed `v0.1.0` checklist | Present |

## Acceptance Criteria

- Public docs explain what the project is and what it is not.
- Maintainers have release and rollback instructions.
- Contributors have setup, validation, pattern, privacy, and i18n expectations.
- Localized quick starts exist and state that English docs remain the source of truth.
- No proprietary solution details are required to understand or contribute patterns.
