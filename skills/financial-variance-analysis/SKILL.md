---
name: financial-variance-analysis
description: Analyzes actual-vs-plan and period-over-period financial variances against predefined dimensions (entity, account, product, region) using standard volume/rate/mix decomposition, with business interpretation. Use when finance teams need variance narratives and action-focused insights explained against known categories. Use `predictive-model-development` instead when the explanatory grouping itself is unknown and must be discovered (e.g., clustering or segmentation to find which vendors, invoice types, or processors are driving a pattern).
---

# Financial Variance Analysis

## When to Use
- Month-end and quarter-end performance reviews.
- Budget vs actual explanation requests.
- Executive review preparation for financial drivers.

## Workflow
1. Define baseline comparison (plan, forecast, prior period).
2. Quantify variance by key dimensions (entity, account, product, region).
3. Decompose variance into volume, rate, mix, and one-off effects.
4. Flag material drivers and recurring patterns.
5. Convert findings into decisions and corrective actions.

## Output Template
```markdown
# Variance Analysis Brief

## Comparison basis
- Actual period:
- Baseline:

## Headline variance
- Amount:
- Percent:

## Driver decomposition
- Volume:
- Rate:
- Mix:
- One-off:

## Actions
1. ...
```

## Quality Checklist
- Baseline is clearly stated and consistent.
- Decomposition logic is traceable and non-overlapping.
- Materiality thresholds are applied.
- Recommendations map to controllable levers.
