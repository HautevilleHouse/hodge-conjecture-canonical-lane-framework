# Scripts

- `hodge_closure_guard.py`: canonical-lane closure gate evaluator for Hodge.

Guard inputs:

- `artifacts/constants_registry.json`
- `artifacts/stitch_constants.json`

Guard output:

- `repro/certificate_runtime.json`

Output schema includes:

- native gate keys (`H_G*`),
- normalized gate layer (`G1..G6,GCoh,GM`) under `normalized`,
- strict pass flags: `all_pass`, `all_pass_normalized`.
