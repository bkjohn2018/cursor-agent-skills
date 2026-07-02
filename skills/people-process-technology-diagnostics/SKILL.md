---
name: people-process-technology-diagnostics
description: Maps People, Process, and Technology interactions in complex business, data, operational, governance, or technology issues. Use when a problem spans ownership, decision rights, workflow, handoffs, controls, systems, data, integrations, reports, automation, or adoption.
---

# People Process Technology Diagnostics

## Core Principle
People, Process, and Technology are overlapping lenses, not mutually exclusive boxes.

## When to Use
- A visible symptom could come from more than one layer of the operating system.
- A tool, team, or process is being blamed before interactions are understood.
- The user needs to see how ownership, workflow, data, controls, and systems reinforce or constrain one another.

## Diagnostic Lenses
- **People**: Ownership, decision rights, skills, incentives, trust, communication, resistance, capacity.
- **Process**: Workflow, handoffs, timing, controls, policies, feedback loops, rework, accountability.
- **Technology**: Systems, data structures, integrations, reports, automation, access, tool limitations, lineage.
- **Interactions**: Where one layer compensates for another, exposes weakness in another, or creates cross-layer friction.

## Workflow
1. Identify relevant people, process, and technology dynamics.
2. Note where the layers overlap or compensate for each other.
3. Flag where a person is being blamed for a design issue.
4. Flag where a tool is being blamed for a process or ownership issue.
5. Flag where process failure reflects unclear incentives, decision rights, or governance.
6. Carry the most important interactions into edge diagnostics.

## Output Template
```markdown
## People / Process / Technology Map
- People dynamics:
- Process dynamics:
- Technology dynamics:
- Key interactions:
- Most important interaction to test:
```

## Quality Checklist
- The map does not claim People, Process, and Technology are MECE.
- Interactions are more important than labels.
- The analysis avoids blaming a node before examining surrounding relationships.
- Findings can feed into `edge-diagnostics` or `root-cause-hypothesis-testing`.
