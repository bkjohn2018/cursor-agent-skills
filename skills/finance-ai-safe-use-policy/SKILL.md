---
name: finance-ai-safe-use-policy
description: Creates and maintains AI Safe Use Policy requirements for finance and accounting teams, including permitted and prohibited use, approval tiers, data handling, human review, disclosure, exceptions, and review cadence. Use when drafting or updating AI safe-use boundaries, policy requirements, standards, or governance guidance for finance AI use.
---

# Finance AI Safe Use Policy

This skill defines finance/accounting-specific safe-use requirements for AI. It establishes the policy decision layer, then delegates formal wording, documentation control, and detailed control design to existing skills.

## When to Use

- Establishing an AI Safe Use Policy for finance or accounting.
- Defining permitted, restricted, and prohibited AI uses.
- Setting approval tiers for AI tools, assistants, agents, models, or workflows.
- Defining human review, disclosure, evidence, and accountability expectations.
- Updating safe-use requirements after new risks, tools, incidents, regulations, or business practices emerge.

## Relationship to Other Skills

- Use `policy-and-standard-writing` to convert approved requirements into mandatory policy language.
- Use `finance-documentation-lifecycle` to govern approval, publication, versioning, retention, revision, and retirement of the policy document.
- Use `finance-ai-use-case-intake` before deciding whether a new use case fits the policy.
- Use `finance-ai-risk-control-mapping` when the use case needs risk/control analysis.
- Use `ai-agent-readiness-assessment` for agentic workflows, tool use, automation, or delegated action.
- Use `data-security-and-privacy-controls` for detailed data handling, privacy, access, logging, sharing, and exception controls.
- Use `internal-control-design` for finance process controls and evidence requirements.

## Source Anchors

- **NIST AI RMF**: Govern, Map, Measure, and Manage AI risks across the lifecycle.
- **AI RMF Playbook**: Use as a question bank for governance, risk identification, measurement, and management practices.
- **NIST SP 800-53 Rev. 5**: Apply security, privacy, access, auditability, change, monitoring, and risk assessment concepts.
- **DAMA-DMBOK**: Align data governance, data ethics, stewardship, metadata, quality, and lifecycle management.

## Policy Design Workflow

1. **Define policy intent and scope**
   - Identify finance/accounting teams, processes, AI tools, agents, models, data types, and decisions in scope.
   - State whether the policy covers public AI tools, enterprise AI tools, embedded vendor AI, custom models, and AI agents.

2. **Classify AI use categories**
   - **Permitted**: Low-risk assistance with no sensitive data and no authoritative output without review.
   - **Restricted**: Sensitive data, finance records, accounting judgments, regulated processes, or management reporting.
   - **Prohibited**: Unapproved disclosure of sensitive data, unsupported accounting conclusions, autonomous posting/approval, credential sharing, control bypass, or use that violates law, contract, policy, or ethics.

3. **Set approval tiers**
   - Define when self-service use is allowed.
   - Define when manager, process owner, data owner, security/privacy, compliance, or finance leadership approval is required.
   - Require readiness assessment for AI agents or automated workflows.

4. **Define data handling rules**
   - Identify restricted inputs such as PII, payroll, bank, tax, vendor, customer, contract, audit, forecast, executive, financial reporting, or unreleased results.
   - Require approved tools, approved data sources, masking/minimization, retention rules, and external sharing limits.

5. **Define human accountability**
   - Require users to validate AI outputs before relying on them.
   - Prohibit treating AI output as authoritative evidence without reviewer judgment, source support, and retained workpapers where needed.
   - Assign accountability to the human preparer, reviewer, approver, and process owner.

6. **Define transparency and evidence**
   - Specify when AI use must be disclosed in workpapers, reports, analyses, reconciliations, memos, or documentation.
   - Define evidence expectations for prompts, inputs, outputs, source documents, validations, approvals, exceptions, and review signoff.

7. **Define exceptions and incidents**
   - Require business rationale, risk acceptance, compensating controls, approver, expiration, and follow-up for exceptions.
   - Escalate suspected data leakage, incorrect finance output, policy violations, control failures, or unauthorized agent action.

8. **Define review and change triggers**
   - Review at least annually or when AI tools, data sensitivity, finance processes, regulations, incidents, or control expectations materially change.

## Output Template

```markdown
# AI Safe Use Policy Requirements: Finance and Accounting

## Purpose
- Business objective:
- Risk objective:

## Scope
- Teams/processes in scope:
- AI tools and workflows in scope:
- Out of scope:

## Use categories
| Category | Description | Examples | Approval required |
|---|---|---|---|
| Permitted |  |  |  |
| Restricted |  |  |  |
| Prohibited |  |  |  |

## Data handling requirements
| Data type | Allowed use | Restrictions | Approval/evidence |
|---|---|---|---|

## Human review and accountability
- Preparer responsibility:
- Reviewer responsibility:
- Process owner responsibility:
- Prohibited delegation:

## Disclosure and evidence
- When AI use must be disclosed:
- Evidence to retain:
- Retention expectation:

## Exceptions and incidents
- Exception approver:
- Required rationale:
- Compensating controls:
- Escalation triggers:

## Lifecycle
- Policy owner:
- Approval authority:
- Review cadence:
- Change triggers:
```

## Acceptance Criteria

- Permitted, restricted, and prohibited uses are explicit and finance-specific.
- Approval tiers are tied to data sensitivity, process criticality, autonomy, and financial/reporting impact.
- Sensitive finance/accounting data handling rules are clear enough to enforce.
- Human accountability cannot be delegated to AI.
- Evidence, disclosure, exception, and incident expectations are defined.
- The skill produces requirements and points to `policy-and-standard-writing` for final policy wording.
