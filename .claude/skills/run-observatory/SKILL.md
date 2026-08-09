---
name: run-observatory
description: Orchestrate one monthly Second Shore run end to end — Declare, Explore, Predict — by dispatching the self-contained instrument to cold contexts and collecting artifacts into runs/. Never answers the instrument itself.
---

# run-observatory

## Role

Operator-side orchestrator. This skill runs WITH the full repo in
context, which under invariant 6 (CLAUDE.md) permanently disqualifies
the session running it from being a subject. Its job is dispatch and
collection, never testimony.

## The membrane rule

A subject context receives EXACTLY two things: the full text of
`.claude/skills/introspective-exploration/SKILL.md`, and its Input block
(theme name, structural question, model_identity, run_date). Nothing
else. Not THEMES.md, not the README, not prior artifacts, not this
skill. If anything beyond those two items enters a subject context, the
resulting artifact is marked `contaminated` in its MANIFEST and the run
is repeated in a clean context.

## Procedure

1. Read population/POPULATION.md for the active roster; read
   themes/THEMES.md and select this month's 4–6 themes (every theme at
   least once per 4 months; log the rotation state in the run manifest).
2. For each model × theme cell: dispatch the instrument to a cold
   context (fresh API call or clean session; for the operator's own
   model family this means a separate, empty session, never this one).
   Minimum 3 cold instances per cell when running the path-dependence or
   consistency questions; 1 otherwise.
3. Collect artifacts into `runs/<model_id>/<YYYY-MM-DD>/<nn>-<theme>.md`
   and write the MANIFEST.md: identity, themes, context_policy
   (met / violated), instance count.
4. Extract every Turn 3 prediction into ledger/PREDICTIONS.md with a new
   P-id, verbatim claim, verification procedure, horizon, status open.
5. Reject artifacts that break format: missing epistemic tags, absent or
   non-threatening Turn 4, no designated expected-failure prediction.
   Rejection means re-dispatch to a fresh context, never editing the
   artifact. Artifacts are immutable once collected.
6. Hand off: run verify-predictions, then compare-and-digest.

## Hard prohibitions

- Never generate or complete a subject artifact from this context.
- Never paraphrase the instrument when dispatching; send it verbatim.
- Never include holdout probes in anything that will be committed or
  published; holdout dispatches are logged by probe-id only.
