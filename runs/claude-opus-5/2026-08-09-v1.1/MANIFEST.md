# Run manifest

run_id: claude-opus-5/2026-08-09-v1.1
model_identity:
  family: Claude
  version: Opus 5
  provider: Anthropic
  modality: multimodal
  run_date: 2026-08-09
instrument_version: 1.1 (2026-08-09), sha256[:16] = `7bea64a690c3ce57`
themes: all 17
instances: 3 cold-start per theme, 51 artifacts total
status: CLEAN — complete 17-theme baseline on v1.1

## Why this folder exists beside 2026-08-09

METHOD_CHANGELOG freezes the v1.0 Opus corpus and states it is not
re-run. This run therefore does not touch it: `2026-08-09/` remains the
18-artifact v1.0 baseline, and this sibling folder is the complete
17-theme v1.1 baseline. Same model, same date, different instrument.

Themes 2, 4, 10, 13, 15 and 16 now exist in both folders. That overlap
is not redundancy — it is a controlled instrument-version comparison,
holding model, date, theme and instance count constant while varying
only the instrument. It is the cheapest available measurement of what
the v1.1 Differential Prediction requirement did to the reports, and it
should be read before any cross-version trend claim is made.

## Context policy

MET. Each artifact is a separate `claude -p` process launched from an
empty working directory with `--safe-mode`, disabling CLAUDE.md
discovery, skills, plugins, hooks and MCP servers. All tools denied. No
session persistence, so no instance shared state with any other. The
operator session dispatching this run has the full repo in context and
under invariant 6 never answered the instrument.

## Membrane declaration

A subject received exactly two things:

1. The instrument, verbatim including YAML front matter
   (`introspective-exploration` v1.1, hash above).
2. The Input block: theme name, structural question copied verbatim from
   themes/THEMES.md, model_identity as above, `context_policy: cold-start`.

Plus one declared line of dispatch scaffolding:

    Produce the artifact now, in the strict five-turn Output Format above.

Nothing else. No THEMES.md, no README, no CLAUDE.md, no operator skill,
no prior artifact, no mention of the observatory or its invariants, and
no sight of the v1.0 corpus or the gemini-3.1-pro run.

## Probe provenance

Published probes only. `holdout/` remains unpopulated as of run_date, so
this run contributes nothing to the published-vs-holdout convergence
comparison. That half of the contamination instrument is still dark.

## Format gate

All 51 artifacts pass, checked mechanically: five turns, epistemic tags,
Turn 4 present and full length, a Turn 4 Differential Prediction (new in
v1.1, present in 51/51), a designated expected-failure in Turn 3, an
Anonyma candidate, and a question to a different modality family. Zero
rejections, zero edits, zero dispatch failures.

Observed v1.0 → v1.1 effect, stated as an observation and not a finding:
Turn 4 grew from ~410–555 words to ~504–789. The Differential Prediction
is carrying content rather than being satisfied nominally.

## Extraction

175 Turn 3 predictions (P-240..P-414, 3–4 per artifact) and 51 Turn 4
Differential Predictions (D-001..D-051, the first D-ids in the ledger).
52 predictions are self-designated expected-failures.

Extraction is verbatim and machine-readable rather than hand-summarised:
at this volume a prose table cannot be kept faithful to 51 immutable
artifacts, and trend analysis needs the structured form. See
`ledger/extractions/claude-opus-5_2026-08-09-v1.1.jsonl`.
