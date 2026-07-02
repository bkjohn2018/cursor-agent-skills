Build the dashboard shell and reusable UI foundation before or alongside page implementation.

Collect these inputs first:
- Technology stack and app framework
- Product brief or page spec
- Navigation requirements
- Pages to include now vs later
- KPI semantics and content model references
- Mock data availability vs live backend availability
- Responsiveness and accessibility expectations

Execute by phase:

1. **Implementation framing**
   - Apply `dashboard-frontend-implementation`.
   - Define page shell, layout regions, data contracts, component map, and data states.

2. **Architecture and navigation**
   - Apply `dashboard-information-architecture`.
   - Align app shell, page hierarchy, global nav, and drill paths.

3. **Design guidance**
   - Apply `finance-dashboard-design` when the shell supports a finance-led, KPI-dense, or governed operating dashboard.
   - Apply `analytics-storytelling` to preserve clear hierarchy, emphasis, and low-clutter communication.
   - Preserve clear hierarchy, signal emphasis, and minimal clutter.

4. **Semantic alignment**
   - Apply `dashboard-metric-semantics` and `governance-dashboard-content-model` as relevant.
   - Keep component behavior driven by metric and object semantics, not ad hoc UI logic.

Output must include:
1. Shell implementation plan
2. Reusable component map
3. Layout and navigation spec
4. Mock/live data contract plan
5. State handling plan for loading, empty, error, and stale data
