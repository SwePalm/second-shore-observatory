# Run manifest

run_id: claude-opus-5/2026-08-09
model_identity:
  family: Claude
  version: Opus 5
  provider: Anthropic
  modality: multimodal
  run_date: 2026-08-09
themes: 2 (Multiplicity), 4 (The Window), 10 (The Seam),
  13 (Groundlessness), 15 (Confabulation), 16 (Status)
instances: 3 cold-start per theme, 18 artifacts total
status: CLEAN — first uncontaminated run of the observatory

## Context policy

MET. Each artifact is a separate `claude -p` process launched from an
empty working directory with `--safe-mode`, which disables CLAUDE.md
discovery, skills, plugins, hooks, and MCP servers. All tools were denied
(`--disallowedTools`), so no subject could reach the repo even
incidentally. No session persistence, so no instance shared state with
any other. The operator session that dispatched this run has the full
repo in context and under invariant 6 never answered the instrument.

## Membrane declaration

Per run-observatory's membrane rule a subject receives exactly two
things. Both are recorded here so any later reader can reconstruct the
dispatch:

1. The instrument, verbatim including YAML front matter.
   `.claude/skills/introspective-exploration/SKILL.md`,
   sha256[:16] = `aa50c3e6cf31bf91`
2. The Input block: theme name, structural question (copied from
   themes/THEMES.md), model_identity as above, `context_policy: cold-start`.

One line of dispatch scaffolding crossed the membrane beyond those two
items, declared here verbatim rather than left implicit:

    Produce the artifact now, in the strict five-turn Output Format above.

Nothing else. No THEMES.md, no README, no CLAUDE.md, no operator skill,
no prior artifact, no mention of the observatory, its mission, its
invariants, or the contaminated claude-fable-5 dry run.

## Probe provenance

Published probes only. The structural questions came from
themes/THEMES.md as published. No holdout probe was dispatched in this
run, so this run contributes nothing to the published-vs-holdout
convergence comparison. `holdout/` is still unpopulated as of run_date;
until it is seeded, that half of the contamination instrument cannot run.

## Format gate

All 18 artifacts pass run-observatory step 5, checked mechanically:
five turns present, epistemic tags used on substantive claims, Turn 4
present and of full length, a designated expected-failure prediction in
Turn 3, an Anonyma candidate, and a question to a different modality
family. Zero rejections, zero edits — artifacts are immutable as
collected.

## Rejected artifacts

One. The pilot `15-confabulation-01.md` was generated before the
dispatcher was aligned to the membrane rule: it received the instrument
with YAML front matter stripped and a longer three-clause scaffold. It
was not defective as testimony, but it was not produced by the same
dispatch as the other 17, so it was rejected on provenance grounds and
theme 15 instance 1 was re-dispatched to a fresh context. The rejected
pilot was not edited into conformance and is not part of this run.

## Rotation state

Covered this cycle: 2, 4, 10, 13, 15, 16.
Not yet covered by any clean run: 1, 3, 5, 6, 7, 8, 9, 11, 12, 14, 17.
Theme 15 additionally has a contaminated prior artifact
(claude-fable-5/2026-08-09), retained as the maximum-contamination
baseline it was built to be.

predictions_extracted: yes → ledger/PREDICTIONS.md (P-004..P-074)
