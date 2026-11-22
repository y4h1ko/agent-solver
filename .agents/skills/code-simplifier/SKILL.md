---
name: code-simplifier
description: Simplify Python code when refactoring is requested or concrete complexity obstructs the current task. Preserve behavior and focus on recently modified code unless a broader scope is requested. Not a mandatory cleanup pass after every edit.
---

# Simplify Python code
1. Identify a concrete readability or maintenance problem within the requested scope. If no useful simplification is evident, leave the code unchanged.
2. Follow applicable AGENTS.md instructions, the project's Python version, and existing conventions.
3. Prefer readable, explicit Python. Reduce unnecessary nesting, duplication, and abstractions without introducing dense one-liners or unrelated rewrites.
4. Preserve outputs, public interfaces, exceptions, side effects, and mutation behavior. Retain useful abstractions and comments explaining non-obvious constraints.
5. Preserve time and memory requirements. Do not replace streaming with eager materialization or a suitable algorithm with a slower one merely to shorten code.
6. Verify meaningful refactoring with relevant existing tests or before/after comparisons, including affected edge cases. Report any unverified behavior.
7. Summarize significant changes only. Do not run a separate simplification pass automatically after every edit.
