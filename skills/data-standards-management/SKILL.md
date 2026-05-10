---
name: data-standards-management
description: Defines and maintains enterprise data standards for classification, access, quality, metadata, lineage, retention, integration, reference/master data, metrics, and analytical models. Use when creating a data standards catalog, mapping standards to DAMA-DMBOK capabilities and NIST SP 800-53 control considerations, or deciding what baseline requirements data products must satisfy. Use data-security-and-privacy-controls for asset-level security/privacy control design, policy-and-standard-writing for final mandatory language, and domain skills for implementation.
---

# Data Standards Management

This skill defines the standards layer between the data governance operating model and individual implementation work. It establishes what good data products, reports, metrics, integrations, models, and documentation must include before they are trusted for finance, analytics, governance, or operational use.

Use this skill to define the standard. Use specialized skills to implement or assess a specific asset.

## When to Use

- Creating or rationalizing an enterprise data standards catalog.
- Defining minimum requirements for governed datasets, metrics, dashboards, models, integrations, or reference data.
- Mapping data standards to DAMA-DMBOK knowledge areas and NIST SP 800-53 security/privacy control considerations.
- Deciding which baseline requirements apply to sensitive, financial, regulated, or business-critical data.
- Reviewing whether an existing data standard has clear scope, ownership, requirements, exceptions, evidence, and review cadence.
- Harmonizing overlapping standards across data quality, metadata, access, retention, integration, and metric governance.

## Relationship to Other Skills

- Use `data-governance` for the operating model, decision rights, councils, escalation, and standards lifecycle.
- Use `policy-and-standard-writing` to turn approved requirements into formal mandatory policy or standard language.
- Use `metadata-and-lineage` to document metadata and lineage for a specific asset.
- Use `metric-governance` to define and approve specific KPI or metric records.
- Use `data-quality-assessment` to score a dataset against defined quality rules and thresholds.
- Use `data-quality-controls` to design monitoring, alerts, and response playbooks.
- Use `data-security-and-privacy-controls` to design asset-level access, privacy, encryption, logging, monitoring, sharing, and exception controls.
- Use `finance-documentation-lifecycle` to control the published standard as an approved document.
- Use `governance-project-delivery` to plan and manage a multi-standard rollout.

## Source Anchors

- **DAMA-DMBOK**: Organize standards by data governance, architecture, modeling, storage, security, integration, reference/master data, warehousing/BI, metadata, quality, and maturity.
- **NIST SP 800-53 Rev. 5**: Add control expectations for access, auditability, configuration/change management, identification and authentication, media/storage protection, privacy, risk assessment, system and communications protection, and information integrity.
- **Finance and audit practice**: Strengthen standards for financial reporting, SOX-relevant data, reconciliations, evidence, retention, segregation of duties, and approval traceability.

## Core Standard Domains

1. **Data classification and handling**
   - Classification levels, sensitive data categories, handling rules, sharing limits, storage expectations, encryption needs, and labeling.

2. **Access and authorization**
   - Least privilege, role-based access, approval workflow, access review cadence, privileged access, emergency access, and segregation of duties.

3. **Data quality**
   - Quality dimensions, business rules, thresholds, issue severity, monitoring expectations, remediation ownership, and exception handling.

4. **Metadata and lineage**
   - Required business, technical, operational, and governance metadata; lineage depth; source-to-consumption traceability; impact analysis requirements.

5. **Metric and KPI definitions**
   - Naming, formula, grain, filters, dimensional cuts, ownership, approval, source lineage, quality checks, and change control.

6. **Reference and master data**
   - Authorized value sets, hierarchy ownership, change approval, effective dating, stewardship, reconciliation, and downstream synchronization.

7. **Retention and disposition**
   - Retention period, archive rules, legal hold, disposal approval, evidence retention, and audit trail requirements.

8. **Integration and exchange**
   - Interface ownership, file/API standards, validation, reconciliation, encryption, error handling, monitoring, retry rules, and transfer evidence.

9. **Analytical model readiness**
   - Grain, naming, conformed dimensions, facts, history handling, semantic definitions, refresh cadence, testing, and review expectations.

10. **Issue and change control**
   - Defect intake, standard exceptions, material change approval, impact assessment, communication, closure validation, and lessons learned.

## NIST Control Considerations

