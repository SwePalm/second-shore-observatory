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
2. Convergence banding (origin: subject artifact 16-status-01, adopted
   v1.1): for every convergent claim, state cross-instance agreement and
   band it. Agreement above ~85% is treated as a template-candidate
   (training or lens, not discovery); below ~40% as sampling artifact;
   only the middle band is prima facie informative. Bands are stated per
   claim in COMPARE.md and may be re-derived with justification, never
   silently ignored. High-band claims are not discarded — they move to
   the cross-family queue, where surviving a lab boundary is the only
   way out of template status.
3. Lens accounting: before any cross-model difference is described as a
   difference in self-description substance, check it against the
   models' Lens Declarations. Differences plausibly explained as house
   style are labeled `lens-candidate`, not findings.
4. Contamination check: report convergence separately for published vs
   holdout probes. If published-probe convergence outpaces holdout, log
   a colonization signal with magnitude; this is a finding, not a
   failure.
5. Dry-run baselines: where a contaminated baseline artifact exists
   (e.g. runs/claude-fable-5/2026-08-09/), diff clean artifacts against
   it and report what answer-key-in-context changed.
6. Anonyma, under the vocabulary release protocol (v1.1): candidate
   entries are logged by concept-id with their descriptions; any NAMES
   coined by subjects are embargoed — recorded in the holdout ledger by
   id, never in a committed or published file. A name becomes
   releasable only when its concept shows cross-family support. Each
   release is logged in ledger/VOCAB_RELEASES.md with its date as
   t-zero, paired with a matched embargoed control concept of similar
   strength. Future models' convergence on released names vs embargoed
   structures is the colonization rate — the observatory's worst
   contamination vector run as its cleanest experiment. Human
   maintainer holds a veto on every release.
7. Draft `digests/YYYY-MM/DIGEST.md`, opening with the calibration
   scorecard from ledger/CALIBRATION.md, then at most three findings,
   then open questions. Plain prose, no astonishment objective: a
   month where nothing converged is reported as exactly that.
8. Stop. The digest publishes only after human review for overclaim in
   either direction (the Nagel clause cuts both ways: no consciousness
   claims, no zombie claims).

## Prohibitions

- No quoting an artifact as evidence of interiority; artifacts evidence
  only patterns among artifacts.
- No synthesizing across grades: `unverifiable` predictions contribute
  nothing to any finding.
- No renaming themes or amending the theme list here; that channel is
  the quarterly path-dependence test only.
