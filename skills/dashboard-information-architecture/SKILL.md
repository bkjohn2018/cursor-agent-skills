---
name: dashboard-information-architecture
description: Designs page hierarchy, navigation, section structure, and drill paths for analytics webspaces and operational dashboards. Use when translating dashboard requirements into page architecture, app shell design, or drill-down flows.
disable-model-invocation: true
---

# Dashboard Information Architecture

## When to Use
- A dashboard needs to become a multi-page webspace.
- The team has sections/cards but no page hierarchy.
- Navigation, drill paths, and page responsibilities are unclear.

## Workflow
1. Start from user decisions and define top-level page types.
2. Organize the experience into global nav, local nav, and in-page sections.
3. Assign each KPI card, list, and visual a destination or drill behavior.
4. Separate overview, investigation, transaction/detail, and administration surfaces.
5. Validate that users can move from summary -> diagnosis -> action without dead ends.

## Page Pattern Defaults
- Overview page for status, trends, and exceptions.
- Domain detail pages for workflow stages or governed entities.
- Object detail pages for records like controls, issues, evidence, or metrics.
- Optional admin/config pages for standards, mappings, thresholds, and ownership.

## Output Template
```markdown
# Dashboard IA Spec

## Global navigation
- ...

## Page map
| Page | Purpose | Primary user | Main actions |
|---|---|---|---|

## Section hierarchy
- Top band:
- Middle analytical band:
- Operational band:
- Right rail / support panel:

## Drill paths
- Card -> Detail page
- Trend chart -> Filtered list
- Exception count -> Issue queue
```

## Quality Checklist
- Every top-level page has a distinct responsibility.
- Drill paths are explicit and purposeful.
- Navigation mirrors the operating model, not just the data model.
- Users can get from signal to action in a few steps.
