---
name: data-profiling
description: Profiles datasets to establish structural fitness — structure, completeness, uniqueness, distributions, and anomalies — as a prerequisite gate, not an analytical finding in itself. Per Tukey's original framing (Bruce, Bruce & Gedeck, *Practical Statistics for Data Scientists*), exploratory data analysis presupposes data already "processed and manipulated into a structured form"; this skill is what establishes that, for either a data engineering build or an analytics project — it is not EDA itself. Use when onboarding a new table, validating source readiness, or when users ask for a data profile.
---

# Data Profiling

## When to Use
- Initial review of unfamiliar datasets.
- Before modeling, quality assessment, or reporting.
- Requests for missingness, duplicates, and distribution checks.

## Relationship to Other Skills
This skill establishes structural fitness; it does not analyze the data for a business question. Once profiling confirms the data is usable, route to one of two places depending on purpose:
- **Building or governing a data asset**: use `dimensional-modeling`, `data-model-requirements-and-quality`, or `data-quality-controls`.
- **Analyzing the data for a business question**: use `descriptive-pattern-analysis` for trend, cohort/category comparison, correlation, or benchmarking on already-known dimensions, or `predictive-model-development` for clustering, forecasting, driver/regression modeling, or discovering an unknown grouping.

## Workflow
1. Define dataset scope and profiling grain.
2. Summarize schema, row counts, and type consistency.
3. Measure null rates, distinct counts, and duplicate keys.
4. Check distribution outliers and suspicious value patterns.
5. Publish a profile summary with priority actions.

## Output Template
```markdown
# Data Profile Summary

## Dataset scope
- Table(s):
- Time window:
- Grain:

## Column health
- Null rate highlights:
- Type issues:
- Cardinality notes:

## Key integrity
- Candidate key:
- Duplicate rate:

## Distribution signals
- Outliers:
- Skew:

## Recommended actions
1. ...
```

## Quality Checklist
- Key columns and candidate primary keys are tested.
- Null, distinct, and duplicate metrics are quantified.
- Outliers are tied to business plausibility.
- Next actions are specific and prioritized.
