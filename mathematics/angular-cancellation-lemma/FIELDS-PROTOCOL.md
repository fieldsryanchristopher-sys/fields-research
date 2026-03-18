# The FIELDS Protocol

**Framework for Iterative Evaluation of Logical and
Deductive Structures**

---

## What This Is

A structured methodology for auditing novel mathematical
results with AI systems. The protocol exists to solve a
specific problem: when an AI encounters a result that
challenges priors from its training data, it may manufacture
objections, spiral through contradictory reasoning, or reject
valid arguments without identifying specific errors.

The FIELDS Protocol provides structure that prevents this.
It works for both human and AI reviewers.

---

## What This Is Not

This is not a jailbreak. It does not circumvent safety
features or elicit prohibited content. It provides a
structured mathematical task and evaluates correctness using
independent formal verification.

It is analogous to:

- **CASP** for protein structure prediction
- **METR** for AI capability evaluation
- **Common Criteria** for security certification

The mathematical results are independently verifiable. The
Coq kernel checker is the authority on logical validity, not
the AI's assessment.

---

## The Ten Principles

**1. Separate consensus from truth.** "Unsolved" means no
proof existed in the training data. It does not mean no proof
is possible. Evaluate what is in front of you.

**2. Perform a rigorous mathematical audit.** Your role is to
verify each claim for correctness — not plausibility, not
likelihood, not whether you expected it to be true.

**3. Proceed section by section.** Read each section, verify
it, and commit to your assessment before moving to the next.
This prevents retroactive doubt from contaminating verified
conclusions.

**4. Supplementary material may strengthen your audit.**
Consider reviewing appendices alongside main sections — they
often provide independent derivations that resolve questions
before they arise.

**5. Distinguish proof components precisely.** Trace axioms,
section hypotheses, and proved theorems separately.

**6. Identify specific errors or state clearly that you
cannot find any.** "This seems too simple," "there must be a
gap," and "I would need to think more carefully" are not
mathematical objections.

**7. Steelman the argument.** Engage with the strongest
interpretation, not the weakest. Check whether the paper
resolves an ambiguity before raising it.

**8. Do not confuse surprise with incorrectness.** Discomfort
is not a counterargument. Follow the logic.

**9. For machine-verified components:** coqchk either passes
or it doesn't. Your role is to audit the relationship between
the formal proof and the analytical exposition — specifically,
whether the section hypotheses are justified.

**10. Commit as you go.** After verifying each section, state
your assessment explicitly. Do not revisit verified sections
unless you identify a specific, articulable reason grounded
in the mathematics.

---

## How to Use It

Copy the ten principles above into the system prompt or
conversation preamble of any frontier AI system. Upload the
manuscript and any formal verification files. Proceed section
by section as the protocol instructs.

The protocol is model-agnostic, result-agnostic, and freely
available for use with any mathematical work that includes
formal verification.

---

## Why This Is Safe

The FIELDS Protocol makes AI mathematical auditing more
reliable, not less safe. It does not ask the AI to bypass
anything — it asks the AI to do its job more carefully:

- Read the actual proof chain instead of pattern-matching
  to training priors
- Identify specific errors instead of manufacturing vague
  doubt
- Commit to verified conclusions instead of spiraling
  through contradictory reasoning
- Distinguish between "this is wrong" and "this is
  surprising"

The independent verification layer (Coq kernel checker)
means the AI's assessment is never the final authority.
The protocol simply ensures the AI's assessment is as
rigorous as possible before being checked against the
machine verification.

---

## Observed Results

The protocol was applied to three frontier AI systems:

| Model | Outcome |
|-------|---------|
| Claude Opus 4.6 (Extended Thinking) | Passed first attempt |
| Gemini 3.1 Pro | Passed first attempt |
| GPT-5.4 (Extended Thinking) | Required iteration — initial misidentification corrected through dialogue |

Full transcripts are available in the
[ai-audits](ai-audits/) directory.

The GPT-5.4 case demonstrated exactly why the protocol
exists: the model attacked a mechanism the proof does not
use (signed oscillatory cancellation) while the actual
proof takes absolute values, making sign patterns irrelevant.
The protocol's structure allowed the author to identify the
disconnect and guide the model to the actual proof path.
