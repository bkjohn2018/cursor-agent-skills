---
name: data-quality-controls
description: Designs preventive and detective controls for data quality with thresholds, alerts, and owner response playbooks. Use when implementing data correctness monitoring, validation rules, defect alerts, or remediation routing. Use internal-control-design for broader COSO-style control matrices, risk-control mapping, evidence, deficiencies, and remediation.
---

# Data Quality Controls

## When to Use
- Operationalizing data quality checks.
- Defining thresholds and alert routing.
- Requests for data quality control catalogs and response playbooks.

## Relationship to Other Skills
- If starting from an unprofiled dataset, use `data-profiling` first to identify structural gaps (nulls, duplicates, outliers) worth converting into controls.
- Use `data-quality-assessment` instead when the need is business-rule-based quality scoring (completeness, validity, consistency, timeliness, uniqueness) rather than raw structural profiling.
- Note: as of this writing, the `build-governance-bundle` pipeline chains directly from `metric-governance` into this skill with no prior profiling or quality-assessment phase — neither of the above is currently part of that tested pipeline. Flagged as a possible gap, not fixed here.

## Workflow
1. Prioritize critical fields and business-critical datasets.
2. Define control type (preventive, detective, reconciliatory).
3. Set thresholds, severity bands, and alert channels.
4. Assign control owner and escalation path.
5. Document remediation steps and closure criteria.

## Output Template
```markdown
# Data Control Spec

## Control
- Name:
- Type:
- Scope:
- Frequency:

## Logic
- Rule:
- Threshold:
- Severity mapping:

## Operations
- Owner:
- Alert channel:
- Escalation:
- Remediation steps:
```

## Quality Checklist
- Controls map to material business risk.
- Thresholds are realistic and testable.
- Ownership and escalation are explicit.
- Remediation completion criteria are measurable.
