---
name: predictive-model-development
description: Runs and documents predictive or statistical model development (clustering, forecasting, driver/regression models, segmentation) as a repeatable six-stage workflow. Forecasting here follows Hyndman & Athanasopoulos, *Forecasting: Principles and Practice* (fpp3, otexts.com/fpp3) — a genuinely uncertain future value estimated from patterns in data, not an already-scheduled or precisely calculable value (their sunrise-time-vs-currency-rate contrast: a recorded invoice due date is the sunrise time, not the forecast). The six stages — dataset/feature framing, EDA, dimensionality/feature reduction, model selection, validation, and translation — are phase-aligned to CRISP-DM, with per-stage decision logging in the spirit of Model Cards (Mitchell et al., 2019) so technique choices can vary project to project while the rationale and rejected-alternative trail stay auditable. Use when building a model for a finance/accounting audience where the process would otherwise be undocumented and unrepeatable. Use `financial-variance-analysis` instead for actual-vs-plan variance narratives against predefined dimensions, `reconciliation-analytics` instead for cross-system ledger matching, and `dimensional-modeling` or `data-model-requirements-and-quality` instead for data schema/warehouse modeling — "model" there means a data structure, not a statistical or predictive model. Not for a simple total, sum, or breakdown by an already-known dimension — those are direct answers or `financial-variance-analysis`.
---

# Predictive Model Development

This skill covers the part of an analytics project that happens after the question is framed and the raw data is profiled: building a predictive or statistical model — clustering, forecasting, a driver/regression model, a segmentation scheme — for an audience that is finance and accounting, not data science. The techniques used will differ by project; the discipline of logging what was tried, why, and what was rejected does not.

## When to Use

- Building a clustering, forecasting, driver/regression, or segmentation model (e.g., workload allocation via cluster analysis, a flash/forecast reporting model, a throughput analytics model built for future deeper analysis).
- Performing EDA, feature engineering, PCA/dimensionality reduction, or model selection as part of an analytics project.
- The process would otherwise be ad hoc and undocumented — each project uses a different combination of techniques, so nothing about a prior pass is directly reusable unless the reasoning, not just the output, was captured.
- Translating model output for stakeholders who will not sanity-check statistical assumptions themselves.

## Relationship to Other Skills

- Use `question-driven-data-projects` first to frame the business question and hypotheses; use this skill once the project has moved from "what should we ask" to "build the model."
- Use `data-profiling` first to understand the raw dataset; this skill picks up from there for feature engineering and modeling.
- Use `financial-variance-analysis` instead for actual-vs-plan or period-over-period variance narratives against predefined dimensions (entity, account, product, region) — that is a fixed, well-defined comparison, not exploratory model development. Use this skill instead when the explanatory grouping itself is unknown and must be discovered, not just decomposed against a known dimension list.
- Use `reconciliation-analytics` instead for cross-system or ledger matching.
- Use `dimensional-modeling` or `data-model-requirements-and-quality` instead for data schema/warehouse modeling.
- Use `analytics-storytelling` for the general principles of narrative communication; Stage 6 below applies those principles specifically to model output, but does not replace that skill for non-model analyses.

## Workflow

1. **Dataset & feature framing**
   - State the data sources and grain — and justify why that unit of analysis was chosen over plausible alternatives (e.g., vendor-level vs. invoice-level vs. processor-level), the same way Stage 4 justifies the chosen model over rejected ones.
   - Document feature engineering applied and why each feature was constructed the way it was.
   - Note known gaps or proxies used in place of ideal-but-unavailable data.

2. **Exploratory data analysis**
   - Explore distributions, relationships, and anomalies relevant to the modeling question.
   - Record what the exploration ruled in or ruled out, not just what was observed.

3. **Dimensionality / feature reduction**
   - State whether reduction (e.g., PCA) was needed and why.
   - Record what was kept vs. dropped and the interpretability cost of that choice.
   - If no reduction was needed, say so explicitly rather than leaving the stage blank.

4. **Model selection**
   - List the candidate approaches considered, not only the one chosen.
   - State why the chosen model won.
   - Record why each rejected candidate was rejected — this is usually the first context lost when the process is undocumented, and the most valuable to future projects.

5. **Validation**
   - State the validation approach used and what it did and did not test.
   - Record known limitations and the conditions under which the model would need to be revisited.

6. **Translation for a finance/accounting audience**
   - State the finding in plain language before any methodology.
   - Express uncertainty as a range or confidence level, never a single false-precise number.
   - Surface the assumptions the audience is implicitly trusting if they act on this output.
   - Avoid unexplained statistical jargon; if a technical term is necessary, define it in one clause.
   - Close with a specific, actionable recommendation tied to the finding.

## Output Template

```markdown
# Model Development Log: [Project Name]

## 1. Dataset & Feature Framing
- Data sources and grain (and why this grain, not an alternative):
- Feature engineering applied:
- Rationale:
- Known gaps or proxies:

## 2. Exploratory Data Analysis
- Patterns/relationships/anomalies found:
- What this ruled in or out:

## 3. Dimensionality / Feature Reduction
- Method used (or "none needed" + why):
- Kept vs. dropped:
- Interpretability cost:

## 4. Model Selection
- Candidates considered:
- Chosen approach:
- Why it won:
- Rejected candidates and why:

## 5. Validation
- Validation approach:
- What it did / did not test:
- Known limitations:

## 6. Translation
- Plain-language finding:
- Uncertainty (range/confidence, not a false-precise point estimate):
- Assumptions the audience is trusting:
- Recommended action:
```

## Quality Checklist

- Every stage has a documented rationale, not just an output or a chart.
- Rejected alternatives are recorded with why, not only the winning approach.
- The specific techniques used are free to vary by project; the six-stage log structure does not.
- Stage 6 output contains no unexplained statistical jargon and states uncertainty honestly.
- A future project facing a similar question could reconstruct the reasoning from the log alone, without re-running the analysis.
