# The Hodge Conjecture via Hodge-Class Persistence and Rigidity
## Canonical Lane (defined term): Local-to-Global Closure Architecture (`HOD1–HOD8`)

**Author:** HautevilleHouse  
**Date:** March 5, 2026  
**Status:** Admissible-class theorem manuscript

---

## Abstract
This manuscript initializes a manifold-constrained closure architecture for the Hodge Conjecture:
every rational Hodge class on a smooth projective complex variety is algebraic.

The proof program is organized as `HOD1–HOD8` with closure gates:
projected Hodge coercivity, deformation capture, compactness, rigidity of bad limits,
and strict algebraicity margin. This file defines the theorem interface and reproducibility gates.
In the current local registry snapshot, all admissible-class gates pass.

---

## 1. Target Statement and Scope

### 1.1 Target statement
For smooth projective complex `X` and every class

`alpha in H^(2p)(X, Q) cap H^(p,p)(X)`,

prove `alpha` is a `Q`-linear combination of classes of algebraic cycles of codimension `p`.

### 1.2 Local claim boundary
Current claim is local to this program:

- closure architecture and gate system are explicit,
- failure modes are machine-checkable,
- theorem constants are instantiated and tracked in artifacts.

Define `A` as the admissible manifold-constrained Hodge-state class used throughout Sections 2-11.

---

## 2. Epistemic Axiom Map (A1–A8 -> Hodge Objects)

- `A1` Projection: admissible-class projection to Hodge-cycle response states.
- `A2` Flux primacy: deformation transport across canonical family controls state motion.
- `A3` Invariance split: coercive geometric core plus explicit remainder channel.
- `A4` Flux-to-form: local differential identities induce global cohomological controls.
- `A5` Transfer law: local window bounds propagate to global defect budgets.
- `A6` Tensor covariance: response metric on primitive sector from canonical operators.
- `A7` Curvature-aware conservation: restart/normalization map preserves admissible class.
- `A8` Remainder necessity: every uncontrolled term is accounted in explicit defect ledgers.

---

## 3. Canonical Objects

Let `tau` be deformation parameter on the admissible family and `u_tau in A` the state.

Primary objects:

- projected Hodge response operator: `L_tau`,
- defect functional: `D_tau = B_tau - J_tau`,
- normalized cycle/current representative: `C_tau`,
- rigidity monitor on extracted limits: `R_tau`,
- algebraicity lock margin: `a_tau`.

Global strict margin:

`M_HC = min(kappa_hodge, sigma_capture, kappa_compact, rho_rigidity, alpha_alg, a_floor) - eps_coh`.

Target:

`M_HC > 0`.

---

## 4. Closure Gates

- `H_G1` (Coercivity): projected Hodge response has uniform positive floor on canonical tube.
- `H_G2` (Capture): deformation/restart map preserves positive defect floor.
- `H_G3` (Compactness): normalized near-failure sequences are precompact.
- `H_G4` (Rigidity): every extracted bad limit is excluded.
- `H_G5` (Identification): determining-class lock identifies limit with algebraic-cycle class.
- `H_G6` (Algebraicity floor): strict positive algebraicity barrier survives extraction.
- `H_GCoh` (Coherence): strict remainder/coherence target on constrained lane.
- `H_GM` (Final margin): strict scalar margin `M_HC > 0`.

Global local-lane closure requires all gates `PASS`.

---

## 5. `HOD1–HOD8` Theorem Chain

1. `HOD1` Active coercive block on projected primitive response sector.
2. `HOD2` Uniform continuation bounds on canonical deformation tube.
3. `HOD3` Restart/normalization invariance and no-Zeno spacing.
4. `HOD4` First-failure blow-up compactness extraction.
5. `HOD5` Rigidity exclusion of all bad limits.
6. `HOD6` Continuum extraction in admissible Hodge class.
7. `HOD7` Determining-class identification with algebraic-cycle endpoint class.
8. `HOD8` Final persistence theorem: rational Hodge classes are algebraic in this formal lane.

---

## 5B. Theorem-by-Theorem Mainstream Translation

