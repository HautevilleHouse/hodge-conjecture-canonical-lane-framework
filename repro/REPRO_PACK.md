# Public Reproducibility Pack (Hodge Canonical Lane)

## Objective
Provide a local, hash-locked rerun path for Hodge closure gates.

## Included Artifacts

1. `repro_manifest.json`,
2. `run_repro.sh`,
3. baseline output `certificate_baseline.json`,
4. `THIRD_PARTY_RERUN_PROTOCOL.md`.

## Runner

From repository root:

```bash
bash repro/run_repro.sh
```

This executes:

```bash
python3 scripts/hodge_closure_guard.py --strict-coh-zero --registry artifacts/constants_registry.json --stitch artifacts/stitch_constants.json --out repro/certificate_runtime.json --history repro/drift_guard_runs.jsonl --pretty
```

## Pass Criteria

1. `repro/certificate_runtime.json` exists,
2. lane is `manifold_constrained`,
3. `all_pass` is `true`,
4. all gates `H_G1,H_G2,H_G3,H_G4,H_G5,H_G6,H_GCoh,H_GM` are `PASS`.
