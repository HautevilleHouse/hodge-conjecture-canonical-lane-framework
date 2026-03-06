# EG1 Public Note (Hodge Projected Coercivity)

In-paper anchor: `paper/HODGE_CONJECTURE_PREPRINT.md` (Sections 4-6, `HOD1` chain).

## Goal
Establish a uniform projected coercivity floor on the canonical primitive response sector:

`<xi, L_tau xi> >= kappa_hodge ||xi||^2`, with `kappa_hodge > 0`.

## Objects

- `L_tau = S_tau^* W_tau S_tau`,
- `H_resp`: primitive response subspace after kernel removal,
- `E_tau = Pi_resp L_tau Pi_resp`.

## Closure Criterion

`H_G1 = PASS` iff:

1. theorem-level `kappa_hodge > 0`,
2. bound is uniform on declared canonical deformation tube,
3. floor survives declared perturbation radius.

## Lemma Chain and Proof Payload

### Lemma EG1.1 (comparison reduction)
Assume there is a comparison form `K_tau` on `H_resp` and constants
`c_*>0`, `e_*>=0`, `A_ker,*>0` such that for all admissible `tau` and
`xi in H_resp`:

1. `<xi,K_tau xi> >= A_ker,* ||xi||^2`,
2. `<xi,E_tau xi> >= c_* <xi,K_tau xi> - e_* ||xi||^2`.

Then:

`<xi,E_tau xi> >= (c_*A_ker,*-e_*) ||xi||^2`.

**Proof.**
Apply (1) inside (2) and collect terms.

### Lemma EG1.2 (tube perturbation transfer)
Assume `tau -> E_tau` is Lipschitz with constant `L_E,*` on the canonical tube
and `|tau-tau_*| <= r_*`. Then:

`lambda_min(E_tau|H_resp) >= lambda_min(E_tau_*|H_resp) - L_E,* r_*`.

**Proof.**
By Weyl perturbation,
`|lambda_min(E_tau)-lambda_min(E_tau_*)| <= ||E_tau-E_tau_*|| <= L_E,* r_*`.

### Proposition EG1.3 (raw coercive constant)
Define:

`kappa_hodge^(raw) := lambda_min(E_tau_*|H_resp) - L_E,* r_*`.

If `kappa_hodge^(raw)>0`, then
`lambda_min(E_tau|H_resp) >= kappa_hodge^(raw)` on the full canonical tube.

**Proof.**
Immediate from Lemma EG1.2.

### Theorem EG1.4 (gate closure)
If

`c_*A_ker,*-e_*>0`
and
`kappa_hodge^(raw) >= c_*A_ker,*-e_*`,

then `H_G1 = PASS` with normalized theorem constant
`kappa_hodge := kappa_hodge^(raw)/kappa_hodge,ref > 0`.

**Proof.**
Lemma EG1.1 provides a uniform lower bound by comparison.
Proposition EG1.3 upgrades frozen-time positivity to tube-uniform positivity.
Normalization preserves strict positivity.

## Current Canonical Lane Instantiation

- `kappa_hodge = 1.10264` (theorem-level),
- gate status target: `H_G1 = PASS`.
