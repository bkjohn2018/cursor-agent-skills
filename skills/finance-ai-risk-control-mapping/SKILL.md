---
name: finance-ai-risk-control-mapping
description: Maps finance and accounting AI risks to governance, security, privacy, data, and internal control requirements using NIST AI RMF, NIST SP 800-53 concepts, DAMA-DMBOK, and finance control practices. Use when assessing AI use cases, agents, models, assistants, vendor AI, or automation for control objectives, owners, evidence, residual risk, and approval conditions.
---

# Finance AI Risk Control Mapping

This skill translates finance/accounting AI risks into practical control objectives, control activities, evidence, ownership, and release conditions. It is the bridge between AI risk assessment and existing control/documentation skills.

## When to Use

- A finance AI use case is medium risk, high risk, agentic, sensitive, recurring, externally visible, or control-relevant.
- AI output may support reconciliations, close, reporting, forecasts, variance analysis, journal support, audit evidence, compliance, tax, treasury, payroll, AP, AR, or management decisions.
- A team needs an AI control matrix, approval conditions, residual risk statement, or remediation plan.
- A use case needs mapping to NIST AI RMF, NIST 800-53-style controls, DAMA data governance concepts, or finance internal controls.

## Relationship to Other Skills

- Use `finance-ai-use-case-intake` before mapping to capture business context, data, and preliminary risk tier.
- Use `finance-ai-safe-use-policy` to confirm policy fit and safe-use requirements.
- Use `ai-agent-readiness-assessment` for agents, autonomy, tool access, or system actions.
- Use `internal-control-design` to deepen control design, testing, deficiencies, and remediation.
- Use `data-security-and-privacy-controls` for asset-level data protection and privacy controls.
- Use `data-standards-management` when an AI control requirement should become an enterprise data or AI standard.
- Use `data-quality-controls` when AI output depends on source data thresholds, alerts, or remediation playbooks.
- Use `data-issue-management` when control failures, incidents, or defects need triage and closure validation.

## Source Anchors

- **NIST AI RMF**: Organize AI risk work around Govern, Map, Measure, and Manage.
- **AI RMF Playbook**: Use as practical prompts for risk context, measurement, monitoring, and response.
- **NIST SP 800-53 Rev. 5**: Apply access control, audit/accountability, configuration management, identification/authentication, privacy, risk assessment, system integrity, and monitoring concepts.
- **DAMA-DMBOK**: Anchor data governance, stewardship, data ethics, data quality, metadata, lineage, standards, and lifecycle controls.
- **Finance control practice**: Emphasize segregation of duties, approval, evidence, reconciliation, review, change control, auditability, and management accountability.

## Mapping Workflow

1. **Confirm context and classification**
   - Identify the finance process, AI capability, users, data, output, downstream reliance, risk tier, and approval need.
   - Classify whether the use case affects operations, reporting, compliance, audit evidence, or management decision-making.

2. **Map AI RMF functions**
   - **Govern**: accountability, policy fit, roles, training, third-party governance, risk tolerance.
   - **Map**: context, users, affected parties, data, process impact, intended and unintended use.
   - **Measure**: accuracy, reliability, validity, security, privacy, bias/fairness where relevant, data quality, explainability, monitoring signals.
   - **Manage**: risk response, approvals, exceptions, incidents, residual risk, monitoring, recertification.

3. **Identify finance AI risk categories**
   - Incorrect or unsupported output.
   - Sensitive data exposure or unauthorized sharing.
   - Poor source data quality or stale context.
   - Unclear ownership or overreliance on AI.
   - Control bypass, segregation-of-duties failure, or undocumented review.
   - Unauthorized system action, access misuse, or excessive permissions.
   - Vendor/model change, prompt/configuration drift, or untested workflow change.
   - Incomplete evidence, retention failure, or audit trail weakness.
   - Compliance, legal, ethical, reputational, or external reporting impact.

4. **Define control objectives**
   - Convert each material risk into a testable control objective.
   - State what must be prevented, detected, approved, validated, logged, reviewed, corrected, or escalated.

5. **Design control activities**
   - Define preventive, detective, corrective, approval, access, privacy, change, validation, monitoring, and evidence controls.
   - Assign owner, performer, reviewer, frequency, trigger, evidence, and exception path.

6. **Assess residual risk**
   - Identify gaps, compensating controls, conditions before use, accepted residual risk, and approval authority.
   - Escalate prohibited uses or unacceptable residual risk.

7. **Define release and monitoring conditions**
   - Set readiness decision, conditions, monitoring metrics, review cadence, issue triggers, and recertification events.

## Control Areas

- **Governance and accountability**: sponsor, process owner, AI owner, data owner, approver, reviewer, RACI, training, policy fit.
- **Data protection and privacy**: data classification, minimization, masking, approved tools, external sharing, retention, privacy review.
- **Access and permissions**: least privilege, tool permissions, service accounts, privileged access, segregation of duties, periodic review.
- **Output reliability**: source validation, independent review, reasonableness checks, reconciliations, threshold checks, sampling, variance review.
- **Human oversight**: review criteria, approval gates, reviewer competence, prohibited delegation, accountability for final decision.
- **Change and configuration**: prompt, model, workflow, data source, permission, vendor, and tool changes reviewed before release.
- **Logging and evidence**: prompts, inputs, outputs, tool calls, approvals, exceptions, tests, reviews, and remediation retained where appropriate.
- **Monitoring and incident response**: quality signals, exceptions, failed controls, unusual activity, user feedback, escalation, closure validation.

## Output Template

```markdown
# Finance AI Risk and Control Mapping: [Use Case]

## Context
- Business process:
- AI capability:
- Users:
- Data involved:
- Output/use:
- Risk tier:

## AI RMF mapping
| Function | Key considerations | Gaps |
|---|---|---|
| Govern |  |  |
| Map |  |  |
| Measure |  |  |
| Manage |  |  |

## Risk and control matrix
| Risk | Impact | Control objective | Control activity | Owner | Reviewer | Frequency | Evidence |
|---|---|---|---|---|---|---|---|

## Control area coverage
- Governance/accountability:
- Data protection/privacy:
- Access/permissions:
- Output reliability:
- Human oversight:
- Change/configuration:
- Logging/evidence:
- Monitoring/incident response:

## Residual risk and decision
- Residual risk:
- Required conditions:
- Compensating controls:
- Exception needed:
- Approval authority:
- Decision: Approve / Approve with Conditions / Do Not Approve / Prohibited

## Monitoring and recertification
- Monitoring signals:
- Review cadence:
- Recertification triggers:
- Issue escalation path:
```

## Acceptance Criteria

- Risks are specific to the AI use case and finance/accounting process.
- Each material risk has a testable control objective and mapped control activity.
- Owners, reviewers, frequency, evidence, and exception paths are defined.
- AI RMF functions are addressed without becoming a generic checklist.
- Security, privacy, data governance, internal control, and finance evidence needs are integrated.
- Residual risk and approval conditions are explicit before use.
