---
name: internal-control-design
description: Designs and reviews internal controls for finance, reporting, compliance, data governance, analytics, and operational processes using COSO-style internal control concepts. Use when mapping risks to controls, assessing control completeness across control environment, risk assessment, control activities, information and communication, and monitoring, or defining control owner, performer, reviewer, frequency, evidence, deficiency, and remediation requirements. Use data-security-and-privacy-controls for NIST-style security/privacy controls and data-quality-controls for data correctness monitoring.
---

# Internal Control Design

This skill applies an internal-control lens to finance, reporting, compliance, data governance, analytics, and operational processes. It uses free COSO materials as source anchors, especially the Internal Control--Integrated Framework Executive Summary, the principles poster, compliance risk guidance, and related public guidance.

Use this skill to decide whether controls are well designed, risk-aligned, evidenced, monitored, and integrated. Use specialized skills for domain-specific implementation details.

## When to Use

- Designing controls for finance, accounting, reporting, reconciliation, compliance, governance, data, analytics, or documentation processes.
- Mapping risks to preventive, detective, corrective, manual, automated, or IT-dependent controls.
- Reviewing whether a control set covers operations, reporting, and compliance objectives.
- Evaluating control gaps, deficiencies, evidence weaknesses, monitoring gaps, or remediation plans.
- Translating compliance risks into control objectives and control activities.
- Building a control matrix, control narrative, test plan, or audit-ready control package.
- Applying COSO-style principles without needing the full paid framework.

## Relationship to Other Skills

- Use `data-governance` for governance operating model, councils, decision rights, and escalation.
- Use `data-standards-management` for baseline data standard requirements and NIST/DAMA mappings.
- Use `data-security-and-privacy-controls` for asset-level access, privacy, encryption, logging, sharing, and security exception controls.
- Use `data-quality-controls` for data quality thresholds, alerts, and remediation playbooks.
- Use `finance-documentation-lifecycle` for approval, publication, versioning, retention, and retirement of control documentation.
- Use `policy-and-standard-writing`, `sop-writing`, and `process-and-procedure-writing` for formal written artifacts.
- Use `governance-project-delivery` to manage a control remediation or rollout initiative.

## Source Anchors

- **COSO Internal Control--Integrated Framework Executive Summary**: Definitions, objectives, components, and high-level internal control principles.
- **COSO Integrated Framework Principles poster**: Quick checklist for the five components and 17 principles.
- **COSO Compliance Risk Management guidance**: Compliance-risk overlay for laws, regulations, contracts, standards, internal policies, and ethical expectations.
- **COSO Knowledge Hub**: Optional supplemental resources; use selectively and vet source quality and sponsor bias.
- **COSO Internal Control over Sustainability Reporting guidance**: Example of applying internal control concepts to nonfinancial information, disclosures, and decision-useful reporting.

## Internal Control Anchors

Apply these concepts pragmatically:

1. **Objectives**: Controls should support operations, reporting, and compliance objectives.
2. **Control environment**: Governance, tone, accountability, structure, competence, and integrity set the foundation.
3. **Risk assessment**: Risks should be identified, assessed, and tied to explicit control objectives.
4. **Control activities**: Controls should be designed to prevent, detect, correct, approve, reconcile, restrict, or evidence important actions.
5. **Information and communication**: Relevant information should reach the right people in time to perform and monitor controls.
6. **Monitoring activities**: Controls should be reviewed, tested, remediated, and improved over time.
7. **Integration**: Components and principles should operate together, not as isolated checkboxes.

## Control Design Workflow

1. **Define the objective**
   - State the operation, report, compliance obligation, data product, process, or decision the control supports.
   - Classify the objective as operations, reporting, compliance, or a combination.

2. **Identify risks**
   - Identify what could go wrong, including errors, omissions, unauthorized activity, incomplete evidence, unclear ownership, delayed review, invalid data, unsupported reporting, noncompliance, or process failure.
   - Assess likelihood, impact, velocity, and detectability where useful.

3. **Define control objectives**
   - Convert each material risk into a control objective.
   - Make the objective testable: what must be true for the risk to be acceptably reduced?

4. **Design control activities**
   - Choose preventive, detective, corrective, manual, automated, or IT-dependent controls.
   - Define control owner, performer, reviewer, frequency, trigger, inputs, steps, outputs, evidence, system dependency, and exception path.

5. **Check COSO-style coverage**
   - Confirm the control set addresses control environment, risk assessment, control activities, information and communication, and monitoring.
   - Identify which component is weak or missing when a control gap persists.

6. **Define evidence and testing**
   - Specify evidence that proves the control operated.
   - Define test approach, sample basis, pass/fail criteria, reviewer, and retention expectation.

7. **Assess deficiencies**
   - Identify design gaps, operating gaps, evidence gaps, ownership gaps, monitoring gaps, and communication gaps.
   - Rate severity based on risk impact, likelihood, control reliance, financial/reporting/compliance exposure, and compensating controls.

8. **Plan remediation**
   - Define corrective action, owner, due date, interim control, retest plan, closure evidence, and escalation path.
   - Use `governance-project-delivery` when remediation requires multiple owners, milestones, or change control.

## Control Types

- **Preventive**: Stops an error, unauthorized action, or noncompliant event before it occurs.
- **Detective**: Identifies an issue after it occurs so it can be investigated and corrected.
- **Corrective**: Restores the process, record, report, or control state after a failure.
- **Directive**: Guides behavior through policies, procedures, training, standards, or approvals.
- **Reconciliatory**: Compares independent sources and resolves differences.
- **Automated**: Runs through configured system logic with limited manual intervention.
- **Manual**: Performed by a person and dependent on clear instructions, evidence, and review.
- **IT-dependent manual**: Manual review relies on system-generated data, reports, or configurations.

## Output Template

```markdown
# Internal Control Design: [Process or Asset]

## Objective
- Operations objective:
- Reporting objective:
- Compliance objective:

## Scope
- Process or asset:
- In scope:
- Out of scope:
- Systems/data involved:

## Risks and control objectives
| Risk | Impact | Control objective | Existing control | Gap |
|---|---|---|---|---|

## Control matrix
| Control | Type | Owner | Performer | Reviewer | Frequency | Evidence | System dependency |
|---|---|---|---|---|---|---|---|

## COSO-style coverage
- Control environment:
- Risk assessment:
- Control activities:
- Information and communication:
- Monitoring activities:

## Testing approach
- Test procedure:
- Sample basis:
- Pass/fail criteria:
- Evidence retained:

## Deficiencies and remediation
| Deficiency | Severity | Owner | Corrective action | Due date | Closure evidence |
|---|---|---|---|---|---|
```

## Acceptance Criteria

- Objectives are linked to operations, reporting, compliance, or a stated combination.
- Each material risk has a control objective and at least one mapped control or accepted gap.
- Controls specify owner, performer, reviewer, frequency, trigger, evidence, and exception path.
- Evidence is sufficient for independent review or audit testing.
- Control coverage is assessed across the five COSO-style components.
- Deficiencies have severity, owner, remediation plan, due date, and closure evidence.

## Quality Checklist

- Controls reduce specific risks instead of existing as generic process steps.
- Ownership separates accountable owner, performer, reviewer, and approver.
- Manual controls include precise evidence and review criteria.
- Automated controls identify system dependency and change-management needs.
- Monitoring catches both design weakness and operating failure.
- Compliance risks consider laws, regulations, contracts, standards, internal policies, and ethical expectations.
