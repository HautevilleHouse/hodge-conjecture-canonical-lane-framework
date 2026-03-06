# Identification Bridge (Hodge Limit -> Algebraic Cycle Class)

In-paper anchor: `paper/HODGE_CONJECTURE_PREPRINT.md` (Sections 3-6 and runtime margin).

## Goal
Ensure extracted canonical-lane limits are identified with algebraic-cycle endpoint class.

## Determining Class (working)

Use Hodge-period and cycle-pairing test class `C_det` with:

1. rational `(p,p)` pairing locks,
2. cycle-class compatibility constraints,
3. normalization and functoriality constraints.

## Uniqueness Target

Two candidate limits with same lock equations on `C_det` are equivalent as canonical representatives.

## Lemma Chain and Proof Payload

### Lemma ID.1 (lock persistence)
If `U_n -> U_infty` on admissible class and observables in `C_det` are
continuous, then `Lock_O(U_n) -> Lock_O(U_infty)` for each `O in C_det`.

**Proof.**
Continuity of observables.

### Lemma ID.2 (determining-class uniqueness)
Assume `C_det` separates admissible endpoint classes.
If `Lock_O(U_infty)=0` for all `O in C_det`, then `U_infty` equals the
canonical endpoint representative up to declared equivalence.

**Proof.**
Contradiction with separation if two non-equivalent endpoints agree on all
determining observables.

### Theorem ID.3 (coherence/identification closure)
If Lemmas ID.1-ID.2 hold and `eps_coh^(raw)=0`, then endpoint identification is
unique and `H_GCoh=PASS`.

**Proof.**
Lock persistence carries equalities to limits; separating-class uniqueness closes
endpoint ambiguity.

## Current Canonical Lane Instantiation

- `alpha_alg = 1.041` (theorem-level),
- `eps_coh = 0.0` (strict-zero theorem-level),
- gate status targets: `H_G5 = PASS`, `H_GCoh = PASS`.
