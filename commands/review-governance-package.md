Review a governance package for quality, consistency, control completeness, lifecycle readiness, and decision readiness before publication, pilot, approval, audit prep, or leadership review.

Collect these inputs first:
- Package/domain name
- Artifacts provided for review
- Review objective: quality check, pilot readiness, audit prep, leadership prep, publication approval, or post-change review
- Audience and governance forum: committee, audit, leadership, process owner, control owner
- Known pain points, disputed definitions, control gaps, privacy/security concerns, or open decisions
- AI tools, assistants, models, automations, vendor AI, or agents included in the package
- Required review depth: quick, standard, comprehensive
- Target readiness decision: Go, Conditional Go, No-Go, or advisory only

Review by gate:

1. **Delivery readiness**
   - Apply `governance-project-delivery`.
   - Check value statement, stakeholders, scope, milestones, acceptance criteria, risks, issues, change control, and closure criteria.

2. **Governance and standards readiness**
   - Apply `data-management-foundations`, `data-governance`, and `data-standards-management` as relevant.
   - Check operating model, decision rights, policy/standards lifecycle, ownership, escalation, and baseline data requirements.

3. **Internal control readiness**
   - Apply `internal-control-design`.
   - Check risk-control mapping, control objectives, control type, owner, performer, reviewer, frequency, evidence, testing, deficiencies, and remediation.

4. **Security and privacy readiness**
   - Apply `data-security-and-privacy-controls`.
   - Check classification, PII/privacy, access, least privilege, segregation of duties, logging, encryption, extract/sharing controls, exceptions, and evidence.

5. **AI readiness**
   - Apply `finance-ai-safe-use-policy`, `finance-ai-use-case-intake`, and `finance-ai-risk-control-mapping` when AI use is in scope.
   - Apply `ai-agent-readiness-assessment` when the package includes agents, tool access, workflow execution, system action, or delegated behavior.
   - Check permitted/restricted/prohibited use, intake routing, risk tiering, approval conditions, human oversight, output validation, monitoring, recertification, and residual risk.

6. **Data trust readiness**
   - Apply `business-glossary-management`, `metric-governance`, `metadata-and-lineage`, `data-quality-assessment`, `data-quality-controls`, and `data-issue-management` as relevant.
   - Check definitions, metric formulas, grain, thresholds, lineage, source systems, quality rules, defect handling, and issue closure.

7. **Documentation lifecycle readiness**
   - Apply `finance-documentation-lifecycle`.
   - Check owner, approver, controlled copy location, publication status, access rules, version history, review cadence, retention, retirement, and audit evidence.

8. **Communication readiness**
   - Apply `executive-summary-writing`, `governance-ppt-deck-writing`, and `analytics-storytelling` as relevant.
   - Check decision narrative, executive clarity, audience fit, actionability, and deck/report alignment.

Score findings by severity:
- Critical: blocks publication, approval, audit reliance, or pilot launch.
- Major: should fix before approval or broad adoption.
- Minor: quality improvement or clarity issue.

Output must include:
1. Readiness decision: Go / Conditional Go / No-Go
2. Review scorecard by gate and artifact
3. Findings list with severity, rationale, and affected artifact
4. Consistency gaps across scope, terms, metrics, roles, controls, evidence, and lifecycle metadata
5. Missing controls, AI readiness gates, privacy/security requirements, data standards, lineage, or documentation lifecycle elements
6. Recommended remediation plan with owner, priority, and target timing
7. Open questions, assumptions, and approval blockers
