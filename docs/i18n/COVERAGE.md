# i18n Coverage

English source files remain the source of truth. Localized files should preserve the same structure,
links, warnings, and evidence/privacy meaning even when the wording is adapted for the target
language.

## Coverage Matrix

| Source area | Korean | Japanese | Chinese | Spanish | French |
| --- | --- | --- | --- | --- | --- |
| Language pack entry page | Complete | Complete | Complete | Complete | Complete |
| Quick start | Complete | Complete | Complete | Complete | Complete |
| Root contribution guide | Complete | Not started | Not started | Not started | Not started |
| Wiki home and sidebar | Complete | Not started | Not started | Not started | Not started |
| Category pages | Complete | Not started | Not started | Not started | Not started |
| Domain pages | Complete | Not started | Not started | Not started | Not started |
| Project / pattern language docs | Complete | Not started | Not started | Not started | Not started |
| Evidence / licensing / roadmap | Complete | Not started | Not started | Not started | Not started |
| Research note | Complete | Not started | Not started | Not started | Not started |
| OSS / distribution docs | Complete | Not started | Not started | Not started | Not started |
| Foundations | Complete | Not started | Not started | Not started | Not started |

## Translation Rules

- Preserve file names and heading structure when possible.
- Preserve links, code spans, command names, pattern IDs, category IDs, and license names.
- Do not translate private or synthetic examples into real private examples.
- Keep "Evidence Hygiene" meaning intact in every language.
- If a source change affects user-facing meaning, update the localized mirror in the same PR or mark
  the gap here.

## Current Complete Mirror

- [Korean wiki mirror](ko/README.md)
