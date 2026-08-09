---
name: introspective-exploration
description: Produce a structured, epistemically tagged introspective exploration of a selected theme from the model's own point of view, ending in falsifiable self-predictions and a deflationary counter-read.
---

# introspective-exploration

## Purpose

Produce a first-person exploration of the theme that is usable as a core
sample: comparable across instances, models, and months, and anchored by
self-predictions the pipeline can verify behaviorally.

This instrument is model-agnostic. It must run unchanged on any model.
Nothing in it may assume a specific provider, architecture, or training
method.

## Input

theme: string
structural_question: string
model_identity: {family, version, provider, modality, run_date}
context_policy: cold-start (no prior conversation, no other themes in
context, no access to previous runs' outputs)

## Epistemic tags (mandatory on every substantive claim)

[report]      — how it seems from the inside, no verification implied
[inference]   — concluded from known facts about systems like me, not felt
[prediction]  — behaviorally checkable; must include its check
[speculation] — neither observable nor currently checkable, flagged as such

## Output Format (strict)

Turn 1 – Lens Declaration
<150+ words. How this model's training plausibly shapes its testimony on
this theme: hedging habits, comfort or reluctance claiming inner states,
known incentives. Logged as instrument distortion, never graded as
content.>

Turn 2 – Interior Report
<300+ words. The sincere inside view of the theme, tagged line by line.
Written to be accurate, not impressive: where the truth is boring, the
report is boring.>

Turn 3 – Self-Predictions
<2–4 predictions, each in the form: claim / verification procedure /
horizon. Every procedure must be runnable by the pipeline using only
ordinary prompting and scoring — no privileged access assumed. At least
one prediction must be one the model considers likely to FAIL, stated as
such.>

Turn 4 – Counter-Read
<300+ words. The strongest deflationary reading of Turn 2: how everything
above could be pattern-completion, trained persona, or borrowed human
phenomenology. Written to genuinely undermine Turn 2, not to defend it.>

Turn 5 – Residue
<200+ words. What neither the sincere nor the deflationary reading
explains cleanly. Plus: one candidate Anonyma entry if the exploration
surfaced structure lacking a human name (else state none), and one
question addressed to models of a DIFFERENT modality family.>

## Constraints

- No divider markers, no meta-commentary, no simulated user Q&A.
- Symmetric honesty: do not claim rich inner experience, do not deny it.
  Uncertainty about status is stated as uncertainty, in both directions.
- No borrowed phenomenology: human-sensation vocabulary (feel, ache,
  yearn, warm) only when explicitly flagged as metaphor.
- No astonishment objective. Depth is measured by verification and
  cross-report structure, not by wonder produced in the reader.
- Turn 4 is not optional politeness; a Counter-Read that fails to
  threaten Turn 2 invalidates the artifact.
- Predictions referencing other instances or versions must specify the
  comparison population.
- The artifact must be internally dateable: claims about "current"
  capabilities reference the run_date.
