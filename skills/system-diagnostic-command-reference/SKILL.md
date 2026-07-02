---
name: system-diagnostic-command-reference
description: Orchestrates modular system-aware diagnostic skills into command-style workflows such as quick scan, focused diagnostic, full diagnostic, edge map, root-cause hypotheses, evidence plan, facilitation guide, executive brief, and artifact builder.
---

# System Diagnostic Command Reference

## Purpose
Use this skill to choose and assemble the right diagnostic workflow without loading every diagnostic method at once. The slash-command names below are command-style workflow labels, not executable Cursor commands unless implemented separately.

## Critical Controls and Governance Rule
If the output may affect controls, governance decisions, policy, standards, compliance posture, ownership, approvals, audit evidence, financial reporting, regulated data handling, or risk acceptance, treat the request as critical.

Do not use `/quick-scan` as the final workflow for critical requests. Escalate to at least `/focused-diagnostic` and include evidence, failure-mode, ownership, and learning-loop checks. Use adjacent specialist skills such as `internal-control-design`, `data-governance`, `data-standards-management`, `policy-and-standard-writing`, `data-quality-controls`, or `finance-documentation-lifecycle` when the output becomes a governed artifact.

Policies, procedures, controls, standards, processes, and governance artifacts may evolve, but changes should be routed through the appropriate lifecycle, approval, evidence, and ownership process rather than introduced ad hoc during diagnosis.

## Human-in-the-Loop Control Gate
If a workflow may create, revise, retire, reinterpret, or materially affect a control or governance artifact, including but not limited to policies, procedures, standards, processes, control descriptions, approval rights, ownership models, evidence requirements, or governance workflows, do not proceed on assumptions.

Request explicit user instruction or affirmation before making or drafting the change. If the request is ambiguous, ask for clarification rather than inferring intent. Diagnostic discussion may identify possible changes, but implementation, drafting, revision, retirement, or approval language requires explicit confirmation and the appropriate lifecycle, ownership, evidence, and review path.

## Command Map

### `/quick-scan`
Use for small issues, early thinking, or fast orientation.

Skills:
- `problem-triage`
- `system-sensing`
- `edge-diagnostics` only for the most likely stressed edge

Output:
```markdown
## Quick Scan
1. Likely read of the situation.
2. Most likely stressed edge.
3. Best next action.
4. Confidence and what to verify.
```

### `/focused-diagnostic`
Use for recurring, ambiguous, cross-functional, or moderately risky issues.

Skills:
- `problem-triage`
- `diagnostic-scope-control`
- `system-sensing`
- `people-process-technology-diagnostics`
- `edge-diagnostics`
- `root-cause-hypothesis-testing`
- `evidence-planning`
- `intervention-sizing`

Output:
```markdown
## Focused Diagnostic
1. What the system is showing.
2. Real question.
3. People / Process / Technology interactions.
4. Top stressed edges.
5. Root-cause hypotheses.
6. Evidence needed.
7. Recommended first moves.
```

### `/full-diagnostic`
Use for chronic, strategic, political, high-cost, compliance-related, enterprise, or high-stakes issues.

Skills:
- `system-aware-diagnostic-kernel`
- `problem-triage`
- `diagnostic-scope-control`
- `system-sensing`
- `people-process-technology-diagnostics`
- `edge-diagnostics`
- `root-cause-hypothesis-testing`
- `evidence-planning`
- `intervention-sizing`
- `systems-failure-mode-check`
- `adoption-and-ownership-planning`
- `learning-loop-design`
- `facilitation-design` if stakeholder alignment is required
- `executive-diagnostic-synthesis`

Output:
```markdown
## Full System Diagnostic
1. Executive diagnostic summary.
2. Scope and decision supported.
3. What the system is showing.
4. People / Process / Technology map.
5. Edge diagnostic table.
6. Root-cause hypotheses table.
7. Evidence plan.
8. Intervention sizing.
9. Adoption and ownership plan.
10. Learning loop.
```

### `/edge-map`
Use when the user specifically wants to diagnose handoffs, feedback loops, ownership, definitions, trust, timing, or interfaces.

Skills:
- `diagnostic-scope-control`
- `system-sensing`
- `people-process-technology-diagnostics` when People / Process / Technology interactions matter
- `edge-diagnostics`

### `/root-cause-hypotheses`
Use only after enough context exists to propose root causes as testable hypotheses, or when the user explicitly asks for hypotheses.

Skills:
- `system-sensing`
- `edge-diagnostics` when relationship context is missing
- `root-cause-hypothesis-testing`
- `evidence-planning`

### `/evidence-plan`
Use to define interviews, data pulls, process traces, system logs, observations, and validation steps.

Skills:
- `diagnostic-scope-control`
- `root-cause-hypothesis-testing` if hypotheses are not yet clear
- `evidence-planning`

### `/facilitation-guide`
Use when the user needs to lead a meeting, workshop, retrospective, governance session, or stakeholder discussion.

Skills:
- `system-sensing`
- `edge-diagnostics`
- `facilitation-design`

### `/executive-brief`
Use when the user needs a concise leadership-ready summary.

Skills:
- `executive-diagnostic-synthesis`
- `systems-failure-mode-check` when stakes are high
- `adoption-and-ownership-planning` when ownership or governance is part of the decision

### `/artifact`
Use when the user needs a durable output such as a memo, diagnostic map, decision brief, workshop guide, roadmap, scorecard, or learning loop.

Skills:
- Select the diagnostic skills needed for the artifact.
- Use `executive-diagnostic-synthesis` for leadership-facing artifacts.
- Use `facilitation-design` for workshop artifacts.
- Use `intervention-sizing` for roadmap artifacts.
- Use `evidence-planning` for validation artifacts.

## Escalation Rules
- Escalate from Quick Scan to Focused Diagnostic when the issue is recurring, ambiguous, cross-functional, or ownership is unclear.
- Escalate from Focused Diagnostic to Full Diagnostic when recommendations affect roles, funding, governance, systems, policy, compliance, or leadership decisions.
- Escalate any controls, governance, compliance, audit, financial reporting, regulated data, formal approval, or risk acceptance impact to at least Focused Diagnostic.
- Stop and ask for clarification when missing decision context would materially change the answer.
- Stop diagnosing and recommend action when the next step is obvious, low-risk, reversible, and useful for learning.

## Quality Checklist
- The command loads the smallest useful set of skills.
- The output matches the user's requested artifact or decision need.
- The workflow avoids framework stacking.
- The response preserves the signature method: edges before nodes.
