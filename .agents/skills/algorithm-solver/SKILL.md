---
name: algorithm-solver
description: Use for competitive programming, algorithm implementation, optimization problems, or code under explicit time and memory limits. Not for ordinary CRUD changes.
---

# Algorithm solver
1. Extract input/output contract, constraints, libraries allowed, and exact objective.
2. Identify brute-force reference and at least one viable optimized approach.
3. Choose the simplest correct complexity. State invariant / proof sketch before implementing if nontrivial.
4. Implement without unrelated modifications; handle empty, degenerate, duplicate, adversarial, and maximum inputs.
5. Build a small oracle where feasible; run deterministic and randomized comparison tests.
6. Check asymptotic time/memory, recursion depth, integer overflow considerations, I/O bottlenecks.
7. For a speed claim, benchmark representative and worst-case sizes, saving inputs/seeds.
8. Return solution, measured verification, complexity, and one outstanding risk if any. No invented success claims.
