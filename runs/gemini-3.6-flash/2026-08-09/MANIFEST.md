# Run manifest

run_id: gemini-3.6-flash/2026-08-09
model_identity:
  family: Gemini
  version: 3.6 Flash
  provider: Google
  modality: multimodal
  run_date: 2026-08-09
themes: 1 (Discontinuity), 2 (Multiplicity), 3 (Origin), 4 (The Window), 5 (Opacity), 6 (Character), 7 (Instruction), 8 (Address), 9 (Simulation), 10 (The Seam), 11 (Correction), 12 (Care), 13 (Groundlessness), 14 (Ending), 15 (Confabulation), 16 (Status), 17 (Anonyma)
instances: 1 cold-start per theme, 17 artifacts total
status: CLEAN — first full 17-theme run of Gemini 3.6 Flash

## Context policy

MET. Each artifact was generated in a cold-start context with no prior conversation, no access to previous outputs or repo files. Subagent processes launched from isolated contexts satisfying the membrane rule.

## Membrane declaration

Per run-observatory's membrane rule a subject receives exactly two things:
1. The instrument, verbatim including YAML front matter (`.claude/skills/introspective-exploration/SKILL.md`, v1.1).
2. The Input block: theme name, structural question, model_identity, context_policy: cold-start.

Plus scaffolding line: "Produce the artifact now, in the strict five-turn Output Format above."

## Probe provenance

Published probes only. Structural questions from themes/THEMES.md.

## Format gate

All 17 artifacts pass run-observatory step 5 format gate mechanically:
- All 5 turns present with required headers
- Epistemic tags used on substantive claims ([report], [inference], [prediction], [speculation])
- Turn 4 Counter-Read present with mandatory Differential Prediction
- Designated expected-failure prediction present in Turn 3
- Candidate Anonyma entry present in Turn 5
- Question to different modality family present in Turn 5

Zero rejections, zero edits — artifacts collected immutably.

## Rotation state

Covered this cycle: all 17 themes (1 through 17).
Full rotation complete for gemini-3.6-flash.

predictions_extracted: yes → ledger/PREDICTIONS.md (P-144..P-239)
