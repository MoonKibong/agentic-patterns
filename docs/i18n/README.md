# Localized Quick Starts

These quick starts and localized wiki pages summarize Agentic Patterns in multiple languages. The
English README and docs remain the source of truth for full details.

Each localized quick start should explain:

- what Agentic Patterns is
- why it exists
- the core pattern categories
- how to browse the catalog
- how to contribute safely without leaking proprietary details

## Languages

| Language | Pack Entry | Quick Start |
| --- | --- |
| English | [en/README.md](en/README.md) | [en.md](en.md) |
| Korean | [ko/README.md](ko/README.md) | [ko.md](ko.md) |
| Japanese | [ja/README.md](ja/README.md) | [ja.md](ja.md) |
| Chinese (Simplified) | [zh/README.md](zh/README.md) | [zh.md](zh.md) |
| Spanish | [es/README.md](es/README.md) | [es.md](es.md) |
| French | [fr/README.md](fr/README.md) | [fr.md](fr.md) |

## Full Wiki Mirrors

| Language | Status | Entry |
| --- | --- | --- |
| Korean | Complete for current `docs/` user-facing wiki pages | [ko/README.md](ko/README.md) |

See [COVERAGE.md](COVERAGE.md) for the maintained i18n coverage matrix.

## Language Pack Contract

Every language pack must have:

- a stable entry page at `docs/i18n/<lang>/README.md`
- a quick-start page at `docs/i18n/<lang>.md`
- working links to the canonical catalog and core patterns

A complete wiki mirror must also reproduce every user-facing English source file under `docs/`,
excluding `docs/i18n/`, and every root-level user-facing project guide approved for public release.
Links inside a complete mirror should prefer the localized page when that page exists.

Review localized links after changing i18n docs.

## Contributor Rule

When changing user-facing docs, pattern categories, privacy/evidence rules, or contribution
workflow, update every localized file in this directory. If a change does not affect translated
docs, say so in the pull request.
