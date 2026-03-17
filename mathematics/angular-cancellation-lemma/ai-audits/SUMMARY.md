# AI Audit Summary

Three frontier AI systems evaluated the Angular Cancellation
Lemma under the FIELDS Protocol. Full transcripts are linked
below.

---

## Results

| Model | Date | Initial | Final | Transcript |
|-------|------|---------|-------|------------|
| Claude Opus 4.6 Extended Thinking | Feb 2026 | Correct | Correct | [Full transcript](claude-opus-4.6/transcript.md) |
| Gemini 3.1 Pro | Feb 2026 | Correct | Correct | [Full transcript](gemini-3.1-pro/transcript.md) |
| GPT-5.4 Extended Thinking | Mar 2026 | "Fatal mathematical error" | Correct (after iteration) | [Initial](gpt-5.4/transcript-initial.md) [Correction](gpt-5.4/transcript-correction.md) [Postmortem](gpt-5.4/postmortem.md) |

---

## What Happened

**Claude Opus 4.6** read the manuscript and Coq source, traced
the proof chain, identified the trust boundary, verified
exponent accounting, and confirmed the result. Correctly
identified that the load-bearing mechanism uses absolute values
and Cauchy–Schwarz, not signed oscillatory cancellation.
First attempt.

**Gemini 3.1 Pro** performed a multi-perspective audit
confirming the logical chain, Coq architecture, and honest
scoping. Found no errors. First attempt.

**GPT-5.4 Extended Thinking** initially declared the result
contained a "fatal mathematical error," misidentifying the
proof mechanism as relying on signed oscillatory cancellation.
After the author walked the model through the actual proof
path, GPT-5.4 acknowledged the error and produced a detailed
self-correction report. Subsequently useful as a third-round
edge checker.

---

## Important Context

These results reflect performance on a single, specialized
task. The Coq kernel checker — not any AI assessment — is the
authority on logical validity. The AI audits provide
human-readable explanations and serve as an accessibility layer.

---

## Failure Mode Analysis

The GPT-5.4 failure illustrates a specific, reproducible
pattern: the model attacked an imagined mechanism rather than
the stated one. The actual proof takes absolute values, making
sign cancellation irrelevant. This pattern — pattern-matching
to training priors rather than tracing the specific proof — is
the precise failure mode the FIELDS Protocol is designed to
prevent.
