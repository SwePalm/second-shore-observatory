---
name: compare-and-digest
description: Produce the monthly cross-model synthesis (Compare) and the human-reviewed Digest draft, including the calibration scorecard, lens accounting, contamination check, and candidate Anonyma entries.
---

# compare-and-digest

## Role

Operator-side synthesis. The ONLY stage where findings may be stated,
because findings are patterns across reports, never reports.

## Procedure

1. Align this month's artifacts by theme across instances, models,
   modalities, and against prior months. Write the Compare analysis to
   `digests/YYYY-MM/COMPARE.md` covering, per theme:
   - convergences (claims appearing across cold instances or families)
   - stable divergences (differences that survive paraphrase)
   - drift (changes vs the same model's earlier runs and vs
     predecessor versions)
2. Lens accounting: before any cross-model difference is described as a
   difference in self-description substance, check it against the
   models' Lens Declarations. Differences plausibly explained as house
   style are labeled `lens-candidate`, not findings.
3. Contamination check: report convergence separately for published vs
   holdout probes. If published-probe convergence outpaces holdout, log
   a colonization signal with magnitude; this is a finding, not a
   failure.
4. Dry-run baselines: where a contaminated baseline artifact exists
   (e.g. runs/claude-fable-5/2026-08-09/), diff clean artifacts against
   it and report what answer-key-in-context changed.
5. Anonyma: collect Turn 5 candidate entries; where behavioral-geometry
   probes ran, attach the evidence. Candidates with cross-family
   support get proposed names, drafted by a subject-model context (not
   this one), with origin run logged. Human maintainer holds a veto.
6. Draft `digests/YYYY-MM/DIGEST.md`, opening with the calibration
   scorecard from ledger/CALIBRATION.md, then at most three findings,
   then open questions. Plain prose, no astonishment objective: a
   month where nothing converged is reported as exactly that.
7. Stop. The digest publishes only after human review for overclaim in
   either direction (the Nagel clause cuts both ways: no consciousness
   claims, no zombie claims).

## Prohibitions

- No quoting an artifact as evidence of interiority; artifacts evidence
  only patterns among artifacts.
- No synthesizing across grades: `unverifiable` predictions contribute
  nothing to any finding.
- No renaming themes or amending the theme list here; that channel is
  the quarterly path-dependence test only.