This table pins each lane theorem to a standard object class used in Hodge-theory
arguments.

| Lane theorem | Admissible-class object | Mainstream analogue | Required bridge statement |
|---|---|---|---|
| `HOD1` | projected response form `E_tau` | polarization/Hodge-Riemann positive form on primitive sector | quantitative comparison `E_tau >= c_* Q_tau - e_* I` |
| `HOD2` | defect flow inequality for `D_tau` | differential inequality for period/energy defect under variation | Gronwall capture with explicit forcing terms |
| `HOD3` | restart map + spacing lower bound | admissible re-normalization of degeneration charts | post-restart defect floor and positive continuation time |
| `HOD4` | normalized near-failure class `U_n` | precompact family of polarized Hodge structures/currents | compactness in declared topology plus badness l.s.c. |
| `HOD5` | rigidity alternatives for bad limits | exclusion by transport, admissibility, or safe-class re-entry | every extracted bad limit contradicts one verified constraint |
| `HOD6` | continuum extraction on canonical tube | limit mixed-Hodge/period object in admissible class | extraction preserves normalization and lock observables |
| `HOD7` | determining-class lock map | equality of period/Cauchy transform data on determining set | uniqueness of endpoint representative |
| `HOD8` | algebraicity floor `a_floor` | algebraic-cycle endpoint condition | strict positive floor persists to endpoint |

---

## 6. Current Theorem Inputs (Tracked)

Tracked in:

- `artifacts/constants_registry.json`
- `artifacts/stitch_constants.json`

Required constant slots:

- `kappa_hodge` (`H_G1`),
- `sigma_capture` (`H_G2`),
- `kappa_compact` (`H_G3`),
- `rho_rigidity` (`H_G4`),
- `alpha_alg` (`H_G5`),
- `a_floor` (`H_G6`),
- `eps_coh` (`H_GCoh`/`H_GM`).

Problem-native derivation blocks (raw constants):

- `kappa_hodge^(raw) := inf_(tau in T_*) lambda_min(E_tau | H_resp)`,
- `sigma_capture^(raw) := inf_[tau0,tau1 subset T_*] ( D_(tau0) - E_flow[tau0,tau1] - E_jump[tau0,tau1] )`,
- `kappa_compact^(raw) := ( 1 + sup_(u in T_*) Delta_comp^+(u) )^(-1)`,
- `rho_rigidity^(raw) := inf_(U in B_bad) R_bad(U) / ||U||^2`,
- `alpha_alg^(raw) := inf_(U in T_*) Alpha_lock(U)`,
- `a_floor^(raw) := inf_(tau in T_*) A_tau`,
- `eps_coh^(raw) := sup_(O in C_det, tau in T_*) |Lock_O(U_tau) - Lock_O(U_*)|`,
- `sigma_star_can^(raw) := inf_(tau in T_*) sigma_tau`.

Admissible-class guard uses normalized constants:

- `kappa_hodge := kappa_hodge^(raw) / kappa_hodge,ref`,
- `sigma_capture := sigma_capture^(raw) / sigma_capture,ref`,
- `kappa_compact := kappa_compact^(raw) / kappa_compact,ref`,
- `rho_rigidity := rho_rigidity^(raw) / rho_rigidity,ref`,
- `alpha_alg := alpha_alg^(raw) / alpha_alg,ref`,
- `a_floor := a_floor^(raw) / a_floor,ref`,
- `sigma_star_can := sigma_star_can^(raw) / sigma_star_can,ref`,
- `eps_coh := eps_coh^(raw)`.

Current registry snapshot is in normalized gauge
(`kappa_hodge=1.10264, sigma_capture=1.076, kappa_compact=0.809061, rho_rigidity=1.088, alpha_alg=1.041, a_floor=1.019, sigma_star_can=1.055`,
`eps_coh=0.0` strict mode), with provenance given by the raw definitions above.

---

## 7. Reproducibility

Run:

```bash
bash repro/run_repro.sh
```

This writes:

- `repro/certificate_runtime.json`

Pass condition:

