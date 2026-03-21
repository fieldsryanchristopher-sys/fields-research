# Angular Cancellation Lemma

**A Machine-Verified Geometric Bound on Shell-Local Vortex
Stretching for the 3D Incompressible Navier–Stokes Equations**

---

## What This Proves

The incompressibility constraint on the 3D Navier–Stokes
equations forces a deterministic geometric cancellation in
the triadic energy transfer kernel. On unit-width shells of
the integer lattice, the shell-local vortex stretching satisfies

|VS_j| <= C_ACL * k_j^{7/2} * E_j^{3/2}

improving the standard trilinear estimate by half a derivative.
The bound is unconditional — it holds for arbitrary amplitude
distributions with no assumptions on phase coherence, Fourier
concentration, or data size.

## What This Does Not Prove

Global regularity. The enstrophy equation requires control at
three spatial derivatives. The ACL operates at one. The gap is
k_j^2 — two full spatial derivatives. This gap is the precise
barrier to a proof of global regularity and remains open.

## Machine Verification

Formalized in the Coq proof assistant (v8.20.1) using MathComp
and MathComp-Analysis. Verified through the trusted kernel
checker coqchk.

- **Zero** Admitted statements
- **Twelve** Qed theorems
- **Three** axioms (all Cauchy–Schwarz variants)

SHA-256: `150fc78c3df393e8d1461cd895932582c88896918be5979e6f8c3c5e679555eb`

## Verify It Yourself

**Option 1 — Mac (Coq Platform, recommended)**

Install [Coq Platform 8.20](https://github.com/coq/platform/releases) then:
```bash
git clone https://github.com/fieldsryanchristopher-sys/fields-research.git
cd fields-research/mathematics/angular-cancellation-lemma
/Applications/Coq-Platform~8.20~2025.01.app/Contents/Resources/bin/coqc NavierStokesACL.v
/Applications/Coq-Platform~8.20~2025.01.app/Contents/Resources/bin/coqchk -Q . "" NavierStokesACL
```

**Option 2 — Linux/Windows**
```bash
git clone https://github.com/fieldsryanchristopher-sys/fields-research.git
cd fields-research/mathematics/angular-cancellation-lemma
coqc NavierStokesACL.v
coqchk -Q . "" NavierStokesACL
```

**Option 3 — Docker (platform-independent, slower first run)**
```bash
git clone https://github.com/fieldsryanchristopher-sys/fields-research.git
cd fields-research/mathematics/angular-cancellation-lemma
docker run --rm --platform linux/amd64 -v "$PWD":/work -w /work coqorg/coq:8.20 bash -c "opam install -y coq-mathcomp-analysis coq-hierarchy-builder 2>/dev/null; coqc NavierStokesACL.v && coqchk -Q . '' NavierStokesACL"
```

> Note: Docker option installs dependencies on first run (~10 minutes). Subsequent runs are faster.

Expected output for all options: `Modules were successfully checked`

Confirm zero Admitted:
```bash
grep -c "Admitted" NavierStokesACL.v
```

Expected: `0`

## Developed in Partnership with AI

This result was developed through iterative collaboration
between a human historian and Claude (Anthropic). The Coq
formalization compiled on first submission. The methodology —
human provides geometric insight, AI helps formalize and verify,
proof assistant confirms independently — is documented in the
manuscript and is reproducible.

## Read the Result Your Way

Five guided reading journeys are available, each tailored to a
different audience. Pick the one that fits you, copy the prompt,
upload the files into any frontier AI, and get a personalized
walkthrough.

**[JOURNEYS.md -->](JOURNEYS.md)**

## AI Audit Transcripts

The result was independently evaluated by three frontier AI
systems under the FIELDS validation protocol. Full transcripts
are published.

**[Audit Summary -->](ai-audits/SUMMARY.md)**

| Model | Result | Notes |
|-------|--------|-------|
| Claude Opus 4.6 (Extended Thinking) | Passed | First attempt |
| Gemini 3.1 Pro | Passed | First attempt |
| GPT-5.4 (Extended Thinking) | Passed after iteration | Initial misidentification corrected |

## The FIELDS Protocol

**[FIELDS-PROTOCOL.md -->](FIELDS-PROTOCOL.md)**

## Files

| File | Description |
|------|-------------|
| [paper.pdf](paper.pdf) | Full manuscript |
| [NavierStokesACL.v](NavierStokesACL.v) | Coq source (559 lines) |
| [NavierStokesACL.vo](NavierStokesACL.vo) | Compiled proof object |
| [NavierStokesACL.glob](NavierStokesACL.glob) | Reference file |

## Citation

DOI: [10.6084/m9.figshare.31392684](https://doi.org/10.6084/m9.figshare.31392684)

## License

CC BY-NC 4.0. Commercial use requires separate written
authorization from the author.
