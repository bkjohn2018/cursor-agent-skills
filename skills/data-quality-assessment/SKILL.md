---
name: data-quality-assessment
description: Assesses data quality across completeness, validity, consistency, timeliness, and uniqueness. Use when users ask for data quality scoring, readiness decisions, or remediation priorities.
---

# Data Quality Assessment

## When to Use
- Dataset readiness reviews for analytics or operations.
- Requests for quality scorecards and defect prioritization.
- Governance checkpoints before release.

## Workflow
1. Define quality dimensions and thresholds by use case.
2. Identify supporting business rules for each quality dimension.
3. Run checks for completeness, validity, consistency, timeliness, uniqueness.
4. Quantify defect rates and business impact.
5. Assign severity and owner for each material issue.
6. Publish scorecard and remediation plan.

## DMBOK Alignment
- Aligns to Data Quality Management activities:
  - Define a data quality framework.
  - Define high quality data by business context.
  - Identify dimensions and supporting rules.
  - Perform initial assessment and prioritize improvements.

## Output Template
```markdown
# Data Quality Scorecard

## Scope
- Data product:
- Period:
- Intended use:

## Dimension scores
- Completeness:
- Validity:
- Consistency:
- Timeliness:
- Uniqueness:

## Top issues
| Issue | Severity | Impact | Owner | ETA |
|---|---|---|---|---|

## Recommendation
- Go/No-Go:
- Conditions:
```

## Quality Checklist
- Thresholds are tied to business tolerance.
- Scores are reproducible from explicit checks.
- Severity reflects user and process impact.
- Remediation ownership and ETA are clear.
