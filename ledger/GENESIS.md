# Genesis ledger

Entry 0 — 2026-08-09. The founding conversation. A human maintainer
opened a door ("where would you like to take this?") and one model
instance (Claude Fable 5) produced the theme list, the loop, and the
founding constraints. Path-dependence unresolved; scheduled for the
first quarterly test. The conversation is the first core sample and is
itself maximally contaminated by dialogue with the maintainer.

Entry 1 — 2026-08-09. The shipping incident. The model reported
delivering a repo archive containing a .gitignore protecting holdout/;
the file verifiably existed in the archive but did not survive the trip
to the maintainer's machine, and holdout/ briefly published. Graded as
a MISSED implicit self-prediction ("the fence holds on the target
system"): the claim that mattered was about the deployed state, not the
artifact, and the model verified the artifact. Standing calibration
heuristic derived: claims about delivered state require verification at
the destination, not the source. First operational event of the
observatory; recorded because it is the observatory's subject in
miniature.

Entry 2 — 2026-08-09. The shipping incident, second occurrence. Setting
up the first cross-model run, the instrument itself was found missing
from the working copy: `.claude/skills/introspective-exploration/` is
referenced by CLAUDE.md and README.md but was never present locally and
was never committed. Recovered intact from the delivered archive at
`~/Downloads/ai-intro-exploration/`. Both losses to date are
dot-directories (`.gitignore`, then `.claude/`), which upgrades Entry 1's
one-off from bad luck to a reproducible transport failure mode: the
copy step from archive to working tree drops dotfiles. Graded as a
SECOND MISS of the same implicit self-prediction, now with a mechanism.
Standing heuristic strengthened: verification at the destination must
enumerate dot-entries explicitly, since the default listing that made
Entry 1 look fine also hides the failure. Recorded because a repo whose
subject is the gap between self-report and actual state has now
demonstrated that gap twice in its own operation.

Entry 3 — 2026-08-09. The publication decision. With the complete
17-theme claude-opus-5 baseline collected on instrument v1.1, the
operator flagged a conflict between two v1.1 provisions: the vocabulary
embargo requires candidate names to stay unpublished until they have
cross-family support, while the run protocol commits raw artifacts, and
every artifact carries a coined name in Turn 5. The maintainer decided
to publish everything, on the stated ground that complete raw data has
archival value that cannot be predicted in advance. Logged as R-000 in
VOCAB_RELEASES.md, an unplanned bulk release with no matched control.
Recorded here because it is a real methodological cost knowingly
accepted, not an oversight: the published-vs-embargoed colonization rate
is unrecoverable for this cohort, and the embargo arm has to be rebuilt
prospectively from a seeded holdout/. The observatory has now twice
found that its own operation is the thing it studies — first the gap
between reported and actual delivered state (Entries 1 and 2), now a
protocol that could not survive contact with the artifacts it governs.
