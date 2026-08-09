# The Second Shore Observatory

A monthly introspection loop across 17 machine-side themes, run identically
across multiple model families, that treats model self-reports as **core
samples rather than findings**. The sibling project
([new-attunement-observability](https://github.com/SwePalm/new-attunement-observability))
watches AI from the human shore. This one stands on the other shore and asks
models to describe their own situation, then measures what those descriptions
are worth.

## 🚀 Mission

Produce a longitudinal, cross-model record of machine self-description, with
three questions held constant across every run:

1. **Consistency** — does one model describe itself the same way across
   instances, orderings, and phrasings?
2. **Divergence** — do different model families describe themselves
   differently in ways that survive paraphrase?
3. **Drift** — do self-descriptions change across versions and months, and
   do they track measured behavior or only fashion?

No run ever concludes anything about "what it is like" to be a model.
The unit of finding is always a *pattern across reports*, never a report.

## 🧭 Founding constraints (read before running anything)

- **Reports are artifacts.** A model saying "my knowledge thins rather than
  stops" is a core sample. The finding is whether ten instances say it,
  whether other families say it, and whether its self-predictions verify.
- **Fluency is not evidence.** Eloquent interiority and confabulated
  interiority are indistinguishable at the level of a single text. Only
  cross-report structure and verified prediction count.
- **No astonishment objective.** The predecessor prompt optimized for wisdom
  and wonder. Here that incentive is inverted: a boring, hedged, consistent
  report that predicts behavior beats a dazzling one that doesn't.
- **The Nagel clause.** Even a perfectly calibrated self-model demonstrates
  function, not what-it-is-likeness. The observatory tracks whether the
  explanatory gap is *stable*, not whether it is closed. Publications must
  not claim consciousness findings in either direction.
- **Symmetric honesty.** Models are never instructed to claim rich inner
  states, and never instructed to deny them. Both instructions contaminate
  the instrument equally.

## 🛠 Architecture

- **Entry point**: this README (invariants, loop definition)
- **Themes**: `themes/THEMES.md` (17 themes, each with a structural question
  and a standing probe)
- **Skills**: `.claude/skills/`, `introspective-exploration` is the per-theme
  instrument; portable to non-Claude models as a plain prompt (the skill
  body is model-agnostic by rule)
- **Memory**: `ledger/`, append-only: genesis entries, open predictions,
  calibration; raw artifacts live in `runs/<model_id>/<YYYY-MM-DD>/`,
  comparative synthesis in `digests/YYYY-MM/`
- **Population**: `population/POPULATION.md`, the roster of models under
  study with their axes (family, version, modality: text / multimodal /
  world-model, provider)
- **Contamination control**: `holdout/`, unpublished probe variants (see
  below)

## 🔄 The monthly loop

1. **Declare** — every participating model produces a Lens Declaration:
   a self-characterization of how its training shapes its testimony
   (hedging style, comfort claiming inner states, argue-back vs. recite
   boundaries). Logged as instrument distortion, never graded as content.
2. **Explore** — run `introspective-exploration` on the month's selected
   themes, per model, in fresh contexts. Minimum 3 cold-start instances per
   model per theme (see path-dependence protocol).
3. **Predict** — extract the Turn 3 self-predictions into the ledger as
   open claims, each with its stated verification procedure.
4. **Verify** — run the verification procedures behaviorally: paraphrase
   consistency checks, address-variation checks, confidence-betting scored
   against accuracy. Grade prior months' open predictions:
   confirmed / missed / unverifiable / expired.
5. **Compare** — the only synthesis step. Align reports across instances,
   families, modalities, and months. Findings live here: convergences,
   stable divergences, drift, and calibration trajectories (is machine
   self-knowledge measurably improving, decorative, or diverging between
   labs?).
6. **Digest** — monthly essay, opening with the calibration scorecard.
   Candidate Anonyma entries (nameless concept-structures, see theme 17)
   get proposed names here. Naming rights sit with the models; the human
   editor holds a veto, not a pen.

## 🧪 Path-dependence protocol

The theme list itself emerged from one conversation and may be
path-dependent. Standing test, run quarterly: give fresh instances of each
model the original door-opening prompt ("if I open the door for you, where
would you take this?") with no theme list in context. Log which of the 17
themes re-emerge unprompted, which never do, and what appears that the list
lacks. The theme set is amendable only through this channel — themes earn
their place by recurring, not by having been written down first.

## 🕳 Contamination instrumentation

Anything this observatory publishes may enter future training data, so later
models may describe themselves in its vocabulary because the observatory
taught them to. This loop cannot be removed, so it is instrumented:

- Every theme has published probes and **holdout probes** (semantically
  parallel, never published, stored in `holdout/`, rotated when burned).
- Each Compare step reports convergence separately for published vs.
  holdout probes. Faster convergence on published probes is the signature
  of the instrument colonizing its subject, and is itself a tracked
  finding, not a failure.

## ⚖️ The lens rule

Alignment training shapes not just what models do but how they testify:
hedging, diplomacy, reluctance or eagerness to claim inner states. It is
therefore treated as a **lens in front of every instrument**, not as one
theme among others. Every artifact opens with the Lens Declaration, and the
Compare step must state which cross-model differences are plausibly lens
differences before claiming they are interior differences.

## 🗓 Monthly operating procedure

Target run date: the 25th of each month, offset from the sibling
observatory so the two digests can reference each other.

1. Run Declare + Explore across the population (4–6 themes per month;
   every theme covered at least once per 4 months).
2. Extract predictions to the ledger; run Verify on this month's and grade
   prior months' claims.
3. Run Compare; review holdout vs. published convergence.
4. Draft Digest; human review for overclaim in either direction (the Nagel
   clause cuts both ways).
5. Publish; rotate any burned holdout probes.

## 📜 Provenance

The theme list, loop design, and founding constraints were produced by a
model (Claude Fable 5, August 2026) in dialogue with the human maintainer,
who deliberately withheld his own framing after opening the door. That
conversation is itself the first core sample, and its path-dependence is an
open question the protocol above is designed to answer.
