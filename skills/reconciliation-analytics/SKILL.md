---
name: reconciliation-analytics
description: Performs reconciliation analysis between systems, ledgers, and reports to identify breaks, root causes, and corrective actions. Use when validating financial consistency across sources.
---

# Reconciliation Analytics

## When to Use
- System-to-system or report-to-ledger mismatch investigations.
- Period close control activities.
- Requests for break analysis and reconciliation packs.

## Workflow
1. Define reconciliation scope, grain, and matching keys.
2. Align extraction timing and cutoff assumptions.
3. Match records and classify unmatched or mismatched items.
4. Quantify breaks by type, aging, and materiality.
5. Propose fixes and prevention controls.

## Output Template
```markdown
# Reconciliation Pack

## Scope
- Source A:
- Source B:
- Cutoff:
- Grain:

## Match results
- Matched count:
- Unmatched count:
- Net break amount:

## Break categories
- Timing:
- Mapping:
- Missing records:
- Calculation differences:

## Actions
1. ...
```

## Quality Checklist
- Matching logic and assumptions are explicit.
- Breaks are categorized with root-cause hypotheses.
- Materiality and aging are quantified.
- Remediation owners and ETAs are assigned.
