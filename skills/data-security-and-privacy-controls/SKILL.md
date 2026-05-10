---
name: data-security-and-privacy-controls
description: Designs data security and privacy controls for sensitive, regulated, financial, and business-critical data using NIST SP 800-53 Rev. 5 control concepts. Use when assessing or defining controls for data access, privacy, PII handling, encryption, logging, monitoring, sharing, retention, segregation of duties, or security exceptions. Use data-standards-management for enterprise standard requirements and use data-governance for operating model and decision rights.
---

# Data Security And Privacy Controls

This skill designs practical security and privacy controls for governed data assets, reports, metrics, integrations, extracts, dashboards, models, and documentation. It uses NIST SP 800-53 Rev. 5 as a control lens and adapts it for finance, analytics, and data governance work.

Use this skill to decide how sensitive data should be protected in practice. Use `data-standards-management` to define enterprise standards and `policy-and-standard-writing` to convert approved requirements into formal policy language.

## When to Use

- Sensitive, financial, regulated, confidential, or business-critical data is being created, moved, stored, analyzed, shared, or retired.
- Users need controls for PII, payroll, vendor, customer, bank, tax, financial reporting, reconciliation, or executive data.
- A dashboard, dataset, integration, extract, report, metric, or model needs access, privacy, encryption, logging, monitoring, or sharing controls.
- Data access requires approval, periodic review, segregation of duties, emergency access, or privileged access handling.
- A privacy or security exception needs risk assessment, compensating controls, approval, expiration, and evidence.
- A data product needs a control checklist before release.

## Relationship to Other Skills

- Use `data-standards-management` for enterprise-wide data security and privacy standard requirements.
- Use `data-governance` for decision rights, escalation paths, councils, and governance operating model.
- Use `metadata-and-lineage` to identify where sensitive data originates, transforms, and flows downstream.
- Use `data-quality-controls` for data correctness monitoring; use this skill for protection, privacy, and access controls.
- Use `finance-documentation-lifecycle` to control published security/privacy procedures or evidence documents.
- Use `governance-project-delivery` to manage a security/privacy remediation or rollout initiative.

## NIST Control Lens

Apply these NIST SP 800-53-inspired control areas pragmatically:

1. **Access Control**: Enforce least privilege, role-based access, authorized sharing, and access review.
2. **Audit and Accountability**: Log access, changes, extracts, approvals, exceptions, and administrator actions.
3. **Configuration Management**: Control changes to schemas, pipelines, permissions, reports, models, and control settings.
4. **Identification and Authentication**: Verify user, service account, and privileged account identities.
5. **Media and Storage Protection**: Protect files, extracts, backups, archives, local downloads, removable media, and shared folders.
6. **Privacy Controls**: Limit collection, use, disclosure, retention, and exposure of PII and sensitive personal data.
7. **Risk Assessment**: Assess data sensitivity, misuse risk, business criticality, downstream impact, and control gaps.
8. **System and Communications Protection**: Protect data transfers, APIs, networks, encryption paths, and external sharing.
9. **System and Information Integrity**: Detect unauthorized changes, anomalies, tampering, leakage, and integrity failures.

## Control Design Workflow

1. **Classify the data**
   - Identify sensitivity level, regulated data, PII, financial reporting relevance, business criticality, and external sharing.
   - Identify whether data is raw, transformed, aggregated, masked, anonymized, archived, or exported.

2. **Map the data flow**
   - Identify source systems, pipelines, transformations, storage locations, dashboards, reports, extracts, users, and downstream consumers.
   - Use `metadata-and-lineage` when detailed lineage or impact analysis is needed.

3. **Identify threats and misuse scenarios**
   - Consider unauthorized access, excess privilege, accidental sharing, stale access, extraction, re-identification, data leakage, tampering, retention failure, and unapproved downstream use.

4. **Select control objectives**
   - Define what must be prevented, detected, approved, logged, encrypted, masked, reviewed, retained, or escalated.
   - Tailor controls to sensitivity and business risk.

5. **Design controls**
   - Define preventive controls, detective controls, approval controls, monitoring controls, and compensating controls.
   - Assign owner, performer, reviewer, frequency, evidence, escalation path, and exception criteria.

6. **Validate operational fit**
   - Confirm controls are enforceable with available systems, roles, workflows, and monitoring.
   - Avoid controls that depend only on informal behavior where system enforcement is required.