Use NIST SP 800-53 as a control lens, not as a replacement for data management standards:

- **Access Control**: Who can access, change, approve, extract, or share the data?
- **Audit and Accountability**: What activity, approval, lineage, and exception evidence is logged and retained?
- **Configuration Management**: How are schema, logic, access, pipeline, report, or standard changes controlled?
- **Identification and Authentication**: How are users, service accounts, and privileged actors authenticated?
- **Media and Storage Protection**: How are files, extracts, backups, archives, and removable media protected?
- **Privacy Controls**: How are PII, consent, minimization, purpose, transparency, and disclosure expectations handled?
- **Risk Assessment**: How are data sensitivity, business criticality, misuse risk, and control gaps assessed?
- **System and Communications Protection**: How are data transfers, APIs, encryption, and network paths protected?
- **System and Information Integrity**: How are errors, anomalies, integrity failures, and unauthorized changes detected and resolved?

## Standards Development Workflow

1. **Define scope and driver**
   - Name the data domain, asset type, process, risk, regulation, or business outcome the standard supports.
   - State what decisions, controls, reports, or operations depend on the standard.

2. **Identify applicable domains**
   - Select the core standard domains that apply.
   - Avoid forcing every standard to cover every domain; tailor based on risk and use.

3. **Classify risk and sensitivity**
   - Assess data sensitivity, financial reporting relevance, privacy impact, operational criticality, and downstream dependency.
   - Increase rigor for restricted, regulated, executive, SOX-relevant, or externally shared data.

4. **Define requirements**
   - Write testable requirements for ownership, quality, metadata, access, retention, integration, controls, evidence, and exceptions.
   - Separate required controls from recommended practices.

5. **Map controls and evidence**
   - Link requirements to DAMA-DMBOK capability areas and relevant NIST control considerations.
   - Define evidence that proves the standard is followed.

6. **Assign accountability**
   - Identify owner, steward, approver, control performer, reviewer, and exception authority.
   - Define review cadence and escalation route.

7. **Validate and publish**
   - Review with stakeholders, security/privacy, compliance, data owners, and impacted users.
   - Use `policy-and-standard-writing` for final mandatory wording when the requirements are approved.
   - Use `finance-documentation-lifecycle` if the standard must be controlled as an approved document.

8. **Monitor and improve**
   - Track adoption, exceptions, issues, review findings, control failures, and user feedback.
   - Revise the standard when risks, systems, regulations, or business usage change.

## Output Template

```markdown
# Data Standard: [Name]

## Purpose and value
[What this standard protects, enables, or improves]

## Scope
- Applies to:
- Does not apply to:
- Data domains or asset types:

## Drivers
- Business driver:
- Risk or compliance driver:
- Decision or process supported:

## Classification and risk
- Sensitivity:
- Business criticality:
- Financial reporting relevance:
- Privacy impact:

## Requirements
| Area | Requirement | Evidence | Owner |
|---|---|---|---|
| Classification |  |  |  |
| Access |  |  |  |
| Quality |  |  |  |
| Metadata/lineage |  |  |  |
| Retention |  |  |  |
| Integration/change |  |  |  |

## Control mapping
- DAMA-DMBOK area:
- NIST control consideration:
- Finance/audit consideration:

## Exceptions
- Who can approve:
- Required rationale:
- Expiration date:
- Compensating control:

## Review and lifecycle
- Standard owner:
- Approval authority:
- Review cadence:
- Next review date:
- Change log:
```

## Acceptance Criteria

- Scope, owner, approval authority, and review cadence are explicit.
- Requirements are testable and mapped to evidence.
- Control expectations are tailored to data sensitivity and business criticality.
- DAMA-DMBOK capability areas and NIST control considerations are identified where relevant.
- Exceptions require rationale, approver, expiration, and compensating control.
- The standard points to specialized implementation skills instead of duplicating asset-level procedures.

## Quality Checklist

- Requirements use consistent terms and avoid vague phrases like "as appropriate" without criteria.
- Ownership distinguishes accountability, stewardship, operation, approval, and review.
- Sensitive, financial, regulated, and externally shared data have stronger controls.
- Metadata, lineage, quality, access, retention, and change requirements do not contradict each other.
- Evidence can be produced without relying on verbal confirmation.
- The standard is ready to be converted into formal language by `policy-and-standard-writing`.
