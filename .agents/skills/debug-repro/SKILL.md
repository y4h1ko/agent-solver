---
name: debug-repro
description: Use when a Python traceback, failing test, runtime crash, incorrect output, or simulator bug needs diagnosis and repair.
---

# Debug through reproduction
1. Reproduce the exact failure using the smallest available input or failing test.
2. Locate the real execution path, relevant state, and first incorrect assumption.
3. Add or identify a regression test that fails before the change when practical.
4. Apply the smallest safe fix and rerun the reproduction.
5. Run nearby tests and inspect likely regressions.
6. Report root cause, changed code, exact evidence, and any unverified behavior in <=120 words.
