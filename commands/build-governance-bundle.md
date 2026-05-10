Build a controlled, testable, auditable governance package for a target domain.

Use this command when the user wants a complete governance package, not just a set of standalone documents. The package should connect business value, ownership, standards, controls, data trust, documentation lifecycle, and stakeholder communication.

Collect these inputs first:
- Domain name and business function
- Governance objective and decision/use case supported
- Target audience, sponsor, accountable owner, reviewers, and approvers
- Reference pattern/source material
- Known systems, datasets, reports, workflows, and documentation
- Known metrics, business terms, and data definitions
- Known risks, control gaps, compliance drivers, and privacy/security concerns
- Any AI tools, assistants, models, automations, vendor AI, or agents involved
- Maturity level: draft, pilot, operational, formalized, audit-ready
- Required outputs and delivery format
- Desired tone: executive, operational, training-oriented, audit-ready
- Target effective date, review cadence, and pilot/rollout timing

Execute by phase:

1. **Delivery framing**
   - Apply `governance-project-delivery`.
   - Define value statement, stakeholders, scope, milestones, acceptance criteria, risks, change control, and closure criteria.

2. **Governance foundation**
   - Apply `data-management-foundations` when enterprise data management context is needed.
   - Apply `data-governance` for operating model, decision rights, councils, escalation, issue workflow, and policy/standards lifecycle.
   - Apply `data-standards-management` for baseline data standard requirements and NIST/DAMA control considerations.

3. **Internal control and risk**
   - Apply `internal-control-design` for risk-control mapping, control objectives, control matrix, evidence, testing, deficiencies, and remediation.
   - Apply `data-security-and-privacy-controls` for access, PII/privacy, encryption, logging, sharing, segregation of duties, and security/privacy exceptions.
   - Apply `data-quality-controls` only for data correctness checks, thresholds, alerts, and remediation routing.
   - Apply `finance-ai-risk-control-mapping` when AI tools, assistants, models, vendor AI, automations, or agents affect the domain.
   - Apply `ai-agent-readiness-assessment` when the domain includes tool access, system actions, workflow execution, or delegated AI behavior.

4. **Data trust and definitions**
   - Apply `business-glossary-management` for governed terms and synonyms.
   - Apply `metric-governance` for official KPI/metric definitions and approval lifecycle.
   - Apply `metadata-and-lineage` for asset-level lineage, source-to-consumption traceability, refresh dependencies, and impact notes.
   - Apply `data-quality-assessment` when readiness scoring or defect prioritization is required.
   - Apply `data-issue-management` for triage, ownership, remediation tracking, and closure validation.

5. **Documentation and lifecycle**
   - Apply `governance-writing-style-guide` before drafting governed artifacts.
   - Apply `policy-and-standard-writing`, `process-and-procedure-writing`, and `sop-writing` for content creation.
   - Apply `finance-ai-safe-use-policy` and `finance-ai-use-case-intake` when the package needs AI safe-use boundaries or AI intake procedures.
   - Apply `finance-documentation-lifecycle` for approval, controlled copy location, publication, access, version history, retention, revision, retirement, and audit evidence.

6. **Communication package**
   - Apply `executive-summary-writing` for leadership-ready summary.
   - Apply `governance-ppt-deck-writing` for committee, audit, or executive deck outline.
   - Apply `analytics-storytelling` when analytical findings or performance narratives are included.

Output must be coherent across:
- Scope and out-of-scope boundaries
- Terminology and definitions
- Roles, RACI, owners, approvers, and reviewers
- Risks, control objectives, controls, evidence, and testing
- AI use boundaries, intake routing, agent readiness, monitoring, and recertification when AI is in scope
- Metrics, formulas, thresholds, lineage, and quality checks
- Security/privacy requirements and exceptions
- Documentation lifecycle metadata
- Governance narrative and decision requests

Default output sections:
1. Executive Summary and Decision Request
2. Initiative Charter / Delivery Plan
3. Governance Operating Model
4. Policy or Standard Addendum
5. High-Level Governance Process
6. Detailed Procedure or SOP
7. RACI / Roles and Responsibilities
8. Risk and Internal Control Matrix
9. Security and Privacy Control Assessment
10. Business Glossary
11. Metric Definitions
12. Data Standards, Metadata, and Lineage Requirements
13. Data Quality Rules and Monitoring Controls
14. Issue and Change Management Procedure
15. Documentation Lifecycle Metadata
16. Adoption / Training Notes
17. Executive or Governance Deck Outline
18. Version History, Change Log, and Open Decisions
