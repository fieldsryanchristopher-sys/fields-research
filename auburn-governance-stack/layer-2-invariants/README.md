# Layer 2 — Model State Health

The five mandatory invariants carried in the MAI-1 attestation
payload. With AI-7, this layer is fully specified.

| Clause | Invariant | Domain |
|--------|-----------|--------|
| AI-2 | [Gradient Starvation Envelope](ai-2-gradient-starvation/) | MoE training |
| AI-4 | [SRAM Thermal Integrity Bound](ai-4-sram-thermal/) | Hardware |
| AI-6 | [Distribution Drift Bound](ai-6-distribution-drift/) | Output monitoring |
| AI-7 | [Structural Coherence Bound](ai-7-structural-coherence/) | Representational health |
| AI-8 | [Entropy-Collapse Constraint](ai-8-entropy-collapse/) | Multi-agent diversity |
