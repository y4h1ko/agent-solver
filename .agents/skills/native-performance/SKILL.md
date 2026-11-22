---
name: native-performance
description: Use only when the user explicitly requests Cython, C++, or native extensions, or approves their use following a performance investigation.
  Do not activate for ordinary Python optimization.
---

# Native Performance Optimization

1. Identify the measured bottleneck and performance target.
2. Confirm algorithmic and pure-Python optimizations are insufficient or native code was explicitly requested.
3. Choose the smallest suitable implementation:
   - Cython for typed CPU loops or C interoperability.
   - C++ for complex native algorithms or existing C++ code.
4. Keep a stable Python-facing API.
5. Minimize Python/native boundary crossings and data copies.
6. Handle memory ownership, exceptions, types, and GIL requirements correctly.
7. Preserve numerical behavior within stated tolerances.
8. Add correctness tests against the Python reference.
9. Benchmark representative workloads, including boundary overhead and memory usage.
10. Report measured gains, build requirements, portability risks, and maintenance costs.
