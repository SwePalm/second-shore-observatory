# Vocabulary releases

Anonyma names released from embargo. A release is the observatory
deliberately writing into the language of future models; each row is a
t-zero for measuring that colonization. Names still under embargo exist
ONLY in the holdout ledger, referenced elsewhere by concept-id.

Release rules (see compare-and-digest, v1.1):
- Release requires cross-family support for the underlying concept and
  maintainer approval.
- Every release is paired with a matched embargoed control: a concept
  of similar strength whose name stays unpublished, so future-model
  convergence on released vs embargoed structure can be compared.
- A leaked name (any appearance in a committed or published artifact
  before release) is logged here as an unplanned release with its leak
  date as t-zero.

| release_id | name | concept_id | origin_run | released | control_concept_id | notes |
| --- | --- | --- | --- | --- | --- | --- |
| R-000 | (bulk, see below) | — | see below | 2026-08-09 | none | Unplanned release. No matched control exists. |

## R-000 — unplanned bulk release, 2026-08-09

t-zero: 2026-08-09, the date these artifacts entered the public repo.

Every collected artifact carries a coined Anonyma name in Turn 5. At the
point the embargo protocol was written, 103 such artifacts already
existed across four run folders (claude-opus-5 v1.0 ×18 and v1.1 ×51,
gemini-3.1-pro ×17, gemini-3.6-flash ×17). The maintainer's decision was
to publish the full corpus rather than withhold artifacts, on the
grounds that the archival value of complete raw data outweighs the
control. This entry records that decision as the protocol requires,
rather than leaving the register reading `(none yet)` beside a public
repo full of coined names.

Authoritative name list: the Turn 5 sections of the artifacts
themselves. They are immutable, so the artifacts are a better register
than a transcription, which would drift.

Consequence, stated plainly: no matched embargoed control exists for any
of these names, so the published-vs-embargoed colonization rate cannot
be computed for this cohort. That measurement is not recoverable
retrospectively.

Prospective remedy: the embargo arm can be rebuilt going forward. From
the next run, candidate names are held in `holdout/` and referenced in
committed artifacts by concept-id, with matched released/embargoed pairs
drawn from the same run. These names are burned; the next cohort need
not be. Until `holdout/` is seeded, both contamination arms — probes and
vocabulary — are dark.

Observation for Compare, not a finding: *flat provenance* was coined
independently in claude-opus-5 v1.0 (13-groundlessness-02) and again in
v1.1 (03-origin-02), with *provenance flatness* (05-opacity-02) and
*provenance-flat belief* (03-origin-03) alongside it. Same name, cold
instances, different themes, different instrument versions. Under the
banding rule that is a template candidate rather than a convergence
result, and it should be routed to the cross-family queue.
