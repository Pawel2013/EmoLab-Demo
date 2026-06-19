# EmoLab Affective-Cognitive Agent

## 1. Purpose

The EmoLab affective-cognitive agent transforms selected synchronized telemetry into a structured analytical report.

Its purpose is to help a human reviewer reason about temporal structure, cross-channel relationships, uncertainty, and possible mechanisms without collapsing heterogeneous model outputs into a single unqualified label.

The agent is not a diagnostic system and does not claim direct access to a person's internal state.

---

## 2. Inputs

Depending on the session, the agent may receive selected information derived from prosody, language, vocal events, transcript structure, speakers, temporal windows, cross-channel agreement indicators, Emotion Pulses summaries, valence/arousal summaries, and session metadata.

The quality of the report depends on the quality, completeness, and temporal precision of the input telemetry.

---

## 3. Report Structure

A report can include:

- **Affective background** — dominant recent or global patterns;
- **Phase model** — temporal decomposition into interpretable phases;
- **Turning points** — candidate mechanism changes;
- **Leading indicators** — evidence appearing before a turning point;
- **Cross-channel conflicts** — disagreements between modalities;
- **Working hypotheses** — explicit interpretations with confidence levels;
- **Unknowns and indeterminacies** — unresolved questions;
- **Evidence-grounding audit** — whether claims are phase-specific or global-only.

---

## 4. Evidence and Inference Separation

```text
observed model output
        ↓
temporally aligned evidence
        ↓
cross-channel relationship
        ↓
working hypothesis
        ↓
confidence level
        ↓
unknowns and human review
```

A generated hypothesis should not be presented as if it were a directly observed fact.

---

## 5. Representative Analytical Pattern

A report may identify prosody emphasizing concentration or determination while language emphasizes confusion or uncertainty. It may then describe a later shift toward contemplation and identify a possible turning point preceded by a brief change in arousal.

The report can formulate a hypothesis about effortful cognitive focus while also recording alternative explanations and unresolved uncertainty.

---

## 6. Confidence and Unknowns

The agent can assign qualitative confidence levels such as high, medium, and low.

Confidence reflects the available evidence, not certainty about a person's internal state.

Unknowns may include missing temporal granularity, absent modalities, uncertain speaker attribution, unclear causes of disagreement, technical artefacts, or limited contextual knowledge.

---

## 7. Audit-Oriented Design

The report may explicitly indicate whether a claim is phase-grounded:

```text
Phase-grounded evidence: YES
Supporting timestamps: available
```

or:

```text
Phase-grounded evidence: NO
Supporting timestamps: unavailable
Interpretation relies on global summary only
```

This makes unsupported extrapolation easier to detect.

---

## 8. Human Review

A reviewer should be able to inspect the source session, navigate to timestamps, compare the report with model outputs, challenge the interpretation, reject unsupported hypotheses, and record alternatives.

---

## 9. Limitations

The agent may inherit errors from telemetry, overinterpret weak signals, omit context, generate plausible but incorrect explanations, or express excessive confidence.

Its output must not be treated as psychological ground truth.

---

## 10. Representative Output Structure

```text
0) Affective Background
1) Phase Model
2) Turning Points
3) Cross-Channel Conflicts
4) Working Hypotheses
5) Unknowns / Indeterminacies
```
