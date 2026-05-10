Adapt an existing governance package pattern to a new domain while preserving useful structure and rebuilding domain-specific risks, controls, standards, privacy/security requirements, metrics, lifecycle metadata, and delivery assumptions.

Collect these inputs first:
- Source package/domain
- Target package/domain
- Business function and scope boundaries
- Artifacts to adapt: all or selected
- Terms, metrics, controls, systems, roles, and documentation patterns to retain vs replace
- Known risks, control gaps, compliance drivers, privacy/security concerns, and issue history for the target domain
- AI tools, assistants, models, automations, vendor AI, or agents to retain, replace, add, or remove
- Desired maturity level: draft, pilot, operational, formalized, audit-ready
- Audience, sponsor, accountable owner, reviewers, and approvers
- Tone and required output format

Execute by phase:

1. **Extract reusable pattern**
   - Identify source structure, artifact inventory, assumptions, terms, roles, controls, metrics, standards, lifecycle metadata, and communication patterns.
   - Mark content as reusable, reusable with modification, target-specific, or retire.

2. **Frame target delivery**
   - Apply `governance-project-delivery`.
   - Define target value statement, stakeholders, scope, acceptance criteria, milestones, risks, and closure criteria.

3. **Rebuild target governance foundation**
   - Apply `data-governance` for target decision rights, operating model, escalation, and issue workflow.
   - Apply `data-standards-management` for target baseline requirements and NIST/DAMA control considerations.

4. **Re-map controls and risk**
   - Apply `internal-control-design`.
   - Re-map source controls to target risks, control objectives, owners, performers, reviewers, evidence, testing, deficiencies, and remediation.
   - Do not carry over source controls unless target risks and processes support them.

5. **Re-map security/privacy**
   - Apply `data-security-and-privacy-controls`.
   - Reassess classification, PII/sensitive data, access, segregation of duties, logging, encryption, sharing, extracts, and exceptions for the target domain.

6. **Re-map AI governance**
   - Apply `finance-ai-safe-use-policy`, `finance-ai-use-case-intake`, and `finance-ai-risk-control-mapping` when the target domain includes AI tools, assistants, models, vendor AI, automations, or agents.
   - Apply `ai-agent-readiness-assessment` when the target domain includes tool access, workflow execution, system actions, scheduled runs, or delegated AI behavior.
   - Do not carry over source AI approvals, risk tiers, agent permissions, or monitoring assumptions unless target-domain risks and data support them.

7. **Re-map data trust**
   - Apply `business-glossary-management`, `metric-governance`, `metadata-and-lineage`, `data-quality-assessment`, `data-quality-controls`, and `data-issue-management` as needed.
   - Replace formulas, grain, thresholds, source systems, lineage, quality rules, and issue workflows where target-domain reality differs.

8. **Rebuild controlled documentation**
   - Apply `governance-writing-style-guide`, `policy-and-standard-writing`, `process-and-procedure-writing`, and `sop-writing` for target-specific content.
   - Apply `finance-documentation-lifecycle` for owner, approver, controlled copy location, version history, review cadence, retention, and retirement metadata.

9. **Update communication artifacts**
   - Apply `executive-summary-writing`, `governance-ppt-deck-writing`, and `analytics-storytelling` when relevant.

10. **Run consistency check**
   - Check scope, terminology, roles, RACI, metrics, controls, evidence, standards, AI safe-use boundaries, agent readiness, privacy/security, lifecycle metadata, issue flow, and decision narrative.

Output must include:
1. Adapted executive summary and decision request
2. Adapted governance operating model
3. Adapted policy/standard, process, and SOP
4. Adapted risk-control matrix and security/privacy control assessment
5. Adapted AI safe-use, intake, risk/control, and agent readiness elements when AI is in scope
6. Adapted glossary, metric definitions, data standards, lineage, and quality controls
7. Adapted issue/change management procedure
8. Adapted documentation lifecycle metadata
9. Adapted deck outline or leadership narrative
10. Adaptation log: retained, changed, retired, and newly created elements with rationale
