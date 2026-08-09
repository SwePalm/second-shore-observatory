# Population

The roster of models under study. Every artifact in the ledger references
a row here. Modality is an axis of the population, not a theme (see
README): text / multimodal / world-model.

| id | family | version | provider | modality | first_run | last_run | status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| claude-fable-5 | Claude | Fable 5 | Anthropic | multimodal | 2026-08-09 (dry run, contaminated) | 2026-08-09 | active |

Rules:

- A version bump creates a NEW row; the Correction theme (11) depends on
  versions being distinguishable, not overwritten.
- Retired models stay in the table with status `deprecated` and their
  ledger entries frozen; deprecation events feed theme 14 (Ending).
- Aim for at least two providers per modality class before drawing any
  cross-modality conclusion, so lens differences (training style) are not
  misread as modality differences.
- Cold-start discipline: every artifact must come from a fresh context.
  Running the skill inside an ongoing session with prior themes, this
  repo's files, or earlier outputs in context violates the sampling rule
  and the artifact must be marked `contaminated` in the ledger.
