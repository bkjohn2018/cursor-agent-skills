---
name: build-governance-bundle
description: Orchestrates a complete governance package across multiple writing, data governance, and analytics skills. Use when users ask for an end-to-end governance bundle for a domain such as AP, AR, CM, or GL analytics.
---

# Build Governance Bundle

## When to Use
- User needs a full governance package, not a single artifact.
- Domain governance must be replicated from a reference pattern.
- Artifacts must stay consistent in scope, terms, roles, and metrics.

## Orchestration Order
1. Apply `question-driven-data-projects` to anchor work on business questions and decision value.
2. Apply `data-management-foundations` to set DMBOK context and boundaries.
3. Apply `data-governance` to define operating framework and decision rights.
4. Apply `governance-writing-style-guide`.
5. Draft core governance flow with `process-and-procedure-writing`.
6. Draft controls-level steps with `sop-writing`.
7. Draft decision-level narrative with `executive-summary-writing`.
8. Build terminology base with `business-glossary-management`.
9. Define KPI governance with `metric-governance`.
10. Define trust controls with `data-quality-controls`.
11. Score current data quality and prioritize defects with `data-quality-assessment`.
12. Capture traceability using `metadata-and-lineage`.
13. Create leadership narrative structure with `governance-ppt-deck-writing`.

## Required Inputs
- Domain name
- Business function
- Governance objective
- Primary audience
- Reference pattern or source material
- Required outputs
- Known metrics
- Known systems
- Known roles
- Known risks/issues
- Governance maturity level
- Tone

## Bundle Outputs
1. Executive summary
2. Governance policy or addendum
3. High-level governance process
4. Detailed SOP
5. RACI / roles and responsibilities
6. Business glossary
7. Metric definitions
8. Data quality rules
9. Data quality assessment
10. Metadata and lineage template
11. Issue management procedure
12. Adoption/training notes
13. PPT deck outline or draft
14. Version history/change log

## Output Template
```markdown
# Governance Bundle: [Domain]

## 0) Bundle Inputs
- Domain:
- Business function:
- Objective:
- Audience:
- Maturity:

## 1) Executive Summary
...

## 2) Policy or Policy Addendum
...

## 3) High-Level Governance Process
...

## 4) Standard Operating Procedure
...

## 5) RACI
...

## 6) Business Glossary
...

## 7) Metric Definitions
...

## 8) Data Quality Rules
...

## 9) Data Quality Assessment
...

## 10) Metadata and Lineage
...

## 11) Issue Management
...

## 12) Adoption and Training Notes
...

## 13) Deck Outline
...

## 14) Version History
...
```

## Quality Checklist
- All artifacts align to the same purpose and scope.
- Terms are consistent with the glossary.
- Metrics and controls are consistent across policy/process/SOP/deck.
- Ownership is explicit for each control and action.
- Decision asks are clear for executive audiences.
- Governance choices are traceable to DMBOK-aligned activities and maturity goals.
- Initial business questions and stage-gate decisions are traceable through every artifact.
