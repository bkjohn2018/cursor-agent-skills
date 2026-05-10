---
name: data-profiling
description: Profiles datasets to reveal structure, completeness, uniqueness, distributions, and anomalies. Use when onboarding a new table, validating source readiness, or when users ask for a data profile.
---

# Data Profiling

## When to Use
- Initial review of unfamiliar datasets.
- Before modeling, quality assessment, or reporting.
- Requests for missingness, duplicates, and distribution checks.

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
