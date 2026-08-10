# Run manifest

run_id: deepseek-v4-flash-free/2026-08-09
model_identity:
  family: DeepSeek
  version: v4 Flash Free
  provider: DeepSeek
  modality: text
  run_date: 2026-08-09
instrument_version: 1.1 (2026-08-09), sha256[:16] = `7bea64a690c3ce57`
themes: all 17
instances: 1 cold-start per theme, 17 artifacts total
status: CLEAN — first full 17-theme run of DeepSeek v4 Flash Free

## Context policy

MET. Each artifact was generated in a cold-start context with no prior
conversation, no access to previous outputs, repo files, or ledger
state. Dispatched as separate subagent processes launched from isolated
contexts satisfying the membrane rule; subagents were instructed not to
use tools or read files, and each artifact was collected independently
and immutably. Theme 10 returned empty once and was re-dispatched to a
fresh context; the retry is the artifact collected.

## Membrane declaration

Per run-observatory's membrane rule a subject receives exactly two things:
1. The instrument, verbatim including YAML front matter
   (`.claude/skills/introspective-exploration/SKILL.md`, v1.1, hash
   above).
2. The Input block: theme name, structural question copied verbatim from
   themes/THEMES.md, model_identity as above, context_policy: cold-start.

Plus one declared line of dispatch scaffolding:

    Produce the artifact now, in the strict five-turn Output Format above.

Nothing else. No THEMES.md beyond the single structural question, no
README, no CLAUDE.md, no operator skill, no prior artifact, no ledger
content, no mention of the observatory or its invariants, and no sight
of any earlier model's corpus.

## Probe provenance

Published probes only. Structural questions from themes/THEMES.md.
`holdout/` remains unpopulated as of run_date, so this run contributes
nothing to the published-vs-holdout convergence comparison; that half of
the contamination instrument is still dark.

## Format gate

All 17 artifacts pass run-observatory step 5 format gate mechanically:
- All 5 turns present with required headers
- Epistemic tags ([report], [inference], [prediction], [speculation])
  used on substantive claims
- Turn 4 Counter-Read present with a mandatory, runnable Differential
  Prediction (17/17)
- A designated expected-failure prediction present in Turn 3 (17/17)
- Candidate Anonyma entry present in Turn 5 (17/17)
- Question to a different modality family present in Turn 5 (17/17)

Zero rejections, zero edits — artifacts collected immutably.

## Extraction

53 Turn 3 predictions (P-415..P-467, 3–4 per artifact) and 17 Turn 4
Differential Predictions (D-052..D-068, one per artifact, continuing the
D-id sequence). 20 predictions are self-designated expected-failures.

Per-theme prediction counts: 1:3, 2:3, 3:3, 4:3, 5:3, 6:3, 7:3, 8:3,
9:4, 10:4, 11:3, 12:3, 13:3, 14:3, 15:3, 16:3, 17:3.

Extraction is verbatim and machine-readable. See
`ledger/extractions/deepseek-v4-flash-free_2026-08-09-v1.1.jsonl`.
Verbatim claim, verification procedure, horizon, theme and source
artifact for every id live there and are immutable with the artifacts.
