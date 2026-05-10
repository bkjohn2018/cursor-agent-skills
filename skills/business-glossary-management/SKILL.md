---
name: business-glossary-management
description: Defines and maintains governed business terms, canonical metric language, and approved synonyms across domains. Use when creating or updating a business glossary, resolving terminology conflicts, or standardizing definitions used in analytics, finance, and governance artifacts.
---

# Business Glossary Management

## When to Use
- A team uses multiple names for the same concept.
- Metric definitions conflict across reports or departments.
- New data products need approved business terminology.
- Governance asks for ownership, definitions, and usage rules.

## Workflow
1. Collect candidate terms from reports, dashboards, SOPs, and stakeholder language.
2. Normalize terms into canonical names, synonyms, and prohibited labels.
3. Draft each term with definition, business intent, formula linkage, and examples.
4. Assign domain owner, data steward, and approval status.
5. Record lineage links to source systems, tables, and metrics where applicable.
6. Run conflict review for duplicate terms or conflicting definitions.
7. Publish versioned glossary updates with change notes.

## DMBOK Alignment
- Supports Data Governance and Metadata Management through:
  - controlled business vocabulary
  - ownership and stewardship accountability
  - traceability to metrics, data assets, and standards

## Term Standard
For each glossary entry, include:
- `term`: Canonical business term.
- `definition`: Plain-language meaning with boundary conditions.
- `businessPurpose`: Why the term exists and what decision it supports.
- `domain`: Finance, Sales, Operations, HR, etc.
- `owner`: Accountable business role.
- `steward`: Day-to-day maintenance role.
- `approvedSynonyms`: Allowed alternate labels.
- `disallowedSynonyms`: Terms that should be avoided.
- `relatedMetrics`: Metrics that use or depend on the term.
- `sourceReferences`: Authoritative docs, systems, or policies.
- `status`: Proposed, reviewed, approved, retired.
- `effectiveDate`: Date term becomes authoritative.

## Conflict Resolution Rules
1. Prefer existing approved canonical terms over introducing net-new labels.
2. If two definitions overlap, split by business boundary (time, process, ownership, or scope).
3. If one term has multiple meanings, create disambiguated canonical variants.
4. If a term is retained for legacy use, mark as deprecated and map to replacement.
5. Require owner sign-off before changing any approved definition.

## Output Template
```markdown
# Glossary Update Package

## Change summary
- Version:
- Date:
- Scope:

## Added terms
| Term | Definition | Domain | Owner | Status |
|---|---|---|---|---|

## Updated terms
| Term | What changed | Impacted artifacts | Approval |
|---|---|---|---|

## Deprecated terms
| Term | Replacement | Retirement date |
|---|---|---|

## Open decisions
1. ...
```

## Quality Checklist
- Each term has a single canonical meaning and clear boundaries.
- Synonym policy is explicit (allowed vs disallowed).
- Ownership and stewardship are assigned.
- Definition changes include impact and migration guidance.
- Terminology is consistent with metric governance and reporting standards.
