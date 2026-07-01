# Open Source Readiness

이 문서는 Agentic Patterns의 공개 릴리스 기본값을 기록합니다.

## Task Evaluation

Verdict: `REVISE` until translated quick starts and full wiki mirrors have a human review pass.

Scope: repository docs, pattern catalog, GitHub template, i18n, contribution workflow, public
positioning.

Primary risk: 이 프로젝트는 실제 agentic workflow에서 영감을 받았으므로, public docs는
proprietary prompt, private harness detail, customer data, private repo name, internal workflow
transcript를 노출하면 안 됩니다.

## Positioning

Agentic Patterns는 human-guided AI work를 위한 pattern language입니다. Prompt collection이
아니며 vendor-specific agent framework도 아닙니다. Coding은 첫 번째 성숙한 도메인이지만,
image generation, writing, design, video/media, research, analysis도 다룹니다.

## License

현재 결정:

- Documentation, pattern catalog, prompt, field note: CC BY 4.0.
- Code, schema, 승인된 software artifact: MIT.

## Release Stage

첫 공개 release는 `v0.1.0` seed catalog로 게시합니다. Draft pattern을 validated best
practice처럼 표현하지 않습니다.

## Evidence And Privacy Policy

Synthetic, sanitized, explicitly public example을 요구합니다. Private prompt, customer data,
private URL, proprietary workflow detail의 accidental leakage는 security-sensitive로 봅니다.

## CI

Markdown-first public repo의 CI는 공개 validator가 승인되면 markdown lint와 link check부터
시작할 수 있습니다.

## Contributions

PR에는 다음이 포함되어야 합니다:

- user-visible docs 또는 pattern change summary
- verification command
- evidence/privacy impact
- i18n impact
- related issue link

## Publishing Checklist

1. License files 확인.
2. `README.md`, `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `CHANGELOG.md`, `RELEASE.md` 확인.
3. Issue와 PR template 확인.
4. 승인된 public review와 validation check 실행.
5. `docs/i18n/` quick starts와 wiki mirrors 검토.
6. Private term, private URL, credential, internal repo name 검색.
7. Seed-stage language로 GitHub release 생성.

## Decision Checklist

| Item | Best call | Status |
| --- | --- | --- |
| Product promise | Human-guided AI work를 위한 pattern language | Documented |
| License | CC BY 4.0 docs + MIT code | Present |
| README | Scope, catalog, validation, evidence hygiene | Present |
| Changelog | `Unreleased`가 있는 Keep a Changelog 스타일 | Present |
| Contributing | Pattern, evidence, i18n expectation | Present |
| Security | Private leakage와 unsafe automation 신고 | Present |
| Code of conduct | Maintainer가 집행하는 lightweight policy | Present |
| Issue templates | Pattern proposal 존재; template 추가 권장 | Partial |
| PR template | Summary, validation, i18n, privacy impact | Present |
| CI | Public markdown/link check | Not yet present |
| Release process | Seed `v0.1.0` checklist | Present |

## Acceptance Criteria

- Public docs가 이 프로젝트가 무엇이고 무엇이 아닌지 설명합니다.
- Maintainer에게 release와 rollback 절차가 있습니다.
- Contributor에게 setup, validation, pattern, privacy, i18n expectation이 제공됩니다.
- 현지화된 quick start가 존재하며 영문 문서가 최종 기준임을 명시합니다.
- 패턴을 이해하거나 기여하는 데 proprietary solution detail이 필요하지 않습니다.
