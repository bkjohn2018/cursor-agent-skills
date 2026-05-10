---
name: ai-agent-readiness-assessment
description: Assesses whether an AI agent or agentic workflow is ready for finance and accounting use based on autonomy, tool access, data sensitivity, control impact, human approval, failure modes, logging, monitoring, rollback, evidence, and recertification. Use before deploying, approving, expanding, or materially changing an AI agent.
---

# AI Agent Readiness Assessment

This skill evaluates whether an AI agent is ready to operate in a finance/accounting context. An agent includes any AI workflow that can plan steps, call tools, access systems, retrieve data, generate work products, trigger actions, or operate with partial autonomy.

## When to Use

- A finance/accounting AI use case includes agents, tool calls, workflow execution, system actions, scheduled runs, or delegated decisions.
- An AI assistant will access finance systems, files, tickets, emails, repositories, dashboards, documents, or structured data.
- An agent may prepare reconciliations, reports, journal support, variance commentary, documentation, control evidence, or process outputs.
- A previously approved agent is changing tools, permissions, prompts, model, data, workflow scope, users, or operating conditions.
- The team needs a ready / ready with conditions / not ready decision.

## Relationship to Other Skills

- Use `finance-ai-use-case-intake` before this assessment to capture the business use and preliminary risk tier.
- Use `finance-ai-safe-use-policy` to test whether the agent is permitted, restricted, or prohibited.
- Use `finance-ai-risk-control-mapping` to map risks to controls and evidence.
- Use `data-security-and-privacy-controls` for access, privacy, sensitive data, logging, sharing, retention, and exceptions.
- Use `internal-control-design` for control owner, performer, reviewer, frequency, evidence, and testing.
- Use `data-quality-controls` when agent outputs depend on monitored data quality rules.
- Use `metadata-and-lineage` when agent inputs, transformations, or downstream outputs require traceability.
- Use `data-issue-management` for incidents, defects, control failures, and closure validation.

## Source Anchors

- **NIST AI RMF**: Govern agent accountability, Map context and impacts, Measure performance and risk, Manage residual risk.
- **AI RMF Playbook**: Use as a question bank for governance, measurement, monitoring, and risk response.
- **NIST SP 800-53 Rev. 5**: Apply access control, audit/accountability, configuration management, identification/authentication, privacy, risk assessment, system integrity, and monitoring concepts.
- **DAMA-DMBOK**: Align data governance, stewardship, data quality, metadata, ethics, and lifecycle controls.

## Readiness Workflow

1. **Define agent purpose and boundaries**
   - State the business process, expected output, users, schedule, and success criteria.
   - Define what the agent is not allowed to do.
   - Identify whether the agent supports, recommends, prepares, approves, posts, communicates, or executes.

2. **Map autonomy and action rights**
   - Identify tool access, system permissions, data access, write access, external communication, scheduling, retries, and escalation paths.
   - Classify autonomy as assistive, supervised, approval-gated, automated with monitoring, or prohibited.

3. **Classify data and process criticality**
   - Identify sensitive finance/accounting data, PII, regulated data, unreleased financials, management reporting, audit evidence, close, reconciliation, tax, treasury, payroll, or compliance impact.
   - Identify downstream reliance and whether output affects books, records, reports, controls, filings, vendors, customers, employees, or executives.

4. **Evaluate human oversight**
   - Define who reviews the agent output, what they review against, what evidence they retain, and when approval is required before action.
   - Require human approval before posting, approving, submitting, externalizing, deleting, overwriting, changing permissions, or bypassing controls.

5. **Assess failure modes**
   - Identify incorrect output, missing context, hallucination, stale data, unauthorized access, prompt injection, tool misuse, duplicate action, overposting, hidden assumptions, evidence gaps, privacy exposure, and control bypass.
   - Define containment, rollback, correction, and escalation steps.

6. **Validate controls and evidence**
   - Confirm access approvals, least privilege, logging, change control, test results, output validation, exception process, monitoring, and reviewer signoff.
   - Confirm prompts, configurations, tool permissions, data sources, and model/vendor dependencies are documented.

7. **Test before release**
   - Run representative scenarios, edge cases, negative tests, permission tests, data quality tests, output validation tests, and failure recovery tests.
   - Confirm the agent cannot perform prohibited actions under normal or foreseeable misuse conditions.

8. **Decide readiness and recertification**
   - Decide Ready, Ready with Conditions, Not Ready, or Prohibited.
   - Define conditions, owner, due date, monitoring cadence, recertification trigger, and expiration of approval.

## Readiness Criteria

- Purpose and scope are bounded.
- Autonomy level and tool permissions are explicit.
- Sensitive data and finance process impact are classified.
- Human review and approval gates are defined for material outputs and actions.
- Access is least privilege and approved by the proper owner.
- Logs capture prompts, inputs, outputs, tool calls, approvals, exceptions, and actions where feasible.
- Testing covers expected use, edge cases, misuse, and failure recovery.
- Rollback, incident escalation, and remediation paths are defined.
- Recertification is required after material change or on a defined cadence.

## Output Template

```markdown
# AI Agent Readiness Assessment: [Agent Name]

## Agent overview
- Business owner:
- Process/team:
- Purpose:
- Users:
- Operating frequency:
- Tools/systems accessed:
- Outputs/actions:

## Scope boundaries
- Agent may:
- Agent may not:
- Human-owned decisions:
- Prohibited actions:

## Autonomy and permissions
| Capability | Permission level | Approval gate | Evidence/log |
|---|---|---|---|
| Read data |  |  |  |
| Write/update |  |  |  |
| Send/submit |  |  |  |
| Schedule/retry |  |  |  |
| External communication |  |  |  |

## Data and process impact
- Data sensitivity:
- PII/regulated data:
- Financial reporting/control relevance:
- Downstream consumers:
- Business criticality:

## Oversight and controls
| Risk/failure mode | Control | Owner | Reviewer | Evidence |
|---|---|---|---|---|

## Testing performed
- Test scenarios:
- Edge/negative tests:
- Permission tests:
- Output validation:
- Recovery/rollback tests:
- Results:

## Monitoring and recertification
- Logs monitored:
- Monitoring owner:
- Review cadence:
- Recertification trigger:
- Approval expiration:

## Readiness decision
- Decision: Ready / Ready with Conditions / Not Ready / Prohibited
- Conditions:
- Residual risk:
- Approver:
- Next review:
```

## Acceptance Criteria

- Agent autonomy and action rights are not ambiguous.
- Approval gates exist before material finance, accounting, compliance, external, or system-changing actions.
- Sensitive data, access, and logging controls are defined.
- Failure modes have controls, escalation, and recovery paths.
- Testing evidence supports the readiness decision.
- Monitoring and recertification are defined before release.
