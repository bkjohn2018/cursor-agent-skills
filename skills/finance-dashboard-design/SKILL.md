---
name: finance-dashboard-design
description: Designs finance, governance, and operating dashboards around governed metrics, decision workflows, and clear visual hierarchy. Use when building or improving KPI-heavy dashboards for leadership and operating teams, especially when metric trust and drill-path clarity matter.
---

# Finance Dashboard Design

## When to Use
- Designing new KPI dashboards for finance stakeholders.
- Designing governance or operating dashboards that need finance-style metric discipline.
- Improving dashboard readability and decision utility.
- Requests for finance visualization standards.

## Workflow
1. Start from `dashboard-product-framing`, `dashboard-metric-semantics`, and `dashboard-information-architecture`; apply them first only if those decisions do not already exist.
2. Apply `governance-dashboard-content-model` when governed objects or workflow stages are involved.
3. Synthesize the upstream decisions into a dashboard layout that moves from summary to diagnostic detail.
4. Choose visual emphasis, KPI hierarchy, and section balance for quick scan plus drill-down.
5. Validate usability and narrative coherence.

## Complementary Skills
- `dashboard-product-framing` for product definition.
- `dashboard-information-architecture` for page and nav structure.
- `dashboard-metric-semantics` for KPI card and status logic.
- `dashboard-frontend-implementation` when moving into actual UI build.
- `analytics-storytelling` for chart/message clarity.

## Output Template
```markdown
# Dashboard Design Spec

## Audience and purpose
- Primary users:
- Decisions supported:

## KPI layer
- KPI:
- Definition:
- Target:

## Visual layout
- Top row:
- Mid row:
- Diagnostic section:

## Interactions
- Filters:
- Drill-down:
```

## Quality Checklist
- Each visual answers a specific question.
- KPIs use governed definitions.
- Layout supports quick scan then deep dive.
- Interaction model is simple and predictable.
- Product, semantics, and IA decisions are explicit before implementation and are not recreated unnecessarily.
