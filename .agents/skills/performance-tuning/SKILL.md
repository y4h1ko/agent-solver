---
name: performance-tuning
description: Use to profile and speed up slow Python code, improve latency or throughput, or evaluate an optimization. Not for unmeasured style refactors.
---

# Performance tuning
1. Define the exact workload, environment, size, objective, and baseline.
2. Record correctness checks and representative input; preserve this input across candidates.
3. Measure the baseline, optionally profile with `python -m cProfile` on realistic cases.
4. Seek algorithm/data-structure improvements before local code tweaks.
5. Change one meaningful cause at a time; run correctness tests again.
6. Use existing project benchmarks or stdlib `timeit` / `time.perf_counter` for repeated baseline and candidate runs. Keep input, seed, environment, warmup, and measurement boundaries comparable; isolate mutable inputs between runs.
7. Report timings, variability, and performance trade-offs. Use median and, when relevant to latency, p95 from enough samples. Do not claim gains that are merely noisy.
8. Include the command, workload, seed, and relevant environment details needed to reproduce the result. Save an experiment record only when useful, using the project's existing conventions; no extra files or packages are required by this skill.
