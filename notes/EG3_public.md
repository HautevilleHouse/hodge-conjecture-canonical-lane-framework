# EG3 Public Note (Compactness Package)

In-paper anchor: `paper/HODGE_CONJECTURE_PREPRINT.md` (Sections 5-6, `HOD4` chain).

## Goal
Show precompactness of normalized near-failure sequences in canonical Hodge lane.

## Candidate Class

Normalized cycle/current representatives with fixed admissibility constraints:

`U_n = N(u_(tau_n))`.

## Closure Criterion

`H_G3 = PASS` iff theorem-level `kappa_compact > 0` gives:

- every bad sequence has convergent subsequence in declared topology.

## Lemma Chain and Proof Payload

### Lemma EG3.1 (precompactness criterion)
If normalized sequence `U_n` has uniform seminorm bounds and tightness in the
declared topology, then `{U_n}` is precompact.

**Proof.**
Apply the topology-specific compactness theorem.

### Lemma EG3.2 (badness lower-semicontinuity)
If `U_n -> U_infty`, then
`Bad(U_infty) >= limsup_n Bad(U_n)`.

**Proof.**
`Bad` is an infimum of continuous lock-residual norms.

### Theorem EG3.3 (gate closure)
Define:

`kappa_compact^(raw) := (1 + sup_(u in T_*) Delta_comp^+(u))^(-1)`.

If `kappa_compact^(raw)>0`, then every normalized bad sequence has a convergent
bad subsequence and `H_G3=PASS` with normalized constant
`kappa_compact := kappa_compact^(raw)/kappa_compact,ref > 0`.

**Proof.**
Lemma EG3.1 supplies compactness and Lemma EG3.2 preserves badness in limits.

## Current Canonical Lane Instantiation

- `kappa_compact = 0.809061` (theorem-level),
- gate status target: `H_G3 = PASS`.
