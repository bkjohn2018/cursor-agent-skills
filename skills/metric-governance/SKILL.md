---
name: metric-governance
description: Governs specific metric definitions, calculation rules, ownership, and approval lifecycle. Use when resolving metric disputes, documenting official KPI definitions, or publishing metric governance records. Use data-standards-management when defining enterprise-wide metric standard requirements.
---

# Metric Governance

## When to Use
- KPI definitions differ by team.
- New executive metrics require formal approval.
- Requests for metric dictionary or rule standardization.

## Workflow
1. Identify candidate metrics and decision use cases.
2. Define formula, grain, dimensional cuts, and refresh cadence.
3. Assign owner, steward, and approval authority.
4. Classify metric type (strategic KPI, operational KPI, diagnostic metric).
5. Link metric to source lineage and quality controls.
6. Publish approved definitions and change logs.

## DMBOK Alignment
- Supports Data Governance and Metadata Management by enforcing:
  - standard definitions
  - ownership and approval workflow
  - traceability from metric logic to source data and controls

## Complementary Skills
- Use `dashboard-metric-semantics` when the governed metric must be translated into card status logic, thresholds, comparators, or drill behavior in a dashboard UI.

## Output Template
```markdown
# Metric Governance Record

## Metric
- Name:
- Purpose:
- Formula:
- Grain:
- Refresh cadence:

## Governance
- Owner:
- Steward:
- Approval status:

## Data and controls
- Source systems:
- DQ checks:

## Change log
- Date:
- Change:
```

## Quality Checklist
- Formula is unambiguous and reproducible.
- Grain and dimensional filters are explicit.
- Ownership and approval path are documented.
- Changes are versioned with rationale.
