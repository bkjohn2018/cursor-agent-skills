Define dashboard KPIs and status semantics so metrics are trustworthy, actionable, and drillable.

Collect these inputs first:
- Dashboard or page name
- Metric names or candidate KPI ideas
- User decisions supported by each metric
- Source systems and data owners
- Desired thresholds, targets, SLA rules, or prior-period comparisons
- Known disputes or ambiguity in metric meaning
- Required drill-down destinations

Execute by phase:

1. **Decision alignment**
   - Apply `question-driven-data-projects`.
   - Confirm what each metric is meant to help the user decide or monitor.

2. **Metric governance**
   - Apply `metric-governance`.
   - Define formula, grain, ownership, refresh cadence, and approval status.

3. **Dashboard semantics**
   - Apply `dashboard-metric-semantics`.
   - Define status logic, comparator logic, UI labels, ring/gauge meaning, and drill behavior.

4. **Traceability and data trust**
   - Apply `metadata-and-lineage`, `data-quality-controls`, and `data-quality-assessment` as relevant.
   - Clarify source lineage, quality checks, and known limitations.

Output must include:
1. KPI catalog
2. Metric-by-metric semantic spec
3. Status and threshold rules
4. Drill behavior and default filters
5. Data trust notes, assumptions, and unresolved definition issues
