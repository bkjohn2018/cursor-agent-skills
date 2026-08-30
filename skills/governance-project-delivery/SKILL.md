---
name: governance-project-delivery
description: Applies PMBOK 7-inspired project delivery discipline to finance governance, analytics, data management, and documentation initiatives — and is also the gate that decides whether an initiative warrants governance-weight process at all. Use first, before any other delivery-flavored skill, to tailor the approach: low-criticality, exploratory, or POC/demo work should route to `discovery-analyst`, `question-driven-data-projects`, or `problem-triage` instead of a governed workstream. For work that does warrant governance, use this when planning, prioritizing, coordinating, measuring, or changing a governance workstream, skill roadmap, documentation program, dashboard initiative, data quality remediation, or analytics delivery effort. Focuses on value, stakeholders, tailoring, planning, delivery, measurement, uncertainty, change control, and closure; use specialized content and governance skills for the deliverables themselves.
---

# Governance Project Delivery

This skill adds a lightweight PMBOK 7 delivery layer around governance, finance documentation, analytics, and data management work. It helps turn good artifacts into managed initiatives with clear value, ownership, sequencing, acceptance criteria, risks, measures, and change control.

Use this skill to manage the work. Use the other skills to produce the work products.

## When to Use

- Deciding, at intake, whether a new initiative warrants governance-weight process at all — before creating any charter or backlog.
- Building or improving a governance, documentation, analytics, or data management capability over multiple steps.
- Creating a roadmap, backlog, charter, delivery plan, or review cadence.
- Coordinating multiple skills or artifacts into one governed initiative.
- Prioritizing work by business value, risk, dependency, and stakeholder need.
- Defining acceptance criteria, status reporting, risks, issues, decisions, or change control.
- Closing out an initiative and transitioning ownership to operations.

## Relationship to Other Skills

- Use `discovery-analyst`, `question-driven-data-projects`, or `problem-triage` instead of this skill when tailoring (Step 3 below) determines the work is exploratory, POC/demo, or otherwise doesn't warrant governance-weight process.
- Use `data-governance`, `data-management-foundations`, and `metric-governance` for governance design.
- Use `sop-writing`, `process-and-procedure-writing`, `policy-and-standard-writing`, and `finance-documentation-lifecycle` for controlled documentation.
- Use `dimensional-modeling`, `metadata-and-lineage`, `data-quality-assessment`, and `data-quality-controls` for data and model work.
- Use `finance-dashboard-design`, `financial-variance-analysis`, `reconciliation-analytics`, and `analytics-storytelling` for finance analytics delivery.
- Use this skill to plan, coordinate, track, measure, adapt, and close the initiative that contains those deliverables.

## PMBOK 7 Anchors

Apply these concepts pragmatically, not bureaucratically:

1. **Value delivery**: Define the business outcome, not just the artifact.
2. **Stakeholders**: Identify users, sponsors, owners, approvers, reviewers, and impacted teams.
3. **Tailoring**: Match the delivery approach to risk, uncertainty, urgency, and stakeholder maturity.
4. **Planning**: Define scope, milestones, dependencies, assumptions, acceptance criteria, and review cadence.
5. **Project work**: Coordinate execution, blockers, decisions, communications, and handoffs.
6. **Delivery**: Validate that outputs are usable, approved, adopted, and tied to the intended outcome.
7. **Measurement**: Track progress, quality, adoption, risk reduction, and decision usefulness.
8. **Uncertainty**: Manage risks, issues, changes, assumptions, and emerging constraints.

## Delivery Workflow

1. **Frame the value**
   - Define the business problem, decision need, control gap, compliance driver, or operating pain.
   - State the intended outcome in user-facing language.
   - Identify what improves if the initiative succeeds.

2. **Map stakeholders and ownership**
   - Name the sponsor, accountable owner, working team, reviewers, approvers, and users.
   - Identify who can accept the deliverable and who must operate it after delivery.
   - Capture stakeholder concerns, constraints, and communication preferences.

