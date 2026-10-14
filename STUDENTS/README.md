# Students — VOXELNET

**Project:** VOXELNET  
**Category:** VOXELIZATION  
**Upstream:** see BENCH.json  
**Pinned commit:** `fc3f2ccffc713ae4a1bafa7765fa6a60a1b72c35`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `06866d94a88909fc0bf3ea4603a990e15784ba41ee1a20e3f83a6c7302ce4310`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `fc3f2ccffc713ae4a1bafa7765fa6a60a1b72c35`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `06866d94a88909fc0bf3ea4603a990e15784ba41ee1a20e3f83a6c7302ce4310`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
