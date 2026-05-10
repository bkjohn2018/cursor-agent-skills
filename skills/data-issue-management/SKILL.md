---
name: data-issue-management
description: Manages data issues through triage, severity scoring, owner assignment, remediation tracking, and closure validation. Use when users need an issue workflow for data defects.
---

# Data Issue Management

## When to Use
- Data incidents or recurring defects are increasing.
- Teams need a standard issue triage and closure process.
- Requests for issue log templates and severity models.

## Workflow
1. Log issue with impacted assets, symptoms, and detection method.
2. Assign severity based on business impact and urgency.
3. Identify owner and immediate containment actions.
4. Track root cause and permanent fix plan.
5. Validate fix, monitor recurrence, and close with evidence.
6. Feed recurring issues into policy, standards, and control updates.

## DMBOK Alignment
- Supports Data Governance and Data Quality Management via:
  - formal issue intake and triage
  - root-cause driven remediation
  - closed-loop improvement into standards and controls

## Output Template
```markdown
# Data Issue Record

## Incident details
- ID:
- Detected at:
- Impacted assets:

## Severity and impact
- Severity:
- Business impact:

## Ownership
- Incident owner:
- Technical owner:

## Resolution
- Root cause:
- Containment:
- Permanent fix:
- Closure evidence:
```

## Quality Checklist
- Severity reflects measurable business impact.
- Owner and ETA are assigned.
- Root cause and permanent fix are distinct.
- Closure includes validation evidence.
