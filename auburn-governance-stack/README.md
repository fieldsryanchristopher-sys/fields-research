# Auburn Governance Stack

A layered architecture comprising 45 documents across 7 layers
for verifiable AI governance.

Follows the structural logic of the TCP/IP protocol stack:
standardize the composition layer, allow unrestricted innovation
above and below, enforce binary conformance through a public
test suite.

---

## Architecture

- [AGS-1 — Architecture Specification](ags-1/)
- [Master Architecture Plan](master-architecture/)

---

## Layer 0 — Foundation

- [Rails: A Governance Protocol for AI](layer-0/rails/)

---

## Threat Surface

- [The Compound Threat Matrix](threat-surface/compound-threat-matrix/)
- [The Stateful Isolation Law](threat-surface/stateful-isolation-law/)

---

## Layer 2 — Model State Health

The five mandatory invariants carried in the MAI-1 attestation
payload.

| Clause | Invariant | Domain |
|--------|-----------|--------|
| AI-2 | [Gradient Starvation Envelope](layer-2-invariants/ai-2-gradient-starvation/) | MoE training |
| AI-4 | [SRAM Thermal Integrity Bound](layer-2-invariants/ai-4-sram-thermal/) | Hardware |
| AI-6 | [Distribution Drift Bound](layer-2-invariants/ai-6-distribution-drift/) | Output monitoring |
| AI-7 | [Structural Coherence Bound](layer-2-invariants/ai-7-structural-coherence/) | Representational health |
| AI-8 | [Entropy-Collapse Constraint](layer-2-invariants/ai-8-entropy-collapse/) | Multi-agent diversity |

---

## Layer 3 — Attestation Interface

- [MSAF — Model State Attestation Framework](layer-3-attestation/msaf/)
- [MAI-1 — Model Attestation Interface](layer-3-attestation/mai-1/)
- [MoE Routing Attestation](layer-3-attestation/moe-routing/)
- [Lyapunov Stability for Speculative Decoding](layer-3-attestation/lyapunov-speculative-decoding/)

---

## Layer 4 — Enforcement

- [CTS-1: MAI-1 Conformance Test Suite](layer-4-enforcement/cts-1/)

---

## Composition Layer

- [CRSA-1 — Compositional Runtime Safety Attestation](composition-layer/crsa-1/)
- [CRSA-1 EU Edition](composition-layer/crsa-1-eu/)
- [Autonomous Agents in Financial Services](composition-layer/autonomous-agents-financial/)
