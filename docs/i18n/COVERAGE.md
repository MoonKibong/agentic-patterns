# i18n Coverage

English source files remain the source of truth. Localized files should preserve the same structure,
links, warnings, and evidence/privacy meaning even when the wording is adapted for the target
language.

## Coverage Matrix

| Source area | Korean | Japanese | Chinese | Spanish | French |
| --- | --- | --- | --- | --- | --- |
| Language pack entry page | Complete | Complete | Complete | Complete | Complete |
| Quick start | Complete | Complete | Complete | Complete | Complete |
| Root contribution guide | Complete | Complete | Complete | Complete | Complete |
| Wiki home and sidebar | Complete | Complete | Complete | Complete | Complete |
| Category pages | Complete | Complete | Complete | Complete | Complete |
| Domain pages | Complete | Complete | Complete | Complete | Complete |
| Project / pattern language docs | Complete | Complete | Complete | Complete | Complete |
| Evidence / licensing / roadmap | Complete | Complete | Complete | Complete | Complete |
| Research note | Complete | Complete | Complete | Complete | Complete |
| OSS / distribution docs | Complete | Complete | Complete | Complete | Complete |
| Foundations | Complete | Complete | Complete | Complete | Complete |

## Translation Rules

- Preserve file names and heading structure when possible.
- Preserve links, code spans, command names, pattern IDs, category IDs, and license names.
- Do not translate private or synthetic examples into real private examples.
- Keep "Evidence Hygiene" meaning intact in every language.
- If a source change affects user-facing meaning, update the localized mirror in the same PR or mark
  the gap here.

## Current Complete Mirrors

All five localized wikis are complete, self-contained mirrors of the current `docs/`
user-facing wiki pages. Internal links inside each mirror resolve to same-locale pages;
the only outbound links are the shared English-only source artifacts (`catalog/`,
`patterns/`, `field-notes/`).

- [Korean wiki mirror](ko/README.md)
- [Japanese wiki mirror](ja/README.md)
- [Chinese (Simplified) wiki mirror](zh/README.md)
- [Spanish wiki mirror](es/README.md)
- [French wiki mirror](fr/README.md)