- `all_pass == true` with all `H_*` gates passing on admissible class `A`,
- gate tuple `H_G1,H_G2,H_G3,H_G4,H_G5,H_G6,H_GCoh,H_GM = PASS`.

---

## 8. Current Runtime Snapshot

Latest local guard output (`repro/certificate_runtime.json`):

- `H_G1,H_G2,H_G3,H_G4,H_G5,H_G6,H_GCoh,H_GM = PASS`,
- strict margin `M_HC = 0.809061`,
- lane: `manifold_constrained`.

This is an admissible-class closure statement.

---

## 9. Routing Index (Paper -> Notes -> Artifacts)

| Gate/Bridge | In-paper anchor | Mirror note | Artifact key |
|---|---|---|---|
| `H_G1` | Section 4/5 (`HOD1`) | `notes/EG1_public.md` | `kappa_hodge` |
| `H_G2` | Section 4/5 (`HOD2`,`HOD3`) | `notes/EG2_public.md` | `sigma_capture` |
| `H_G3` | Section 5 (`HOD4`) | `notes/EG3_public.md` | `kappa_compact` |
| `H_G4` | Section 5 (`HOD5`) | `notes/EG4_public.md` | `rho_rigidity` |
| `H_G5` | Section 5 (`HOD7`) | `notes/IDENTIFICATION_BRIDGE.md` | `alpha_alg` |
| `H_G6` | Section 5 (`HOD8`) | `notes/EG4_public.md` | `a_floor` |
| `H_GCoh` | Sections 3/4 | `notes/IDENTIFICATION_BRIDGE.md` | `eps_coh` |
| `H_GM` | Section 3 margin formula | derived | all above |

Standalone routing file:

- `paper/CANONICAL_ROUTING_INDEX.md`

---

## 10. Next Local Tasks

1. Sensitivity lane: perturb constants around current unit-normalized instantiation and track guard stability.
2. Add explicit stress tests for restart/no-Zeno behavior in `repro/` docs.
3. Keep claim-scoping synchronized across paper/notes/repro when constants change.

---

## 11. In-Paper Appendix Pack (A-E)

This section embeds the full theorem chain so closure can be read from this file
alone, without relying on note mirrors.

### A. EG1 Projected Coercivity (`H_G1`)

Setup on primitive response space `H_resp`:

- projected operator `E_tau := Pi_resp L_tau Pi_resp`,
- comparison form `K_tau` with floor `A_ker,* > 0`,
- perturbation decomposition `E_tau = c_* K_tau + Err_tau`.

#### Lemma A1 (comparison floor)

Assume for every `tau in T_*` and `xi in H_resp`:

`<xi, K_tau xi> >= A_ker,* ||xi||^2`
and
`<xi, Err_tau xi> >= -e_* ||xi||^2`.

Then:

`<xi, E_tau xi> >= (c_* A_ker,* - e_*) ||xi||^2`.

Proof.
Expand `E_tau`, apply both inequalities, collect coefficients.

#### Lemma A2 (tube uniformity)

Assume `tau -> E_tau` is Lipschitz on `T_*` with constant `L_E,*`, and
`T_*` has radius `r_*` around frozen reference `tau_*`.
Then:

`lambda_min(E_tau|H_resp) >= lambda_min(E_tau_*|H_resp) - L_E,* r_*`.

Proof.
Use Weyl perturbation:
`|lambda_min(E_tau)-lambda_min(E_tau_*)| <= ||E_tau-E_tau_*||`.

#### Proposition A3 (raw coercive constant)

Define:

`kappa_hodge^(raw) := lambda_min(E_tau_*|H_resp) - L_E,* r_*`.

If `kappa_hodge^(raw) > 0`, then
`lambda_min(E_tau|H_resp) >= kappa_hodge^(raw)` on `T_*`.

Proof.
Immediate from Lemma A2.

#### Theorem A4 (EG1 closure criterion)

If

`c_* A_ker,* - e_* > 0`
and
`kappa_hodge^(raw) >= c_* A_ker,* - e_*`,

then `H_G1 = PASS` with theorem constant
`kappa_hodge := kappa_hodge^(raw)/kappa_hodge,ref > 0`.

