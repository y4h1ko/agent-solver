---
name: verification-before-completion
description: Use before claiming a coding change is complete, a bug is fixed, tests pass, or performance improved. Check evidence relevant to the final changes and state verification limits.
---

# Verify before claiming completion
1. Identify the claim and choose checks proportional to the change and its risk.
   - Documentation or instructions: inspect the final content, references, and any relevant syntax or metadata. Unrelated application tests are unnecessary.
   - Python behavior: run targeted tests or a reproducible example covering the changed behavior and relevant edge cases.
   - Bug fixes: rerun the original failure and relevant regression checks. If claiming a test detects the bug, confirm it fails without the fix when practical.
   - Algorithms: check boundaries and compare with a simple reference on small inputs when feasible; consider worst-case resource limits.
   - Performance: verify correctness and compare repeated baseline/candidate measurements under equivalent conditions.
2. Inspect actual output and exit status. A passing linter does not establish runtime correctness; passing selected tests does not establish that an entire suite passes.
3. Use results that apply to the final state. Reuse relevant checks already run on unchanged code; rerun checks when later edits or environment changes could invalidate them. Do not repeat checks just to send an update, switch tasks, or delegate.
4. Review the final changes against the requested behavior and scope. Use a diff when available; otherwise inspect the edited files directly.
5. Report what was verified and any failures or checks that could not run. Never turn assumptions, edits alone, or an unverified success report into a claim of correctness. Do not claim measured coverage or speedups without measurements.
