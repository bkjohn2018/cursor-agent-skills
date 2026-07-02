# /build-analytics-governance-bundle

## Purpose

Generate a controlled analytics governance bundle for a finance or operational analytics domain. Use this command when the deliverable is centered on reports, dashboards, metrics, data products, analytical models, or decision workflows.

For broader process, policy, control, or documentation packages, use `/build-governance-bundle`.

## Inputs

Collect these inputs first:
- Analytics domain and business function
- Business questions and decisions supported
- Audience, sponsor, data owner, metric owner, steward, reviewers, and approvers
- Source systems, datasets, dashboards, reports, semantic models, and refresh cadence
- Known metrics, formulas, grain, filters, thresholds, and disputes
- Known data quality issues, lineage gaps, access/privacy concerns, and control risks
- AI-generated narratives, forecasts, models, copilots, assistants, automations, or agents involved
- Required outputs and target maturity: draft, pilot, operational, formalized, audit-ready
- Reference package or proof of concept, if any
- Non-goals, assumptions, constraints, and required disclaimers

## Execution

1. **Frame the analytics value**
   - Apply `question-driven-data-projects`.
   - Apply `governance-project-delivery` for scope, stakeholders, acceptance criteria, milestones, risks, issues, and closure criteria.

2. **Define governance and standards**
   - Apply `data-governance` for ownership, decision rights, escalation, and issue workflow.
   - Apply `data-standards-management` for baseline requirements across metrics, metadata, lineage, data quality, access, retention, integration, and analytical model readiness.

3. **Define metrics and meaning**
   - Apply `business-glossary-management` for governed terms.
   - Apply `metric-governance` for official metric records, formulas, grain, dimensional cuts, source lineage, quality controls, owner, steward, approval, and change log.

4. **Define data trust**
   - Apply `metadata-and-lineage` for source-to-consumption traceability.
   - Apply `data-profiling` when onboarding or assessing source data.
   - Apply `data-quality-assessment` for readiness scoring and defect prioritization.
   - Apply `data-quality-controls` for correctness checks, thresholds, alerts, and remediation routing.
   - Apply `data-issue-management` for defect triage and closure validation.

5. **Define model and dashboard design**
   - Apply `dimensional-modeling` when facts, dimensions, grain, conformance, or mart design are required.
   - Apply `data-model-requirements-and-quality` and `data-model-scorecard-review` when model clarity or QA is required.
   - Apply `finance-dashboard-design` when the bundle includes KPI dashboard or analytics webspace design outputs that need layout, hierarchy, filters, and drill-path guidance.

6. **Define controls**
   - Apply `internal-control-design` for risk-control mapping, evidence, deficiencies, and remediation when analytics support financial, compliance, or control decisions.
   - Apply `data-security-and-privacy-controls` for PII, sensitive data, access, logging, encryption, sharing, extracts, and privacy/security exceptions.
   - Apply `finance-ai-risk-control-mapping` when analytics include AI-generated outputs, AI-assisted decisions, models, copilots, vendor AI, or automation.
   - Apply `ai-agent-readiness-assessment` when analytics include agents, tool access, scheduled AI runs, workflow execution, or delegated behavior.

7. **AI safe use and intake**
   - Apply `finance-ai-safe-use-policy` and `finance-ai-use-case-intake` when analytics users need AI use boundaries, risk tiering, approval routing, disclosure, or evidence requirements.

8. **Control documentation**
   - Apply `finance-documentation-lifecycle` for controlled copy location, approval, version history, review cadence, retention, retirement, and audit evidence.
   - Apply `policy-and-standard-writing`, `process-and-procedure-writing`, or `sop-writing` only when the analytics bundle requires formal operating documentation.

9. **Communicate**
   - Apply `analytics-storytelling` for stakeholder narrative.
   - Apply `executive-summary-writing` for leadership summary.
   - Apply `governance-ppt-deck-writing` for steering, audit, risk, or executive deck outline.

## Output

Create a durable package containing:
1. `README.md`
2. `<Domain>_Analytics_Package_Summary.md`
3. `<Domain>_Governance_Package.md`
4. `<Domain>_Deployment_Guide.md`
5. `<Domain>_Governance_Checklist.md`
6. `<Domain>_Data_Dictionary.md`
7. `<Domain>_Business_Glossary.md`
8. `<Domain>_Metric_Definitions.md`
9. `<Domain>_Data_Standards_Requirements.md`
10. `<Domain>_Control_Matrix.md`
11. `<Domain>_Security_Privacy_Assessment.md`
12. `<Domain>_Lineage_Map.md`
13. `<Domain>_Data_Quality_Rules.md`
14. `<Domain>_Issue_Management_Template.md`
15. `<Domain>_Documentation_Lifecycle_Record.md`
16. `<Domain>_Executive_Deck_Outline.md`

## Rules

- Every declared parameter must be used or explicitly marked layout-only.
- Every non-goal must appear in README, deployment guide, checklist, and report disclaimer.
- Any package artifact that becomes a controlled document must align with `finance-documentation-lifecycle`.
- Any analytics output used for financial, compliance, audit, or executive decisions must include metric governance, lineage, quality controls, and security/privacy review.
- Any AI-assisted analytics output used for financial, compliance, audit, or executive decisions must include safe-use fit, risk/control mapping, human review, evidence, monitoring, and agent readiness where applicable.
