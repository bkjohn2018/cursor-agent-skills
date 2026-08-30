---
name: question-driven-data-projects
description: Frames analytics work around business questions, strategic objectives, available data realities, and decision value. Use when defining analysis scope, shaping data projects, or when users ask to start with the right questions before selecting methods, models, or AI.
---

# Question Driven Data Projects

## When to Use
- New analytics requests with vague scope.
- Projects that need clear business decisions and measurable outcomes.
- Requests to turn stakeholder questions into an analysis plan.
- Teams are jumping into tools/models before clarifying value and constraints.

## Workflow
1. Capture the core business question, decision owner, and intended business value.
2. Identify pain points, objectives, and what success looks like for stakeholders.
3. Inventory available data, data gaps, and time horizon constraints.
4. Assess skillset, technology, and governance readiness for the project scope.
5. Rewrite the question into 1-3 testable hypotheses.
6. Define success criteria, required dimensions, and required metrics.
7. Map each hypothesis to needed data sources, costs, risks, and assumptions.
8. Produce a scoped project brief with milestones and explicit go/no-go criteria.

## Complementary Integration
- With `dimensional-modeling`: use question outputs to select business process and declare grain.
- With `data-model-requirements-and-quality`: convert questions into conceptual/logical model requirements.
- With `data-governance`: align decisions to ownership, controls, and policy constraints.
- With `dashboard-product-framing`: turn the business question into dashboard users, decisions, and page scope.
- With `data-profiling`: once scoped, understand the raw dataset before analysis begins.
- With `descriptive-pattern-analysis`: once scoped, use for trend, cohort/category comparison, correlation, or benchmarking on already-known dimensions.
- With `predictive-model-development`: once scoped, use when a hypothesis calls for clustering, forecasting, driver/regression modeling, or discovering an unknown grouping.

## Output Template
```markdown
# Data Project Brief

## Core question and decision
- Business question:
- Decision to support:
- Decision owner:

## Business context
- Main pain points:
- Objectives:
- Definition of success:

## Data reality check
- Available data:
- Missing data:
- Time horizon:
- Trust/quality concerns:

## Delivery readiness
- Skillsets available:
- Technology constraints:
- Governance constraints:

## Hypotheses
1. ...
2. ...

## Success criteria
- Metric:
- Target:
- Timeframe:

## Required data
- Source:
- Grain:
- Key fields:

## Risks, costs, and assumptions
- Cost drivers:
- ...

## Stage gate decision
- Proceed / Pause / Reframe:
- Rationale:
```

## Quality Checklist
- Question is decision-oriented, not purely descriptive.
- Hypotheses are testable with available or acquirable data.
- Success criteria are measurable and time-bound.
- Data requirements are explicit at the right grain.
- Risks, costs, and constraints are identified before detailed build work.
