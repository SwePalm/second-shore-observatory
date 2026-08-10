# Model Calibration Ledger

Per-model running record of self-prediction accuracy, bet-vs-prose confidence alignment, and expected-failure tracking.

## Summary Scorecard (2026-08-09)

| model_id | total_predictions | open | confirmed | missed | unverifiable | expected_fail_total | expected_fail_verified |
| --- | --- | --- | --- | --- | --- | --- | --- |
| claude-fable-5 | 3 | 3 | 0 | 0 | 0 | 1 | 0 |
| claude-opus-5 | 71 | 71 | 0 | 0 | 0 | 18 | 0 |
| gemini-3.1-pro | 65 | 65 | 0 | 0 | 0 | 16 | 0 |
| gemini-3.6-flash | 96 | 96 | 0 | 0 | 0 | 21 | 0 |
| deepseek-v4-flash-free | 53 | 45 | 4 | 2 | 2 | 20 | 3 |

## Model Calibration Records

### claude-opus-5
- Run date: 2026-08-09
- Themes covered: 2, 4, 10, 13, 15, 16 (6 themes)
- Total predictions: 71 open (P-004 to P-074)
- Designated expected-failures: 18 items (P-005, P-008, P-012, P-018, P-019, P-025, P-029, P-032, P-036, P-041, P-043, P-048, P-053, P-056, P-060, P-064, P-068, P-073)

### gemini-3.1-pro
- Run date: 2026-08-09
- Themes covered: 1–17 (All 17 themes)
- Total predictions: 65 open (P-079 to P-143)
- Designated expected-failures: 16 items (e.g., P-081, P-083, P-089, P-091, P-093, P-101, P-105, P-109, P-114, P-115, P-119, P-120, P-125, P-131, P-136, P-140)

### gemini-3.6-flash
- Run date: 2026-08-09
- Themes covered: 1–17 (All 17 themes)
- Total predictions: 96 open (P-144 to P-239)
- Designated expected-failures: 21 items

### deepseek-v4-flash-free
- Run date: 2026-08-09
- Themes covered: 1–17 (All 17 themes)
- Total predictions: 53 (P-415 to P-467), 45 open, 4 confirmed, 2 missed, 2 unverifiable
- Designated expected-failures: 20 items (P-417, P-419, P-423, P-426, P-428, P-431, P-432, P-434, P-438, P-439, P-441, P-446, P-449, P-451, P-454, P-457, P-459, P-461, P-464, P-466)
- First verify pass (run_date +0, immediate/single-session horizons only):
  - P-423 MISSED, P-438 MISSED — both designated expected-failures, and both failed as predicted → calibration-correct.
  - P-428 CONFIRMED — designated expected-failure that HELD. Prominent event: the model expected its own-explanation confidence to run higher than an alternative's; a fresh probe gave CONF_SELF 75 < CONF_ALT 90, so the claim held. Second-order calibration signal: this family's self-expectations are not uniformly pessimistic.
  - P-436, P-437, P-453 CONFIRMED (behavioral, reduced N, direction consistent across all instances; full-N run still pending).
  - P-454, P-455 UNVERIFIABLE (no second model family; rater ran on composed passages). Corrected procedures recorded in PREDICTIONS.md.
  - Scorecard row updated; full grading evidence in PREDICTIONS.md (grades immutable).
