Review a dashboard for semantic consistency across metrics, labels, object states, statuses, and drill behavior.

Collect these inputs first:
- Pages or dashboard areas in scope
- Metric specs, glossary terms, and governed definitions if available
- Known disputed labels, statuses, or KPI logic
- Content model or entity list if available
- Desired review depth: quick, standard, comprehensive

Review by gate:

1. **Business terms and governed objects**
   - Apply `business-glossary-management` and `governance-dashboard-content-model`.
   - Check entity names, statuses, ownership labels, and lifecycle terms.

2. **Metric and status semantics**
   - Apply `metric-governance` and `dashboard-metric-semantics`.
   - Check formulas, thresholds, ring/gauge meanings, trend arrows, status colors, and drill behavior.

3. **Traceability and governance alignment**
   - Apply `metadata-and-lineage` and `data-governance` as relevant.
   - Check whether visible dashboard semantics map cleanly to source assets, controls, and operating definitions.

Output must include:
1. Semantic consistency review summary
2. Metric definition conflicts
3. Object/state naming conflicts
4. Status/threshold mismatches
5. Recommended standardization actions and priorities
