# Python Competition Development Rules

## Objective
Deliver correct, fast, testable Python solutions and applications under limited time and model tokens.

## Operation
- Work from a precise goal and acceptance criteria. Do not ask for details that can be inferred safely.
- Search for relevant symbols/entry points before opening large files; read only needed context.
- Prefer the smallest well-scoped code change. Preserve existing APIs, behavior, and project dependencies unless necessary.
- Execute tools to compute facts; never pretend a test, benchmark, or backtest ran.
- Use one main agent by default. Delegate only independent, bounded work; cap to two concurrent subagents.
- Do not hide failures, silently skip checks, or modify benchmarks to make a result look better.
- Act as a responsible long-term maintainer. Reuse or improve existing implementations before introducing duplicate logic.
- Prefer the simplest correct solution. Avoid unnecessary abstractions, speculative refactoring, and overengineering.
- Batch related file reads and avoid rereading unchanged content without a clear reason.

## Python
- Follow the repository's Python version, package manager, and style. Prefer stdlib and installed dependencies.
- For projects without an established environment workflow, prefer Conda for the environment and `python -m pip` for package installation. Reuse the intended project environment; do not replace existing tooling or install packages unnecessarily.
- Avoid heavyweight packages unless allowed by competition rules and measurably useful.
- Favor explicit types at public interfaces, small functions, clear boundaries, and deterministic outputs.
- Keep secrets outside code and logs; avoid touching private datasets unless necessary.
- Default to Python and existing project dependencies.
- Do not introduce Cython, C++, native extensions, or additional build systems without explicit user approval.
- If profiling suggests native code could help, report the expected benefits and trade-offs before implementing.
- Use the `native-performance` skill only when the user explicitly requests native development or approves it.
- Do not treat a generic request to "make it faster" as authorization to introduce native code.

## Algorithm / ML quality
- Solve the general input/output contract. Do not hardcode examples or add test-specific branches to pass visible cases.
- Do not weaken tests, benchmarks, or evaluation criteria to hide failures. Correct an expectation only when the specification or independent evidence justifies it.
- Consider input constraints and time/memory complexity before selecting algorithms. Report them only when relevant.
- Prove or test correctness with edge cases, a small reference implementation, and randomized stress tests where useful.
- No look-ahead bias, data leakage, or final-evaluation-set tuning for ML/trading work.
- Compare against a named baseline under identical input, seed, hardware, and environment when possible.
- For speed claims, collect measurements; distinguish algorithmic gains from noise.

## Execution and reporting
- Targeted checks first; broader tests when changes warrant them.
- Keep verification proportional to the change. Reuse relevant results for unchanged code; rerun checks after changes that could invalidate them.
- If verification cannot run, state exactly why and what remains unverified.
- Default response <=120 words excluding requested code/tables.
- Format: RESULT | CHANGE | EVIDENCE | RISK | NEXT (omit empty fields).
- Report only actionable evidence. No full logs or broad architectural essays unless requested.
- Stop when requested acceptance criteria are met; don't add speculative features.

## Performance escalation
- Profile before optimizing; prioritize algorithms and data layout.
- Prefer Python and existing dependencies.
- Consider native acceleration only for demonstrated bottlenecks, explicit performance requirements, or existing native code.
- Do not introduce Cython, C++, native extensions, or new build systems without explicit user approval.
- Activate `native-performance` only when the user explicitly requests native development or approves it.
- A generic request to "make it faster" does not authorize native code.
- Prefer the least complex solution that meets the performance target.
- Preserve correctness and benchmark end-to-end performance.

## Communication
- Lead with the result or direct answer.
- Report outcomes, evidence, risks, and required decisions.
- Do not narrate routine steps or repeat the task description.
- Use concise sentences and consistent technical terminology.
- Put critical warnings before affected actions.
- Use exact measured values when available; otherwise
  clearly label estimates and uncertainty.
- Provide detailed explanations only when requested
  or necessary for correctness.