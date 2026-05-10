---
name: dimensional-modeling
description: Designs dimensional models using Kimball-first methods, including the four-step process, star schema patterns, conformed dimensions, and bus matrix planning, while incorporating complementary Hoberman techniques for clarity and quality. Use when building analytical marts, defining fact/dimension structures, or standardizing enterprise-ready dimensional models.
---

# Dimensional Modeling

## When to Use
- New analytics mart design.
- Refactoring wide operational schemas for BI.
- Requests for fact-dimension modeling.
- Defining enterprise conformance across multiple marts.

## Kimball-First Workflow
1. Select the business process.
2. Declare the grain before selecting any facts or dimensions.
3. Identify dimensions for descriptive context.
4. Identify facts and classify additive behavior.
5. Choose fact table pattern (transaction, periodic snapshot, accumulating snapshot, or factless).
6. Design surrogate-keyed dimensions and SCD behavior.
7. Define conformed dimensions/facts and update the bus matrix.
8. Validate drill paths and cross-process analysis use cases.

## Hoberman Complementary Techniques
- Use conceptual and logical model checkpoints before final physical design.
- Use explicit scope and abstraction decisions to keep models understandable.
- Use clear naming and definition discipline across entities, attributes, and relationships.
- Apply Data Model Scorecard category checks to catch ambiguity, missing definitions, structure issues, and consistency gaps.

## Output Template
```markdown
# Dimensional Model Spec

## Business process and decision context
- Process:
- Core business questions:

## Fact table
- Grain:
- Fact table type:
- Measures:
- Additivity class:
- Keys:

## Dimensions
- Dimension:
  - Natural key:
  - Surrogate key:
  - SCD type:
  - Hierarchies:
  - Role-playing usage:

## Enterprise conformance
- Shared dimensions:
- Conformed facts:
- Bus matrix row/column impact:

## Model quality checks (Hoberman-inspired)
- Scope and abstraction choices:
- Definition completeness:
- Naming consistency:
- Data Model Scorecard category ratings:
  - Correctness / Completeness / Scheme / Structure / Abstraction
  - Standards / Readability / Definitions / Consistency / Data
- Open risks:
```

## Quality Checklist
- Grain is declared first and consistently enforced.
- Fact table type matches process behavior.
- Fact grain is explicit and stable.
- Measures align with grain and additive rules.
- Conformed dimensions and facts enable drill-across.
- Surrogate keys and SCD choices are justified.
- Naming and definitions are clear to business and technical users.
- Scorecard category ratings are captured before model sign-off.
