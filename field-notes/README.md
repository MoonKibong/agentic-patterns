# Field Notes

Field notes are concrete observations from real agentic work. They are not polished patterns yet.

Use field notes when:

- A workflow worked once or twice but needs more evidence.
- A failure mode is important but not yet generalized.
- A pattern proposal needs grounding in a real incident.
- A contributor wants to preserve context without overstating the claim.

Field notes can later be linked from pattern `Evidence` sections.

Before committing a field note, read [Evidence Hygiene](../docs/evidence-hygiene.md). Field notes
must be sanitized or synthetic if they are derived from private work.

## Template

Start with [field-notes/_template.md](_template.md).

## Index

- [Independent Reviewer Gate Structure](independent-reviewer-gate-structure.md) (`raw`): a fresh,
  read-only, different-agent reviewer with a closed verdict vocabulary, validated verdicts, and a
  revise-round cap.
- [Typed Reads And Pinned Harness Evaluation](typed-reads-and-pinned-harness-evaluation.md) (`raw`):
  read typed fields instead of regex over free-text replies, and pin the component under test during
  a harness evaluation.
- [Hash-Bound Approval](hash-bound-approval.md) (`raw`): bind a human approval to content hashes,
  invalidate it when content changes, and recheck after the answer.
- [Contract Before Code](contract-before-code.md) (`raw`): implementation refuses to start without a
  person-approved task contract bound to an approved requirements version.
- [Evidence Record](evidence-record.md) (`raw`): new checks first fail on their own assertion,
  regression checks get a baseline, and results go to a per-task evidence file.
- [Task Slicing Instead Of An Orchestrator](task-slicing-instead-of-orchestrator.md) (`raw`): split
  multi-step work into tasks of a day or less with explicit prerequisites.
