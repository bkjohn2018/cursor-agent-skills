---
name: dashboard-frontend-implementation
description: Implements dashboards and analytics webspaces through reusable frontend components, data contracts, mock-first development, and clear interaction states. Use when building the actual UI for dashboard pages, app shells, KPI cards, filters, and drill-down views.
disable-model-invocation: true
---

# Dashboard Frontend Implementation

## When to Use
- Moving from requirements/design into frontend delivery.
- Building reusable dashboard components and app shells.
- Implementing mock-data prototypes before backend completion.

## Workflow
1. Start from the product brief, IA spec, and metric semantics.
2. Break the page into reusable components: shell, nav, filter bar, cards, charts, lists, detail panels.
3. Define component props and data contracts before implementation.
4. Build mock-first screens with realistic empty, loading, error, and stale-data states.
5. Add responsive behavior, drill interactions, and accessibility hooks.
6. Validate against the target user flows, not just pixel resemblance.

## Implementation Defaults
- Prefer reusable layout primitives over page-specific hacks.
- Separate presentational components from data-fetching containers.
- Keep status, thresholds, and labels driven by semantic config where possible.
- Design for progressive enhancement from mock data to live APIs.

## Output Template
```markdown
# Frontend Implementation Plan

## Page shell
- Layout regions:
- Navigation pattern:

## Component map
| Component | Responsibility | Input contract |
|---|---|---|

## Data states
- Loading:
- Empty:
- Error:
- Partial/stale:

## Interaction states
- Hover:
- Selected:
- Drill-down:
- Filtered:
```

## Quality Checklist
- Components reflect semantic requirements, not just visuals.
- Mock and live data can share the same contracts.
- Empty/loading/error states are intentional.
- Reusable components are favored over one-off page code.
