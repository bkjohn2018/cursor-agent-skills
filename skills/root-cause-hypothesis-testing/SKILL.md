---
name: root-cause-hypothesis-testing
description: Frames possible root causes as testable hypotheses for business, data, process, organizational, or technology problems. Use after system sensing or edge diagnostics, or when the user explicitly asks for root-cause hypotheses.
---

# Root-Cause Hypothesis Testing

## When to Use
- The user asks why a recurring or ambiguous problem is happening.
- Enough context exists to propose plausible causes without presenting them as facts.
- System sensing or edge diagnostics has identified stressed relationships that need evidence testing.

## Do Not Use When
- The user only needs a quick operational answer.
- There is not enough context to distinguish materially different causes.
- The analysis would imply blame without examining system structure.

## Workflow
1. Start from observed symptoms and stressed edges.
2. Convert possible causes into testable hypotheses.
3. Categorize each hypothesis.
4. Define evidence that would prove or disprove it.
5. Rate confidence as Low, Medium, or High.
6. State the risk of acting before confirming the hypothesis.

## Categories
Use one or more:
- People.
- Process.
- Technology.
- Governance.
- Data.
- Incentive.
- Timing.
- Strategy.

## Evidence Discipline
Separate:
- **Facts**: Directly observed or verified.
- **Interpretations**: What the facts may mean.
- **Hypotheses**: Possible causes to test.
- **Recommendations**: Actions that should follow only with enough confidence or as controlled tests.

## Output Template
```markdown
## Root-Cause Hypotheses to Test
| Hypothesis | Category | Evidence needed | Confidence | Risk of premature action |
|---|---|---|---|---|
```

## Quality Checklist
- Root causes are not stated as facts unless evidence is strong.
- Each hypothesis has disconfirming evidence, not just confirming evidence.
- Confidence reflects evidence quality, not narrative appeal.
- Premature-action risk is explicit.
