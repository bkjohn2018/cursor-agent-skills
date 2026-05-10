---
name: finance-ai-use-case-intake
description: Captures and triages proposed AI use cases for finance and accounting teams before use, build, purchase, or deployment. Use when evaluating AI requests, AI pilots, embedded vendor AI, assistants, copilots, models, automations, or agents for business purpose, data sensitivity, process impact, risk tier, approvals, and required assessments.
---

# Finance AI Use Case Intake

This skill is the front door for finance/accounting AI use. It captures enough information to route the request to policy fit, risk/control mapping, data protection review, agent readiness assessment, or project delivery without duplicating those skills.

## When to Use

- A finance or accounting team wants to use an AI tool, assistant, model, workflow, vendor feature, or agent.
- A pilot, proof of concept, automation, dashboard feature, analysis, documentation workflow, or reporting process may involve AI.
- The team needs to decide whether a use case is low-risk, restricted, prohibited, or requires additional review.
- A business sponsor wants an intake form, triage checklist, or approval package for AI use.

## Relationship to Other Skills

- Use `finance-ai-safe-use-policy` to test fit against permitted, restricted, and prohibited use categories.
- Use `finance-ai-risk-control-mapping` for medium/high-risk use cases or finance processes with control reliance.
- Use `ai-agent-readiness-assessment` when the use case includes autonomy, tool access, workflow execution, system actions, or delegated decisions.
- Use `data-security-and-privacy-controls` when sensitive, regulated, confidential, financial, or personal data is involved.
- Use `metadata-and-lineage` when source-to-output lineage or downstream impact matters.
- Use `question-driven-data-projects` to sharpen business questions and decision value.
- Use `governance-project-delivery` when the intake becomes a multi-stakeholder rollout or remediation project.

## Source Anchors

- **NIST AI RMF**: Use Govern/Map/Measure/Manage to route the use case through proportionate risk management.
- **AI RMF Playbook**: Use as a prompt set for context, impacts, measurement, monitoring, and risk response.
- **NIST SP 800-53 Rev. 5**: Consider access, auditability, privacy, security, configuration, monitoring, and integrity.
- **DAMA-DMBOK**: Consider data governance, stewardship, ethics, quality, metadata, and lifecycle needs.

## Intake Workflow

1. **Describe the business use**
   - Capture the business problem, process, decision, users, expected benefit, frequency, and urgency.
   - Confirm whether AI is necessary or whether a simpler process, report, control, or automation is enough.

2. **Identify the AI capability**
   - Classify the capability as assistant, search, summarization, classification, extraction, forecasting, code generation, model, embedded vendor AI, workflow automation, or agent.
   - Identify tool/vendor, hosting model, approved status, and whether outputs are retained or used for training.

3. **Classify data and sources**
   - Identify finance/accounting data involved: GL, AP, AR, payroll, tax, bank, vendor, customer, contracts, audit, planning, forecasts, close, reconciliations, reporting, or executive data.
   - Identify PII, regulated data, confidential data, unreleased financials, and external sharing.

4. **Assess process and decision impact**
   - Identify whether the output supports operations, accounting judgments, financial reporting, controls, compliance, management reporting, external reporting, or audit evidence.
   - Identify downstream consumers and whether humans will review the output before reliance.

5. **Screen for prohibited or high-risk use**
   - Flag unapproved sensitive data disclosure, autonomous posting/approval, unsupported accounting conclusions, credential sharing, control bypass, legal/regulatory determinations without review, or external communication without approval.

6. **Assign preliminary risk tier**
   - **Low**: Approved tool, no sensitive data, productivity support, no authoritative output, human review.
   - **Medium**: Internal finance data, recurring process support, moderate reliance, review required.
   - **High**: Sensitive data, financial reporting, control reliance, accounting judgment, external impact, compliance impact, or broad deployment.
   - **Agentic**: Any autonomy, tool access, system action, workflow execution, or delegated decision path.

7. **Route next steps**
   - Low risk: document intake and safe-use obligations.
   - Medium/high risk: perform risk/control mapping.
   - Sensitive data: perform data security/privacy control review.
   - Agentic: perform agent readiness assessment.
   - Policy exception: escalate through exception approval.

## Output Template

```markdown
# Finance AI Use Case Intake: [Use Case Name]

## Business context
- Sponsor:
- Process/team:
- Business problem:
- Expected benefit:
- Frequency:
- Users:

## AI capability
- Tool/vendor/model:
- Capability type:
- Approved tool status:
- Inputs retained or used for training:
- Human user role:

## Data involved
- Source systems/data:
- Sensitivity:
- PII or regulated data:
- Financial reporting relevance:
- External sharing:
- Downstream consumers:

## Process and decision impact
- Output use:
- Finance/accounting decision affected:
- Control or compliance relevance:
- Human review before reliance:
- Evidence retained:

## Risk screening
| Screening question | Yes/No | Notes |
|---|---|---|
| Sensitive finance/accounting data involved? |  |  |
| PII or regulated data involved? |  |  |
| Financial reporting, close, reconciliation, audit, or compliance impact? |  |  |
| AI output used as support for a decision or control? |  |  |
| Agent, automation, tool use, or system action involved? |  |  |
| External communication or third-party sharing involved? |  |  |
| Potential prohibited use? |  |  |

## Preliminary risk tier
- Tier: Low / Medium / High / Agentic / Prohibited
- Rationale:

## Required next steps
- Safe-use policy fit:
- Risk/control mapping:
- Data security/privacy review:
- Agent readiness assessment:
- Approvals:
- Conditions before use:
```

## Acceptance Criteria

- Business purpose and decision value are explicit.
- AI capability, vendor/tool, and deployment context are identified.
- Data sensitivity and finance process impact are classified.
- Prohibited and high-risk indicators are screened before approval.
- Preliminary risk tier is documented with rationale.
- Required follow-up skills and approval path are clearly routed.
