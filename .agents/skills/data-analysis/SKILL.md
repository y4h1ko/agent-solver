---
name: data-analysis
description: >-
  Use for exploratory data analysis, competition dataset investigation, statistical insights, visualizations, feature discovery, and evidence-based modeling suggestions.
  Reuse existing research before analyzing. Not for ordinary coding, debugging, or algorithm-only tasks.
---

# Data Analysis

## Objective
Discover actionable patterns, risks, and testable hypotheses.
Build persistent project knowledge to avoid repeated analysis.
Prioritize useful evidence over exhaustive reporting.

## Workflow

### 1. Recover existing knowledge
- Read existing `analysis/` notes before running analysis.
- Check dataset identity, version, target, and assumptions.
- Reuse valid findings, figures, and previous experiments.
- Revalidate only when data, methods, or assumptions changed.
- Identify unanswered questions and knowledge gaps.

### 2. Understand and inspect data
- Identify objective, metric, constraints, target, and
  information available at prediction time.
- Check schema, types, units, missing values, duplicates,
  outliers, cardinality, class balance, and data quality.
- Sample large datasets when useful; disclose sampling.
- Avoid unnecessary full scans and raw data dumps.

### 3. Investigate useful patterns
- Examine distributions, tails, variance, and dependencies.
- Investigate feature-target relationships and interactions.
- Compare relevant subgroups and train/test distributions.
- For time series, analyze lags, autocorrelation, seasonality,
  volatility, jumps, regime changes, and temporal stability.
- Check whether findings survive outliers and sample changes.
- Distinguish observed associations from predictive evidence.

### 4. Validate and visualize
- Choose time-based, grouped, stratified, or random validation
  according to the data-generating process.
- Audit leakage, future information, and evaluation bias.
- Keep target-dependent analysis within training boundaries.
- Select plots that answer concrete questions:
  distributions, ECDFs, scatter/hexbin, heatmaps, rolling
  statistics, conditional relationships, and error plots.
- Prefer a few informative figures over exhaustive galleries.
- Label axes, units, periods, and sample sizes.
- Do not tune against final evaluation data.

### 5. Generate testable hypotheses
- Turn important observations into concrete hypotheses.
- Propose features, transformations, models, or experiments.
- Specify expected usefulness, risks, and validation method.
- Prioritize by expected value, evidence, and testing cost.
- Recommend a simple baseline before complex approaches.
- Never claim predictive improvements without evaluation.

## Persistent Research Memory

Store research inside the current project:

- `analysis/DATA_PROFILE.md`
  Dataset identity/version, schema, objective, quality,
  important properties, and limitations.

- `analysis/FINDINGS.md`
  Observed facts, numerical evidence, methods, assumptions,
  relevant figures, and data provenance.

- `analysis/HYPOTHESES.md`
  Testable ideas, evidence, experiment results, status,
  risks, and next actions.

- `analysis/figures/`
  Useful plots only, with descriptive names.

- `analysis/scripts/`
  Reproducible analysis code when worth retaining.

### Knowledge management
- Create these files only when substantive analysis warrants it.
- Update existing entries instead of duplicating knowledge.
- Assign stable IDs to hypotheses (H001, H002, ...).
- Track status: Proposed, Testing, Supported, Rejected,
  or Inconclusive.
- For each hypothesis, record evidence, dataset/version,
  test method, baseline, numerical result, and next step.
- Preserve negative results to prevent repeated failed ideas.
- Supported associations are not necessarily validated gains.
- Mark stale findings when data or assumptions change.
- Save meaningful insights during analysis, not only at the end.
- Keep notes concise, searchable, and grounded in evidence.
- Never fabricate findings or overwrite contradictory evidence.

## Reporting
- Summarize the 3-5 most useful findings with evidence.
- Show only visualizations supporting important conclusions.
- Distinguish new, reused, and invalidated knowledge.
- Recommend up to 3 prioritized next experiments.
- State limitations and which research files were updated.

## Constraints
- Follow competition rules and existing dependencies.
- Prefer NumPy, pandas, Matplotlib, SciPy, and scikit-learn.
- Do not install packages or train expensive models
  unless necessary and authorized.
- Make calculations reproducible; label approximations.
- Avoid unnecessary dashboards, reports, and artifacts.
- Do not commit or push research files without permission.
- Never claim calculations or experiments that were not run.
