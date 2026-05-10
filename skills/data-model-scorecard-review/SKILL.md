---
name: data-model-scorecard-review
description: Reviews conceptual, logical, and physical data models using Data Model Scorecard categories to produce structured findings, scores, and remediation plans. Use when users request model quality validation, review readiness checks, or formal data model QA.
---

# Data Model Scorecard Review

## When to Use
- Formal quality review of a data model before approval.
- Model quality gate in delivery lifecycle.
- Independent QA of conceptual, logical, or dimensional designs.

## Review Workflow
1. Confirm model type (conceptual, logical, physical; relational or dimensional).
2. Collect required review documentation and model scope.
3. Review model in manageable chunks, not all at once.
4. Score each Data Model Scorecard category.
5. Aggregate findings, prioritize remediation, and assign owners.
6. Re-score after fixes and publish final readiness decision.

## Scorecard Categories
1. Correctness
2. Completeness
3. Scheme
4. Structure
5. Abstraction
6. Standards
7. Readability
8. Definitions
9. Consistency
10. Data

## Output Template
```markdown
# Data Model Scorecard Review

## Review context
- Model name:
- Model type:
- Scope:
- Reviewers:

## Category scores
| Category | Score | Key findings |
|---|---:|---|
| Correctness |  |  |
| Completeness |  |  |
| Scheme |  |  |
| Structure |  |  |
| Abstraction |  |  |
| Standards |  |  |
| Readability |  |  |
| Definitions |  |  |
| Consistency |  |  |
| Data |  |  |

## Prioritized issues
| Severity | Category | Issue | Recommendation | Owner | ETA |
|---|---|---|---|---|---|

## Readiness decision
- Decision: Go / Conditional Go / No-Go
- Conditions:
```

## Quality Checklist
- Scores are justified with clear evidence.
- Findings are actionable and assigned to owners.
- Re-review criteria are explicit.
- Readiness decision is tied to material risk.
