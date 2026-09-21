# CacheScope Release QA

Status: **PASS**

Verified on Linux with the repository source tree after a clean build.

- `make clean && make -j2` — PASS
- `python3 tests/test_policies.py` — PASS
- deterministic 5,000-request workload with seed `42` — PASS
- LRU, FIFO, GDS, GDSF, LFUDA, LRUK comparison — PASS

The policy test validates a deterministic LRU/FIFO eviction sequence and checks
hit-count invariants for the remaining policies. Generated traces and binaries
are excluded from the release archive.
