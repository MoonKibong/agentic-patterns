# Open Source Readiness

이 문서는 Agentic Patterns의 공개 릴리스 기본값을 기록합니다.

## Task Evaluation

Verdict: `REVISE` until translated quick starts and full wiki mirrors have a human review pass.

Primary risk: 이 프로젝트는 실제 agentic workflow에서 영감을 받았으므로, public docs는
proprietary prompt, private harness detail, customer data, private repo name, internal workflow
transcript를 노출하면 안 됩니다.

## Positioning

Agentic Patterns는 human-guided AI work를 위한 pattern language입니다. Prompt collection이
아니며 vendor-specific agent framework도 아닙니다. Coding은 첫 번째 성숙한 도메인이지만,
image generation, writing, design, video/media, research, analysis도 다룹니다.

## License

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

PR에는 user-facing change summary, verification command, evidence/privacy impact, i18n impact,
related issue link가 있어야 합니다.

## Publishing Checklist

1. License files 확인.
2. `README.md`, `CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `CHANGELOG.md`, `RELEASE.md` 확인.
3. Issue와 PR template 확인.
4. 승인된 public review와 validation check 실행.
5. `docs/i18n/` quick starts와 wiki mirrors 검토.
6. Private term, private URL, credential, internal repo name 검색.
7. Seed-stage language로 GitHub release 생성.
