---
name: dashboard-metric-semantics
description: Defines dashboard KPI semantics, status logic, thresholds, comparators, and drill-down meaning so metrics remain trustworthy and actionable. Use when dashboards need metric cards, trend indicators, health rings, status chips, or governed KPI definitions.
disable-model-invocation: true
---

# Dashboard Metric Semantics

## When to Use
- KPI cards or gauges are being designed.
- Teams disagree on what a dashboard metric means.
- Status colors, thresholds, or trend labels need clear logic.

## Workflow
1. Define the metric purpose and user decision it supports.
2. Specify formula, grain, population, filters, and refresh cadence.
3. Define comparator logic such as target, prior period, SLA, or threshold band.
4. Define status semantics for colors, rings, labels, and trend arrows.
5. Define what happens when the user clicks the metric.

## Output Template
```markdown
# Dashboard Metric Spec

## Metric identity
- Name:
- Purpose:
- Metric type:

## Calculation
- Formula:
- Grain:
- Filters:
- Refresh cadence:

## Status logic
- Green:
- Yellow:
- Red:
- Null / unavailable:

## Comparison basis
- Target:
- Prior period:
- SLA:

## Drill behavior
- Click destination:
- Default filters:
```

## Quality Checklist
- Metric meaning is independent of the chart or card style.
- Status colors and labels have explicit logic.
- Comparison basis is unambiguous.
- Drill behavior matches the user’s next likely question.