3. **Tailor the approach**
   - **Decide if this is governed work first**, using PMBOK's tailoring variables:
     - *Product/deliverable*: compliance or regulatory exposure, requirements stability, security classification, whether it can ship incrementally.
     - *Project*: how much stakeholder involvement is required, schedule constraints, funding certainty.
     - *Organization*: governance maturity and formality expected for this kind of work.
   - **If nothing here trips governed-work criteria** — no controls, financial reporting, audit evidence, governed metrics, or executive-decision exposure; exploratory, POC, or demo intent — **stop here and hand off** to `discovery-analyst`, `question-driven-data-projects`, or `problem-triage` instead of producing a Charter or Backlog.
   - **Clarifier**: audience seniority alone does not trip this gate. Presenting to an executive or director is not itself "executive-decision exposure" — that criterion means a governed decision materially depends on this output (e.g., a budget reallocation, a control certification, a public disclosure). A concept check or demo shown to a director stays on the non-governed path unless a real decision rides on it.
   - **If it does trip governed-work criteria**, scale rigor to fit:
     - Use a lightweight checklist for low-risk, single-artifact work.
     - Use a roadmap, backlog, formal approval gates, and change log for high-risk or cross-functional work.

4. **Plan the work**
   - Define scope, out-of-scope items, milestones, dependencies, assumptions, and constraints.
   - Break work into reviewable deliverables.
   - Assign owners and target dates.
   - Define acceptance criteria before drafting or building.

5. **Coordinate delivery**
   - Track status, blockers, decisions, risks, issues, and change requests.
   - Use the relevant specialized skills for each deliverable.
   - Keep stakeholders aligned on scope, priority, and tradeoffs.

6. **Measure readiness and outcomes**
   - Validate deliverables against acceptance criteria.
   - Confirm users can find, understand, trust, and apply the output.
   - Track quality signals such as review findings, open issues, adoption, control exceptions, rework, or unresolved definitions.

7. **Control change**
   - Log material scope, requirement, owner, date, or control changes.
   - Assess impact on related artifacts, skills, templates, metrics, documentation, and downstream users.
   - Require explicit approval for changes that affect risk, auditability, financial reporting, or governed definitions.

8. **Close and transition**
   - Confirm acceptance, publication, ownership, operating cadence, support path, and next review date.
   - Archive key evidence: decisions, approvals, versions, issue resolutions, lessons learned, and open follow-ups.
   - Move ongoing responsibilities into the relevant lifecycle or governance process.

## Core Artifacts

### Initiative Charter

```markdown
# Initiative Charter: [Name]

## Value statement
[What outcome this initiative delivers and why it matters]

## Problem or opportunity
[Control gap, decision need, process issue, compliance driver, or analytics need]

## Scope
- In scope:
- Out of scope:
- Key assumptions:
- Constraints:

## Stakeholders
- Sponsor:
- Accountable owner:
- Working team:
- Reviewers:
- Approvers:
- Primary users:

## Deliverables
- Deliverable:
- Owning skill or method:
- Acceptance criteria:
- Target date:

## Risks and issues
- Risk or issue:
- Impact:
- Owner:
- Response:

## Measurement
- Progress measure:
- Quality measure:
- Adoption or value measure:

## Closure criteria
- Accepted by:
- Published or transitioned to:
- Ongoing owner:
- Next review date:
```

### Delivery Backlog

```markdown
# Delivery Backlog

## Item: [Short name]
- Outcome supported:
- Deliverable:
- Priority:
- Owner:
- Dependency:
- Status:
- Acceptance criteria:
- Risk if delayed:
- Next action:
```

### Change Record

```markdown
# Change Record

## Change: [Short name]
- Requested by:
- Date:
- Reason:
- Affected deliverables:
- Impact on scope, schedule, risk, controls, or users:
- Decision:
- Approved by:
- Follow-up actions:
```

## Acceptance Criteria

- The initiative has a clear business value statement and named owner.
- Stakeholders, approvers, users, and operators are identified.
- Deliverables are broken into reviewable work products with acceptance criteria.
- Risks, issues, dependencies, and change requests are visible and owned.
- Specialized skills are used for specialized deliverables instead of duplicating their content.
- Closure includes acceptance, transition, evidence retention, and next review cadence.

## Quality Checklist

- Value is stated as an outcome, not only an artifact.
- Scope boundaries prevent uncontrolled expansion.
- The delivery approach is tailored to risk and complexity.
- Every material decision has an owner and evidence trail.
- Measures include progress, quality, and adoption or value.
- Open issues and residual risks are explicit at closeout.
