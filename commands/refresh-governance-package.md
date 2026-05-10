Refresh an existing governance package after changes to metrics, ownership, systems, controls, standards, risks, privacy/security requirements, documentation lifecycle, or process design.

Collect these inputs first:
- Package/domain name
- Current version, date, owner, and controlled copy location
- Change drivers: metric, owner, system, process, risk, policy, standard, control, privacy/security, regulatory, documentation lifecycle
- AI change drivers: tool/vendor, model, prompt, agent permission, workflow automation, data source, policy, monitoring, incident, exception, or recertification
- Artifacts to refresh: full package or selected sections
- Effective date and transition period
- Stakeholders, reviewers, approvers, and impacted users
- Required output format and tone
- Known open issues, exceptions, audit findings, or control deficiencies

Execute by phase:

1. **Baseline current package**
   - Identify current scope, artifacts, owners, metrics, controls, standards, lineage, document metadata, and open decisions.
   - Preserve user-provided or previously approved content unless the change driver requires replacement.

2. **Impact analysis**
   - Apply `governance-project-delivery` for stakeholder, milestone, risk, issue, dependency, and change-control impact.
   - Apply `internal-control-design` for risk-control, evidence, deficiency, and remediation impact.
   - Apply `data-security-and-privacy-controls` for access, privacy, sharing, logging, encryption, and exception impact.
   - Apply `data-standards-management` for standards and baseline requirement impact.
   - Apply `metric-governance`, `metadata-and-lineage`, `data-quality-controls`, and `data-issue-management` for data trust impact.
   - Apply `finance-ai-safe-use-policy`, `finance-ai-use-case-intake`, `finance-ai-risk-control-mapping`, and `ai-agent-readiness-assessment` when AI tools, models, automations, or agents changed or were added.
   - Apply `finance-documentation-lifecycle` for approval, publication, version, retention, and retirement impact.

3. **Refresh impacted artifacts**
   - Use only the relevant specialized skills for changed artifacts:
     - `policy-and-standard-writing`
     - `process-and-procedure-writing`
     - `sop-writing`
     - `business-glossary-management`
     - `metric-governance`
     - `metadata-and-lineage`
     - `data-quality-assessment`
     - `data-quality-controls`
     - `data-security-and-privacy-controls`
     - `internal-control-design`
     - `finance-ai-safe-use-policy`
     - `finance-ai-use-case-intake`
     - `finance-ai-risk-control-mapping`
     - `ai-agent-readiness-assessment`
     - `executive-summary-writing`
     - `governance-ppt-deck-writing`

4. **Reconcile consistency**
   - Check terminology, role ownership, RACI, metric formulas, thresholds, lineage, data quality rules, AI risk/control mapping, agent readiness, privacy/security controls, issue workflow, and documentation lifecycle metadata.

5. **Update lifecycle records**
   - Apply `finance-documentation-lifecycle`.
   - Update version history, change log, approval status, effective date, controlled copy location, retention notes, superseded sections, and open approvals.

Output must include:
1. Updated artifact set, full or scoped
2. Delta summary by artifact
3. Impact assessment across roles, controls, standards, metrics, lineage, AI use, agent readiness, privacy/security, reporting, and documentation lifecycle
4. Updated version history and effective-date notes
5. Open approvals, pending actions, residual risks, and unresolved questions
6. Readiness decision for the refreshed package
