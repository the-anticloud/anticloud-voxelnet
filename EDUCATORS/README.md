# Educators — VOXELNET

**Project:** VOXELNET  
**Category:** VOXELIZATION  
**Upstream:** see BENCH.json  
**Pinned commit:** `fc3f2ccffc713ae4a1bafa7765fa6a60a1b72c35`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `06866d94a88909fc0bf3ea4603a990e15784ba41ee1a20e3f83a6c7302ce4310`  
**Date:** October 2026

## Teaching with VOXELNET

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `06866d94a88909fc0bf3ea4603a990e15784ba41ee1a20e3f83a6c7302ce4310` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
