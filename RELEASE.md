# Release Guide

This guide is for maintainers preparing Agentic Patterns for public release.

## Release Policy

Publish the first public release as `v0.1.0` and describe it as a seed catalog. Avoid claiming that
patterns are definitive until they have public evidence, examples, and contributor review.

Use lightweight semantic versioning:

- Patch: typo fixes, link fixes, translation fixes, small clarifications.
- Minor: new patterns, new domain pages, new validation rules, new contribution workflows.
- Major: breaking changes to pattern schema, catalog structure, or licensing terms.

## Pre-Release Checklist

1. Confirm the release is being prepared from a fresh filtered public export, not by making a
   private-history repository public.
2. Confirm `README.md` clearly states the scope and seed-stage status.
3. Confirm `CHANGELOG.md` has release notes.
4. Confirm license files are present and linked from `README.md`.
5. Run the approved public link checks and private-name leak scans against the export.

6. Review [Open Source Readiness](docs/oss/OPEN_SOURCE_READINESS.md).
7. Confirm `docs/i18n/` quick starts are aligned with user-facing README changes.
8. Confirm no proprietary prompts, private harness details, customer data, private URLs, or private
   repo names are present.

## Publishing

1. Move `CHANGELOG.md` entries from `Unreleased` to the release version.
2. Commit the release changes.
3. Tag the commit:

```bash
git tag v0.1.0
```

4. Push branch and tag.
5. Create a GitHub release using the changelog.

## Rollback

If a release exposes private or unsafe material:

1. Remove or sanitize the material immediately.
2. Push a patch release.
3. If needed, delete or replace the GitHub release artifact.
4. Document the incident in a maintainer note without repeating sensitive content.
