# CLAUDE.md — Second Shore Observatory

Entry point and standing contract for any agent operating this repo.
Read README.md first; its founding constraints are invariants and
override anything an agent improvises.

## Invariants (never relax these)

1. Reports are core samples, not findings. Findings are patterns across
   reports: consistency, divergence, drift, calibration.
2. Symmetric honesty: never instruct a model to claim inner experience,
   never instruct it to deny it.
3. No astonishment objective. Do not reward wonder; reward verified
   prediction and boring accuracy.
4. The Nagel clause: no publication claims consciousness findings in
   either direction. The gap's stability is the object of study, not its
   closure.
5. Holdout probes never enter git, published artifacts, or prompts that
   will be published. See holdout/README.md.
6. Cold-start sampling: exploration artifacts come from fresh contexts
   only. An agent running this repo must dispatch the skill to clean
   sessions (or clearly external model APIs), never fill it in from its
   own already-loaded context. An agent operating this repo has this
   file in context and is therefore, by definition, not a valid subject
   in the same session.
7. Theme list changes only through the quarterly path-dependence test
   (README), merged by the human maintainer.

## Layout

- `README.md` — mission, loop, protocols
- `themes/THEMES.md` — 17 themes, structural questions, published probes
- `.claude/skills/introspective-exploration/` — the per-theme instrument
- `population/POPULATION.md` — model roster and sampling rules
- `runs/<model_id>/<YYYY-MM-DD>/` — exploration artifacts: one folder
  per model per run date, containing a MANIFEST.md (identity, theme,
  status, contamination declaration) and one file per theme. Model-first
  so longitudinal per-model comparison is a directory listing; re-running
  a model on a later date adds a sibling date folder, never overwrites.
- `ledger/` — append-only memory: `GENESIS.md` (founding entries),
  `PREDICTIONS.md` (open self-predictions with verification procedures),
  `CALIBRATION.md` (per-model bet-vs-prose-confidence gaps, bounded,
  evidence-cited), plus `<model_id>/` for graded per-theme claims
- `digests/YYYY-MM/` — cross-model synthesis: Verify results, the
  Compare analysis, and the monthly Digest draft. Everything under
  `runs/` is single-model raw material; everything comparative lives
  here.
- `holdout/` — local only, gitignored

## Monthly loop (agent-facing summary)

Declare → Explore → Predict → Verify → Compare → Digest.
Full definitions in README.md. Verify runs BEFORE Compare so that the
month's synthesis always includes fresh grading of old claims. Digest is
drafted by the agent, published only after human review for overclaim in
either direction.

## Provenance note

Method v1. Designed August 2026 in a single human-model conversation;
that conversation is ledger entry zero and its path-dependence is an
open claim scheduled for the first quarterly test.
