# Read the Result Your Way

This repository contains a machine-verified mathematical result
about the Navier–Stokes equations — the Angular Cancellation
Lemma. You can explore it with the help of any frontier AI
system.

**How it works:** Pick the journey below that sounds like you.
Copy the prompt underneath it. Open your preferred AI (Claude,
Gemini, ChatGPT, or any model with long-context capability).
Upload the PDF manuscript and the three Coq files (.v, .vo,
.glob) from this repository. Paste the prompt. The AI becomes
your personal guide through the result, tuned to what you
actually want to know.

---

## Journey 1 — "Just Tell Me: Is It Right or Wrong?"

**This one's for you if:** You're a mathematician, a PDE
researcher, or someone who reads proofs for a living. You don't
need motivation or analogies. You want the axiom inventory, the
proof chain, the trust boundary, and a straight answer.

**What you'll get:** A blunt, technical audit. The AI will trace
every step of the Coq formalization, cross-reference it against
the analytical arguments in the paper, identify exactly what's
proved versus what's assumed, check the exponent accounting, and
give you a direct verdict. No hedging. No hand-holding.

> **Copy this prompt:**
>
> I'm a working mathematician. I've uploaded the Angular
> Cancellation Lemma manuscript and its Coq formalization.
> Read the full PDF and the complete .v source file. Give me
> a rigorous audit: axiom inventory, the full proof chain from
> factor_A through angular_cancellation_lemma, the trust
> boundary at per_mode_res_bound and whether the analytical
> arguments in Section 4.5 justify it, exponent accounting,
> and your honest verdict on correctness. Tell me precisely
> what is proved, what is assumed, and what remains open.
> Be direct.

---

## Journey 2 — "What Even Is This?"

**This one's for you if:** You're curious. Maybe you saw a
headline, maybe someone sent you a link, maybe you just like
learning things. You don't have a math background and you're
not pretending to. You want to understand what this is and why
people are excited about it.

**What you'll get:** A warm, jargon-free walkthrough. The AI
will explain what the Navier–Stokes equations are, why there's
a million-dollar prize attached to them, what this result found,
and what it means that a computer verified every step. It'll be
honest about what this doesn't solve. You'll come away
understanding the big picture and feeling like you belong in the
conversation — because you do.

> **Copy this prompt:**
>
> I have zero math background but I'm genuinely curious. I've
> uploaded a paper called the Angular Cancellation Lemma and
> its Coq proof files. Explain this to me from the ground up —
> what are the Navier–Stokes equations, why do they matter,
> what's the million-dollar prize, what did this paper find,
> and what does it mean that a computer checked the proof. Use
> the paper's own analogies where they help. Be honest about
> what it doesn't solve. Talk to me like a smart friend, not
> a student.

---

## Journey 3 — "What Does This Mean for the Real World?"

**This one's for you if:** You work in policy, government,
defense, infrastructure, or science funding. You need to know
if the math checks out, and then you need to know what changes.
What does this mean for the software your agencies use? What
does it mean that an independent researcher did this with AI?
What should you be paying attention to?

**What you'll get:** A briefing. The AI will confirm the
mathematical soundness quickly, then focus on concrete
implications — for computational fluid dynamics and turbulence
modeling, for independent scientific production, and for what
formal verification offers over traditional peer review.
Practical, direct, focused on what matters for your world.

> **Copy this prompt:**
>
> I work in policy and need a briefing. I've uploaded the
> Angular Cancellation Lemma manuscript and its Coq
> formalization. First, confirm whether the mathematics is
> sound. Then focus on implications: what does the cascade
> locality result mean for computational fluid dynamics used
> in civilian applications, aerospace, and weather modeling? What does it
> mean for startup categories? What does machine verification offer that
> traditional peer review doesn't? Be concrete and practical.

---

## Journey 4 — "What Does This Mean for AI?"

**This one's for you if:** You work in AI — as a researcher,
engineer, investor, or journalist. You want to know what the
human-AI collaboration actually looked like, what the FIELDS
Protocol is as a methodology, and what the AI audit results
reveal about where frontier models are right now in mathematical
reasoning.

**What you'll get:** A technical but narrative-driven analysis.
The AI will walk you through the collaboration methodology, what
it means that the Coq formalization compiled on first pass, how
the FIELDS Protocol works as an evaluation framework, and what
the model comparison results show. Fair to all models discussed.
Honest about what this is — a single extraordinary data point —
and what it signals.

> **Copy this prompt:**
>
> I'm in the AI industry. I've uploaded the Angular
> Cancellation Lemma manuscript and its Coq formalization.
> After confirming the math is sound, focus on the AI story:
> how was human-AI collaboration used to develop this result?
> What does it mean that the Coq formalization compiled on
> first pass? What is the FIELDS Protocol as a methodology
> for evaluating AI mathematical reasoning? If the paper
> includes AI audit transcripts, walk me through the model
> comparison results — be precise, be fair, and frame it as
> what it is. What does this signal about where AI-assisted
> mathematics is headed?

---

## Journey 5 — "Where Do We Go from Here?"

**This one's for you if:** You're a researcher — PDE analysis,
formal methods, turbulence theory, or a graduate student looking
for a problem worth your time. You want to know what's genuinely
new, what's open, and where the most promising paths forward are.

**What you'll get:** A collaborator's assessment. The AI will
evaluate novelty against existing literature, then focus on the
open problems: the enstrophy gap, why five closure approaches
failed, which research directions are most promising, what it
would take to formalize the remaining hypothesis in Coq, and
where this work should be published. 
The kind of conversation you'd have over a whiteboard.

> **Copy this prompt:**
>
> I'm a researcher looking for my next problem. I've uploaded
> the Angular Cancellation Lemma manuscript and its Coq
> formalization. Assess what's genuinely novel here relative
> to existing PDE literature. Then go deep on the enstrophy
> gap in Section 4.6 — what does closure actually require,
> why did each of the five approaches in Remark 4.31 fail,
> and which research directions are most promising? What
> would it take to formalize per_mode_res_bound in Coq?
> Where should this be published and which communities need
> to see it? Talk to me like a collaborator.
