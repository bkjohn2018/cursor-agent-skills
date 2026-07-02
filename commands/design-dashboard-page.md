Design a specific dashboard page from requirements, a screenshot, or an existing product brief.

Collect these inputs first:
- Page name and page purpose
- Target user and operating cadence
- Decisions/actions supported on the page
- Required KPIs, visuals, lists, and workflow states
- Desired drill-down destinations
- Reference screenshots, wireframes, or design patterns

Execute by phase:

1. **Page framing**
   - Apply `dashboard-product-framing`.
   - Clarify the page role: overview, detail, workflow queue, or exception investigation page.

2. **Information architecture**
   - Apply `dashboard-information-architecture`.
   - Define section order, right rail vs main canvas, filters, and drill paths.

3. **Content model**
   - Apply `governance-dashboard-content-model` when the page represents governed entities or workflow states.
   - Define what objects appear directly vs only in drill-down.

4. **Metric semantics**
   - Apply `dashboard-metric-semantics` and `metric-governance` when KPIs or status indicators are present.
   - Define thresholds, comparators, status colors, and click behavior.

5. **Visual narrative**
   - Apply `finance-dashboard-design` when the page is finance-led, KPI-dense, or a governed operating page.
   - Apply `analytics-storytelling` for message clarity and emphasis.
   - Choose page hierarchy, visual patterns, and emphasis strategy.

Output must include:
1. Page purpose and user action summary
2. Section-by-section layout spec
3. KPI and interaction summary
4. Drill path map
5. Visual and narrative guidance for implementation
