---
name: evidence-planning
description: Defines the evidence needed to validate diagnostic claims, root-cause hypotheses, and intervention choices. Use when diagnosing business, data, process, organizational, governance, or technology issues where confidence depends on interviews, data pulls, process traces, logs, lineage, observations, or decision history.
---

# Evidence Planning

## When to Use
- A diagnosis depends on incomplete facts or stakeholder anecdotes.
- Root-cause hypotheses need validation.
- Recommendations should be separated from assumptions.
- The user needs a practical validation plan before action.

## Evidence Sources
Consider:
- Interviews.
- Data pulls.
- Process traces.
- Workflow observation.
- System logs.
- Report or data lineage.
- Decision history.
- Policy or control review.
- Stakeholder mapping.
- Before/after metrics.
- Exception analysis.

## Workflow
1. List known facts.
2. Separate interpretations from facts.
3. Identify the hypotheses that need validation.
4. Define evidence that would confirm or disconfirm each hypothesis.
5. Prioritize the smallest evidence set that can change the decision.
6. Assign likely evidence owners or sources.

## Output Template
```markdown
## Evidence Plan
| Claim or hypothesis | Evidence needed | Source | Owner or contact | Confidence impact | Priority |
|---|---|---|---|---|---|

## Evidence Discipline
- Facts:
- Interpretations:
- Hypotheses:
- Recommendations:
```

## Quality Checklist
- Evidence is tied to a decision, hypothesis, or recommendation.
- The plan includes disconfirming evidence, not only confirming evidence.
- Evidence collection is proportionate to risk and urgency.
- The next evidence step is practical and assignable.