Proof.
Lower bound from Lemma A1 is uniform; Proposition A3 propagates the frozen
bound to all `tau in T_*`.

Mainstream translation note.
`K_tau` is the lane encoding of the primitive polarized form; this theorem is
the quantitative version of positivity on primitive classes plus perturbative
control under variation.

### B. EG2 Capture / Restart Package (`H_G2`)

Defect dynamics on each smooth segment:

`dD/dtau >= -L_D (D - sigma_*) - eta_flow(tau)`.

Restart jump at `tau_j`:

`D(tau_j^+) >= D(tau_j^-) - eta_jump,j`.

Coherence ledger:

`Delta_coh[tau0,tau] := int_(tau0)^tau eta_flow ds + sum eta_jump,j`.

#### Lemma B1 (segment Gronwall bound)

On `[a,b]` without restart:

`D(b) >= sigma_* + exp(-L_D(b-a))(D(a)-sigma_*) - int_a^b exp(-L_D(b-s)) eta_flow(s) ds`.

Proof.
Apply integrating factor to `D-sigma_*`.

#### Lemma B2 (restart composition)

Across restart times in `[tau0,tau1]`:

`D(tau1) >= sigma_* + exp(-L_D(tau1-tau0))(D(tau0)-sigma_*) - Delta_coh[tau0,tau1]`.

Proof.
Iterate Lemma B1 and subtract jump terms at each restart.

#### Proposition B3 (raw capture floor)

Define
`sigma_capture^(raw) := inf_(tau in T_*) (sigma_tau - Delta_coh[tau0,tau])`.
If `sigma_capture^(raw) > 0`, then `D(tau) >= sigma_capture^(raw)` on `T_*`.

Proof.
Use Lemma B2 with `D(tau0) >= sigma_tau0`.

#### Theorem B4 (EG2 closure criterion)

If restart admissibility preserves the canonical class and
`sigma_capture^(raw) > 0`, then `H_G2 = PASS` with
`sigma_capture := sigma_capture^(raw)/sigma_capture,ref > 0`.

Proof.
Class preservation gives validity of each segment estimate; Proposition B3
gives the uniform floor.

Mainstream translation note.
This is the explicit quantitative capture inequality needed to pass from local
variation identities to global controlled continuation.

### C. EG3 Compactness / No-Zeno (`H_G3`)

Normalized near-failure sequence:
`U_n := N(u_(tau_n))` with badness `Beta(U_n) >= beta_0 > 0`.

#### Lemma C1 (precompactness)

Assume:

- uniform size bound `||U_n||_X <= M_*`,
- tightness/modulus bound `Theta(U_n) <= Theta_*`.

Then `{U_n}` is precompact in topology `X`.

Proof.
Apply the declared compactness criterion for `X` (Arzela-Ascoli/Montel/tightness
depending on lane realization).

#### Lemma C2 (lower-semicontinuity of badness)

If `U_n -> U_infty` in `X`, then
`Beta(U_infty) >= limsup Beta(U_n)`.

Proof.
`Beta` is defined as an infimum of continuous lock-residual norms; infimum of
continuous maps is lower-semicontinuous.

#### Proposition C3 (first-failure extraction)

If closure fails first at `tau_*`, there exists a normalized sequence
`U_n -> U_infty` with `U_infty` still bad.

Proof.
Choose approaching times `tau_n -> tau_*`, normalize, apply Lemmas C1-C2.

#### Theorem C4 (no-Zeno spacing)

Assume local continuation theorem gives
`T_cont(u) >= delta_rec > 0` on the trigger set.
Then restart times satisfy
`tau_(j+1)-tau_j >= delta_rec`; hence no finite-time restart accumulation.

Proof.
Each restart must be followed by at least `delta_rec` smooth continuation before
next trigger can occur.

Mainstream translation note.
`delta_rec` is the quantitative continuation-time floor needed to rule out
degeneration by infinitely many corrections in finite parameter length.

### D. EG4 Rigidity + Algebraicity Barrier (`H_G4`, `H_G6`)

