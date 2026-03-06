# Canonical Routing Index (Hodge)

This file is the single routing map for where each proof package lives in:

- main preprint sections,
- mirror note files,
- certificate/artifact keys.

## Gate Routing

| Gate | Main preprint location | Mirror note | Registry/artifact key(s) |
|---|---|---|---|
| `H_G1` (coercivity) | `Section 4/5` (`HOD1`) | `notes/EG1_public.md` | `kappa_hodge` |
| `H_G2` (capture) | `Section 4/5` (`HOD2`,`HOD3`) | `notes/EG2_public.md` | `sigma_capture`, `sigma_star_can` |
| `H_G3` (compactness/no-Zeno) | `Section 5` (`HOD4`) | `notes/EG3_public.md` | `kappa_compact` |
| `H_G4` (rigidity) | `Section 5` (`HOD5`) | `notes/EG4_public.md` | `rho_rigidity` |
| `H_G5` (identification lock) | `Section 5` (`HOD7`) | `notes/IDENTIFICATION_BRIDGE.md` | `alpha_alg` |
| `H_G6` (algebraicity floor) | `Section 5` (`HOD8`) | `notes/EG4_public.md` | `a_floor` |
| `H_GCoh` (strict coherence) | `Sections 3/4` | `notes/IDENTIFICATION_BRIDGE.md` | `eps_coh` |
| `H_GM` (final strict margin) | `Section 3` margin formula | derived | all above keys |

## Repro Routing

| Artifact | Path |
|---|---|
| Runner | `repro/run_repro.sh` |
| Guard | `scripts/hodge_closure_guard.py` |
| Runtime certificate | `repro/certificate_runtime.json` |
| Baseline certificate | `repro/certificate_baseline.json` |
| Registry | `artifacts/constants_registry.json` |
| Stitch constants | `artifacts/stitch_constants.json` |
| Third-party rerun protocol | `repro/THIRD_PARTY_RERUN_PROTOCOL.md` |
