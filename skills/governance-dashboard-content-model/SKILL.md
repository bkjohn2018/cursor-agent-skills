---
name: governance-dashboard-content-model
description: Defines the domain objects, relationships, statuses, and lifecycle states needed for governance and finance-led operating dashboards. Use when designing dashboards for policies, controls, evidence, issues, certifications, lineage, or audit readiness.
disable-model-invocation: true
---

# Governance Dashboard Content Model

## When to Use
- Building governance, control, risk, or audit dashboards.
- Mapping business objects before designing UI or APIs.
- Turning workflow concepts into dashboard-ready entities and states.

## Core Object Types
- Policy
- Standard
- Control
- Certification / attestation
- Evidence item
- Risk owner
- Exception / issue
- Workflow request / approval
- Data asset / report / metric
- Ledger or operational artifact when finance traceability is required

## Workflow
1. Identify the core entities shown on the page.
2. Define each object’s lifecycle states, owners, and timestamps.
3. Map parent-child relationships and traceability paths.
4. Separate summary entities from drill-down entities.
5. Define which counts, statuses, and trends each object should expose.

## Output Template
```markdown
# Dashboard Content Model

## Core entities
| Entity | Purpose | Owner | Key statuses |
|---|---|---|---|

## Relationships
- Request -> Approval
- Control -> Evidence
- Issue -> Owner
- Metric -> Data asset

## Traceability paths
- Business event -> Operational data -> Control -> Approval -> Ledger -> Analytics

## Dashboard exposure
| Entity | Card metric | Drill page | Key actions |
|---|---|---|---|
```

## Quality Checklist
- Entity names match governed business terminology.
- Lifecycle states are explicit and mutually understandable.
- Traceability paths are complete enough for drill-down design.
- Summary counts are backed by drillable object models.
