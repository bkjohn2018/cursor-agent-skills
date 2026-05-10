---
name: data-quality-controls
description: Designs preventive and detective controls for data quality with thresholds, alerts, and owner response playbooks. Use when implementing data correctness monitoring, validation rules, defect alerts, or remediation routing. Use internal-control-design for broader COSO-style control matrices, risk-control mapping, evidence, deficiencies, and remediation.
---

# Data Quality Controls

## When to Use
- Operationalizing data quality checks.
- Defining thresholds and alert routing.
- Requests for data quality control catalogs and response playbooks.

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
