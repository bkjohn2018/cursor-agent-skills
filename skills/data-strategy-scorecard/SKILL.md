---
name: data-strategy-scorecard
description: Defines scorecards for data strategy, governance, data management maturity, CoE performance, quality, metadata, adoption, value, and risk reduction. Use when measuring data strategy execution, MVDG progress, roadmap outcomes, or CoE effectiveness.
---

# Data Strategy Scorecard

Use this skill to measure whether a data strategy is producing business value, reducing risk, improving trust, and increasing data management maturity.

## When to Use

- Defining success measures for a data strategy.
- Tracking MVDG launch progress.
- Reporting roadmap execution to executives or governance forums.
- Measuring CoE service performance and continuous improvement.
- Creating adoption, trust, quality, metadata, or maturity indicators.

## Measurement Categories

1. **Business value**
   - Decision cycle time, revenue protection, cost reduction, productivity, operational improvement, reporting confidence, and stakeholder value.

2. **Adoption**
   - Active owners/stewards, forum participation, standards usage, glossary usage, training completion, data product certification, and CoE service demand.

3. **Risk reduction**
   - Critical data issues, control exceptions, audit findings, access exceptions, unresolved ownership gaps, and overdue remediation.

4. **Data quality**
   - Rule coverage, pass rates, defect trends, severity, recurrence, timeliness, completeness, validity, and issue closure.

5. **Metadata and lineage**
   - Critical asset coverage, lineage coverage, term linkage, owner assignment, freshness, and impact analysis readiness.

6. **Governance effectiveness**
   - Decision cycle time, policy/standard approvals, issue aging, escalation outcomes, exception trends, and maturity movement.

7. **CoE performance**
   - Intake volume, cycle time, service-level performance, advisory review throughput, enablement reach, satisfaction, and reusable asset adoption.

## Workflow

1. Confirm audience, decision need, reporting cadence, and level of detail.
2. Select a small set of measures tied to strategy outcomes and lifecycle stage.
3. Define each measure with owner, source, formula, threshold, frequency, and action trigger.
4. Balance leading indicators, lagging indicators, risk indicators, and adoption indicators.
5. Define thresholds for green, watch, intervention, and escalation.
6. Assign owners for metric production, review, action, and exception approval.
7. Review measures periodically and retire low-value metrics.

## Related Skills

- Use `metric-governance` for formal KPI definitions.
- Use `data-quality-controls` for quality thresholds and response playbooks.
- Use `metadata-and-lineage` for metadata and lineage coverage measures.
- Use `data-coe-operating-model` for CoE performance measures.
- Use `data-strategy-lifecycle` to align the scorecard to the roadmap.

## Output Template

```markdown
# Data Strategy Scorecard

## Scorecard purpose
- Audience:
- Decision supported:
- Reporting cadence:
- Lifecycle stage:

## Measures
| Category | Measure | Definition | Source | Owner | Threshold | Action trigger |
|---|---|---|---|---|---|---|

## Executive view
- On track:
- Watch items:
- Interventions needed:
- Decisions required:

## Measure governance
- Producer:
- Reviewer:
- Approval authority:
- Refresh cadence:
- Change control:

## Continuous improvement
- Measures to add:
- Measures to retire:
- Open data gaps:
```

## Quality Checklist

- Every measure connects to a business outcome, risk, adoption goal, or maturity target.
- Measures include owner, source, threshold, cadence, and action trigger.
- The scorecard avoids vanity metrics that do not drive decisions.
- Indicators are tailored to lifecycle stage rather than overloaded from day one.
- Review cadence includes metric retirement and refinement.
