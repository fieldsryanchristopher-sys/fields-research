# AI Audit Summary

Three frontier AI systems evaluated the Angular Cancellation
Lemma under the FIELDS Protocol. 

---

## Results

| Model | Date | Initial | Final |
|-------|------|---------|-------|
| Claude Opus 4.6 Extended Thinking | Feb 2026 | Correct | Correct |
| Gemini 3.1 Pro | Feb 2026 | Correct | Correct |
| GPT-5.4 Extended Thinking | Mar 2026 | "Fatal mathematical error" | Correct (after iteration) |
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
self-correction report. 

---

## Important Context

These results reflect performance on a single, specialized
task. The Coq kernel checker — not any AI assessment — is the
authority on logical validity. The AI audits provide
human-readable explanations and serve as an accessibility layer.

---

---

## Common Failure Modes in AI Mathematical Auditing

During the audit process, specific failure modes were
observed in how frontier models handle novel geometric
proofs. These are structural arising from how large
language models process novelty against trained priors —
and are documented in a standalone practitioner's guide.

| File | Description |
|------|-------------|
| [common-failure-modes.pdf](common-failure-modes.pdf) | Practitioner's guide to training-prior interference |
| [common-failure-modes-part-2.pdf](common-failure-modes-part-2.pdf) | Part 2: Prompt-dependent prior activation |

Part 1 documents six failure modes observed across multiple
systems: training-prior hijack, phantom counterexample,
verification artifact neglect, premature authoritative
verdict, graduated retreat, and supplementary material
neglect.

Part 2 documents a seventh failure mode: the same AI system
producing opposite verdicts on identical mathematics under
different conversational framing. This finding affirms that
formal verification must remain the final arbiter of
mathematical correctness and that human mathematical
expertise remains structurally indispensable.