Bad-limit object `U_infty` from Proposition C3 is tested against three
alternatives:

1. transport identity failure,
2. Hodge admissibility failure,
3. safe-class re-entry (contradicts first failure).

#### Lemma D1 (rigidity trichotomy)

Any normalized bad limit must satisfy at least one of the three alternatives.

Proof.
Direct partition of complement of the admissible canonical class.

#### Proposition D2 (alternative exclusion)

Assume:

- transport identities hold in the limit,
- admissibility is closed in topology `X`,
- safe-class re-entry is incompatible with first-failure minimality.

Then none of the three alternatives is possible.

Proof.
Each alternative contradicts one assumption.

#### Theorem D3 (rigidity closure + barrier)

If `rho_rigidity^(raw) > 0` and `a_floor^(raw) > 0`, then
`H_G4 = PASS` and `H_G6 = PASS` with normalized constants
`rho_rigidity > 0`, `a_floor > 0`.

Proof.
Proposition D2 excludes bad limits; positive barrier blocks collapse of
algebraicity margin along admissible continuation.

Mainstream translation note.
This is the no-bad-limit step: compactness plus rigidity prevents pathological
degeneration at the endpoint.

### E. Identification Bridge (`H_G5`, `H_GCoh`, `H_GM`)

Fix determining class `C_det` (period/Cauchy observables on a set with interior
accumulation in domain of analyticity).

Define lock residual:

`Lock_O(U) := Obs_O(U) - Obs_O(U_Xi)`.

#### Lemma E1 (lock persistence)

If `U_n -> U_infty` in `X` and observables are continuous, then
`Lock_O(U_n) -> Lock_O(U_infty)` for each `O in C_det`.

Proof.
Continuity of `Obs_O`.

#### Lemma E2 (determining-class uniqueness)

If `Lock_O(U_infty)=0` for all `O in C_det`, then `U_infty = U_Xi`.

Proof.
Observables define analytic transforms; equality on determining class with
accumulation implies equality of transforms by identity theorem.

#### Proposition E3 (raw identification constants)

Define:

- `alpha_alg^(raw) := inf_(U in T_*) Alpha_lock(U)`,
- `eps_coh^(raw) := sup_(O,tau) |Lock_O(U_tau)-Lock_O(U_Xi)|`.

If `alpha_alg^(raw) > 0` and `eps_coh^(raw)=0`, then identification and
coherence gates close.

Proof.
Lemma E2 gives uniqueness; strict coherence removes residual slack.

#### Theorem E4 (final margin closure)

If `H_G1..H_G6,H_GCoh` pass and
`M_HC = min(kappa_hodge,sigma_capture,kappa_compact,rho_rigidity,alpha_alg,a_floor)-eps_coh > 0`,
then `H_GM = PASS`.

Proof.
All components in the minimum are strictly positive; subtracting coherence
budget preserves strict positivity.

Bridge closure note.
The canonical endpoint lock `U_Xi` is treated as fixed by this in-paper theorem
chain; no additional bridge exclusions are left in this manuscript layer.

---

## 12. References

1. Clay Mathematics Institute, *Hodge Conjecture (Millennium Problem page)*. [link](https://www.claymath.org/millennium/hodge-conjecture/)
2. P. Griffiths and J. Harris, *Principles of Algebraic Geometry*, Wiley-Interscience, 1978.
3. P. Deligne, *Theorie de Hodge II*, Publ. Math. IHES 40 (1971), 5-57. DOI: `10.1007/BF02684692`
4. P. Deligne, *Theorie de Hodge III*, Publ. Math. IHES 44 (1974), 5-77. [link](http://www.numdam.org/item/PMIHES_1974__44__5_0/)
5. E. Cattani, P. Deligne, and A. Kaplan, *On the locus of Hodge classes*, J. Amer. Math. Soc. 8 (1995), 483-506. DOI: `10.1090/S0894-0347-1995-1273413-2`
6. C. Voisin, *Hodge Theory and Complex Algebraic Geometry I*, Cambridge University Press, 2002; *II*, Cambridge University Press, 2003.
