---
name: metadata-and-lineage
description: Documents technical and business metadata plus upstream/downstream lineage for specific data assets, metrics, dashboards, reports, or integrations. Use when users ask for lineage mapping, impact analysis, or asset-level metadata documentation. Use data-standards-management when defining enterprise metadata requirements or standards.
---

# Metadata And Lineage

## When to Use
- Impact analysis before schema or logic changes.
- Governance efforts requiring system traceability.
- Requests for business and technical metadata documentation.

## Workflow
1. Define lineage scope (dataset, metric, dashboard, report).
2. Capture upstream sources, transforms, and owners.
3. Capture downstream consumers and decision points.
4. Record business, technical, and operational metadata fields.
5. Record critical metadata fields and refresh dependencies.
6. Publish impact notes and high-risk dependencies.

## DMBOK Alignment
- Aligns to Metadata Management activities:
  - define metadata requirements
  - create and maintain metadata
  - support lineage and impact analysis
  - enforce metadata standards and controls

## Output Template
```markdown
# Lineage Summary

## Asset
- Name:
- Type:
- Owner:

## Upstream
- Source:
- Transformation:
- Refresh:

## Downstream
- Consumer:
- Artifact:
- Decision impact:

## Risk notes
- ...
```

## Quality Checklist
- Lineage chain is complete from source to consumption.
- Ownership is shown at each critical step.
- Refresh dependencies and SLAs are included.
- Impact analysis identifies high-risk breakpoints.