7. **Document exceptions**
   - Require business rationale, risk acceptance, compensating controls, approver, expiration date, review date, and evidence.
   - Escalate exceptions involving PII, financial reporting, external sharing, privileged access, or legal/regulatory risk.

8. **Monitor and improve**
   - Track access review findings, policy exceptions, incidents, audit issues, failed controls, stale access, unusual activity, and remediation status.
   - Feed recurring issues into `data-standards-management`, `data-governance`, or `data-issue-management`.

## Core Control Catalog

### Access Controls

- Role-based access aligned to job duties.
- Least privilege for users, service accounts, and administrators.
- Formal approval before granting sensitive access.
- Periodic access review with owner attestation.
- Timely removal when users change roles or leave.
- Segregation of duties for preparation, approval, posting, reconciliation, and administration.
- Emergency access with time limit, logging, and post-use review.

### Privacy Controls

- PII inventory and purpose documentation.
- Data minimization: collect and retain only what is needed.
- Purpose limitation: use sensitive personal data only for approved purposes.
- Masking, tokenization, aggregation, or anonymization where full detail is not needed.
- Disclosure controls for internal sharing, external sharing, exports, and screenshots.
- Privacy impact review for new datasets, dashboards, integrations, or AI/analytics uses involving personal data.
- Retention and deletion aligned to approved policy and legal hold requirements.

### Protection Controls

- Encryption in transit and at rest for sensitive data where supported.
- Secure transfer methods for files, APIs, and extracts.
- Storage restrictions for local drives, personal folders, email attachments, and unmanaged collaboration spaces.
- Backup and archive protection consistent with source sensitivity.
- Environment separation for production, test, development, and sandbox data.
- Masked or synthetic data for non-production environments when feasible.

### Audit and Monitoring Controls

- Access logs for sensitive datasets, reports, dashboards, and extracts.
- Change logs for permissions, schemas, transformation logic, metric logic, and report filters.
- Extract/download monitoring for restricted data.
- Alerting for unusual access, failed access attempts, bulk exports, or unauthorized sharing.
- Evidence retention for approvals, access reviews, exceptions, incidents, and remediation.

### Change and Integrity Controls

- Approval before changing access rules, classification, masking, retention, or sharing controls.
- Impact review before schema, pipeline, report, dashboard, metric, or model changes.
- Reconciliation or validation after control-relevant changes.
- Integrity checks for critical pipelines, interfaces, and reports.
- Incident escalation when unauthorized change, exposure, or tampering is suspected.

## Output Template

```markdown
# Data Security and Privacy Control Assessment: [Asset]

## Asset and use
- Asset name:
- Asset type:
- Business purpose:
- Primary users:
- Downstream consumers:

## Classification
- Sensitivity:
- PII or personal data:
- Financial reporting relevance:
- Business criticality:
- External sharing:

## Data flow
- Sources:
- Transformations:
- Storage locations:
- Reports/dashboards/extracts:
- External transfers:

## Risks
| Risk | Impact | Likelihood | Current control | Gap |
|---|---|---|---|---|

## Required controls
| Control area | Requirement | Owner | Frequency | Evidence |
|---|---|---|---|---|
| Access |  |  |  |  |
| Privacy |  |  |  |  |
| Protection |  |  |  |  |
| Audit/monitoring |  |  |  |  |
| Change/integrity |  |  |  |  |

## Exceptions
- Exception:
- Business rationale:
- Risk accepted:
- Compensating control:
- Approver:
- Expiration:

## Release decision
- Ready / Ready with conditions / Not ready:
- Required remediation:
- Owner:
- Target date:
```

## Acceptance Criteria

- Data classification and sensitivity are explicit.
- PII and regulated data are identified with purpose, minimization, sharing, retention, and protection expectations.
- Access controls include approval, least privilege, periodic review, and removal triggers.
- Logging, monitoring, and evidence requirements are defined.
- Exceptions include approver, rationale, compensating control, expiration, and follow-up.
- Control design is tailored to risk and can be operated by named owners.

## Quality Checklist

- Controls are specific enough to test.
- Owners distinguish approver, control performer, reviewer, and exception authority.
- Sensitive data is protected across source, transformation, storage, consumption, extract, archive, and disposal.
- Non-production use of sensitive data is addressed.
- External sharing and downstream use are explicitly controlled.
- Residual risk is visible before release or approval.
