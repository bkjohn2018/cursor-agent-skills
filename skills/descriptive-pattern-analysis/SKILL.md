---
name: descriptive-pattern-analysis
description: Performs descriptive/exploratory analysis on already-known dimensions — trend over time, comparison across existing cohorts or categories, correlation between measured variables, and benchmarking against a reference — for a finance/accounting audience, picking up after `data-profiling` and before `analytics-storytelling`. Trend here follows Hyndman & Athanasopoulos, *Forecasting: Principles and Practice* (fpp3, otexts.com/fpp3): "a long-term increase or decrease in the data" isolated from seasonal/cyclic effects — not a raw YTD cumulative total or a plain period-over-period line, and not to be confused with seasonal (fixed, known-period) or cyclic (variable-frequency, economic) patterns, which the book explicitly warns get conflated. Correlation is described as a relationship, never stated as causation unless a controlled comparison supports it. Use `predictive-model-development` instead when the goal is discovering an unknown grouping (clustering), building a statistical model, or forecasting a genuinely uncertain future value (also Hyndman-anchored there) — this skill's techniques operate only on dimensions and time windows that are already known, including its own use of "EDA," which here means the whole descriptive deliverable, not `predictive-model-development`'s Stage 2 EDA that feeds a model. Use `financial-variance-analysis` instead for actual-vs-plan or period-over-period variance against predefined dimensions using volume/rate/mix decomposition. Use `reconciliation-analytics` instead for cross-system/ledger matching. Not for a simple total, sum, or single-period breakdown — those are direct answers.
---

# Descriptive Pattern Analysis

This skill covers descriptive, already-known-dimension analysis — the step between understanding a dataset (`data-profiling`) and communicating findings (`analytics-storytelling`) for requests that aren't actual-vs-plan variance, cross-system reconciliation, or model-building. It exists because a real trend claim, a real correlation claim, and a real benchmark claim each carry a specific statistical meaning that is easy to conflate with an informal one (a YTD total, a coincidence, an arbitrary reference point) — and a finance/accounting audience has no independent way to catch the difference.

## When to Use

- Describing a trend over time (in Hyndman's sense: a long-term direction net of seasonal/cyclic effects, not a raw running total or plain line chart).
- Comparing an already-known cohort or category — region, vendor tier, cost center, business unit — against another, or against itself over time.
- Investigating whether two or more measured variables move together (e.g., throughput vs. maintenance capex), stated as a relationship, not a cause.
- Benchmarking a metric against an internal or external reference point.
- Following up on an anomaly `data-profiling` flagged, to determine whether it's a real business signal or a data quality issue.

## Relationship to Other Skills

- Use `data-profiling` first to understand the raw dataset; this skill picks up once the data is known to be usable.
- Use `predictive-model-development` instead when the grouping itself is unknown and must be discovered (clustering), when a model is being built, or when a genuinely uncertain future value must be forecast.
- Use `financial-variance-analysis` instead for actual-vs-plan or period-over-period variance against predefined dimensions.
- Use `reconciliation-analytics` instead for cross-system or ledger matching.
- Use `analytics-storytelling` for the general principles of narrative communication; Stage 4 below applies those principles specifically to a descriptive finding, but does not replace that skill for other deliverables.

## Workflow

1. **Frame the descriptive question**
   - State the pattern being investigated, the known dimension or time window it applies to, and what it's being compared against (a prior period, a peer, an internal reference, or nothing — a pure observation).
   - Confirm the dimension or grouping is already known and defined; if it isn't, this is a `predictive-model-development` request instead.

2. **Select and apply the technique**
   - Choose from: trend (decomposition-aware — separate direction from seasonal/cyclic effects before claiming a trend exists), cohort/category comparison, correlation between measured variables, or benchmarking against a reference.
   - State briefly which technique was used and why it fits the question — this doesn't need the full rejected-alternatives log `predictive-model-development` requires, but the choice should not be silent.

3. **Check materiality and robustness**
   - Confirm the pattern is large enough to matter, not just visible.
   - Confirm the sample size or time window is adequate to support the claim.
   - Check whether removing an outlier or extending the window changes the conclusion.
   - For correlation claims, check whether both series share a common trend and re-test on detrended data (or period-over-period deltas) before concluding the relationship is real — two unrelated trending series will show high correlation purely because both are moving over time.

4. **Translate for a finance/accounting audience**
   - State the finding in plain language before any methodology.
   - If the finding involves correlation, state it as a relationship, not a cause, unless a controlled comparison supports causation.
   - Express uncertainty honestly rather than with false precision.
   - Avoid unexplained statistical jargon; if a technical term is necessary, define it in one clause.
   - Close with a specific, actionable recommendation tied to the finding.

## Output Template

```markdown
# Descriptive Analysis: [Question or Metric]

## 1. Framing
- Pattern being investigated:
- Known dimension / time window:
- Compared against:

## 2. Technique
- Technique applied:
- Why it fits this question:

## 3. Materiality & Robustness
- Is the pattern large enough to matter:
- Sample size / window adequacy:
- Sensitivity to outliers or window changes:

## 4. Translation
- Plain-language finding:
- Relationship vs. causation (if applicable):
- Uncertainty:
- Recommended action:
```

## Quality Checklist

- A trend claim reflects a decomposed long-term direction, not a raw cumulative total or an unexamined line chart.
- Cohort/category comparisons use dimensions that were already known going in, not an undisclosed discovered grouping.
- Correlation is never presented as causation without a controlled comparison to support it.
- A correlation between two trending series is re-tested on detrended data before being called real, not accepted at face value.
- The benchmark or comparison reference is explicit and defensible, not arbitrary.
- Materiality and robustness are checked before a finding is presented as decision-worthy.
- Translation is jargon-free and states uncertainty honestly.
