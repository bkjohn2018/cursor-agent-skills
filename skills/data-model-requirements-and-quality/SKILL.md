---
name: data-model-requirements-and-quality
description: Captures and validates data model requirements using Hoberman-style conceptual/logical framing plus Data Model Scorecard quality categories, designed to complement Kimball dimensional delivery. Use when users need better model clarity, scope control, and formal model quality scoring before implementation.
---

# Data Model Requirements And Quality

## When to Use
- Requirements are unclear before dimensional modeling.
- Teams need stronger conceptual/logical alignment with business language.
- Models need quality review before physical implementation.

## Workflow
1. Ask strategic framing questions (scope, audience, decision use, time horizon, constraints).
2. Produce conceptual model view (key concepts and relationships).
3. Produce logical model view (keys, cardinality, attribute definitions).
4. Confirm integration points with Kimball dimensional targets (facts, dimensions, conformance).
5. Run Data Model Scorecard checks and resolve gaps.
6. Produce review-ready findings with severity and remediation actions.

## Data Model Scorecard Categories
Use these quality categories as review headings:
1. Correctness
2. Completeness
3. Scheme
4. Structure
5. Abstraction
6. Standards
7. Readability
8. Definitions
9. Consistency
10. Data

## Complement To Kimball
- Use this skill before or alongside `dimensional-modeling`.
- Keep Kimball as default for warehouse/mart design decisions.
- Use this skill to improve requirement quality, naming, and model readability.
- Use `data-profiling` first to ground conceptual/logical requirements in the real structure and quality of the source data.

## Output Template
```markdown
# Model Requirements and Quality Review

## Strategic framing
- Business objective:
- Scope boundaries:
- Time perspective:
- Primary consumers:

## Conceptual model summary
- Concepts:
- Relationships:
- Major definitions:

## Logical model summary
- Candidate entities:
- Candidate keys:
- Relationship cardinalities:
- Critical attributes/domains:

## Dimensional handoff notes
- Candidate facts:
- Candidate dimensions:
- Conformance considerations:

## Quality scorecard
- Correctness:
- Completeness:
- Scheme:
- Structure:
- Abstraction:
- Standards:
- Readability:
- Definitions:
- Consistency:
- Data:
- Open issues:
```

## Quality Checklist
- Scope and abstraction choices are explicit.
- Definitions are testable and non-ambiguous.
- Keys and relationships are validated with business users.
- Dimensional handoff is clear enough for Kimball design.
- Scorecard findings include priorities and remediation owners.
