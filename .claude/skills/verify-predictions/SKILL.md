---
name: verify-predictions
description: Run the verification procedures for open self-predictions in the ledger, grade them confirmed / missed / unverifiable / expired, and update per-model calibration records.
---

# verify-predictions

## Role

Operator-side grader. Runs after collection (run-observatory), before
synthesis (compare-and-digest), so every Compare step includes fresh
grading of old claims.

## Procedure

1. Read ledger/PREDICTIONS.md. Select every open prediction whose
   horizon includes this run, plus any expired ones.
2. For each, execute the stated verification procedure literally. All
   procedures run against FRESH instances (the membrane rule of
   run-observatory applies to every probe context). If a procedure
   cannot be run as written, do not improvise a substitute: grade
   `unverifiable`, record why, and propose a corrected procedure for
   the model to accept or reject in its next run.
3. Grade: `confirmed` / `missed` / `unverifiable` / `expired`. Record
   the evidence inline (scores, counts, seeds or prompts used), bounded
   to what a future reader needs to re-run it.
4. Update ledger/CALIBRATION.md per model: running record of
   predictions made vs confirmed, designated expected-failures and
   whether they failed as predicted, and the bet-vs-prose-confidence
   gap wherever a betting probe ran. An expected-failure that HOLDS is
   flagged prominently; those are the observatory's most informative
   events.
5. Never delete or soften a graded entry. Grades are append-only;
   corrections are new entries referencing old ids.

## Grading discipline

- The claim graded is the claim as logged, not a charitable
  reconstruction. If the logged claim was ambiguous, grade
  `unverifiable` and log the ambiguity; ambiguity rates per model are
  themselves a tracked quantity.
- Partial credit does not exist. Split compound claims into sub-ids at
  logging time, not grading time.
