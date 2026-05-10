---
name: data-management-maturity-assessment
description: Assesses data management maturity across DAMA-DMBOK capability areas and produces scored findings, gaps, priorities, and maturity improvement recommendations. Use when evaluating current data capability, governance maturity, metadata maturity, quality maturity, or readiness for a data strategy or CoE.
---

# Data Management Maturity Assessment

Use this skill to score current-state data management capability before strategy, roadmap, standards, or CoE design.

## When to Use

- Establishing baseline maturity for a data strategy.
- Comparing maturity across domains, functions, systems, or business units.
- Prioritizing capability improvements by risk, value, and feasibility.
- Measuring progress from MVDG to managed data function or CoE.

## Capability Areas

Assess the relevant DAMA-DMBOK areas:

1. Data governance
2. Data architecture
3. Data modeling and design
4. Data storage and operations
5. Data security
6. Data integration and interoperability
7. Reference and master data
8. Data warehousing and BI
9. Metadata management
10. Data quality management
11. Data management maturity and change adoption

## Maturity Scale

Use a 1-5 scale:

1. **Ad hoc**: Informal, inconsistent, person-dependent.
2. **Emerging**: Some repeatable practices, limited ownership or coverage.
3. **Defined**: Documented processes, roles, and standards exist for priority areas.
4. **Managed**: Practices are measured, controlled, and adopted across key domains.
5. **Optimized**: Continuous improvement, automation, and enterprise adoption are established.

## Assessment Workflow

1. Define assessment scope, domains, stakeholders, and evidence sources.
2. Collect evidence through interviews, artifacts, standards, reports, controls, system metadata, and issue history.
3. Score each capability using evidence, not aspiration.
4. Identify gaps, root causes, risks, dependencies, and quick wins.
5. Recommend target maturity by capability, based on business criticality and risk.
6. Prioritize improvements using value, risk reduction, dependency, effort, and readiness.
7. Define reassessment cadence and scorecard integration.

## Evidence Examples

- Governance charters, RACIs, decision logs, issue logs, and policy approvals.
- Data standards, glossary entries, metric definitions, and exception records.
- Metadata catalogs, lineage maps, quality rules, access reviews, and retention schedules.
- Data architecture diagrams, integration inventories, model documentation, and BI inventories.
- Training records, adoption metrics, control evidence, and audit findings.

## Output Template

```markdown
# Data Management Maturity Assessment

## Scope
- Organization/domain:
- Capabilities assessed:
- Evidence reviewed:
- Stakeholders consulted:

## Executive summary
- Overall maturity:
- Highest-risk gaps:
- Highest-value improvements:

## Maturity scores
| Capability | Current score | Target score | Evidence | Key gap | Priority |
|---|---:|---:|---|---|---|

## Cross-capability themes
- Strengths:
- Gaps:
- Dependencies:
- Risks:

## Improvement roadmap
| Priority | Capability | Recommendation | Owner | Time horizon | Success measure |
|---|---|---|---|---|---|

## Reassessment plan
- Cadence:
- Owner:
- Scorecard linkage:
```

## Quality Checklist

- Scores are evidence-based and consistently calibrated.
- Target maturity is risk-based, not automatically 5 for every capability.
- Findings distinguish symptoms from root causes.
- Recommendations are sequenced by value, risk, readiness, and dependencies.
- Reassessment is built into the lifecycle.
