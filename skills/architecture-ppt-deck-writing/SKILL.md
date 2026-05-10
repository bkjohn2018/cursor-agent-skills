---
name: architecture-ppt-deck-writing
description: Structures architecture, operating model, capability model, governance framework, and transformation concept decks with clear visual hierarchy, decision narrative, layered explanation, reusable patterns, and implementation path. Use when turning architecture guides, governance models, operating models, or framework visuals into executive or stakeholder PowerPoint decks.
---

# Architecture PPT Deck Writing

Use this skill to turn an architecture or operating model into a presentation that leaders and practitioners can understand, discuss, and approve.

## When to Use

- Creating decks for reference architectures, operating models, governance frameworks, or capability models.
- Explaining layered models, dependency structures, maturity paths, or adoption sequences.
- Presenting a domain-agnostic pattern with one worked example.
- Translating a visual architecture into executive-ready slides.
- Preparing a deck that needs both concept clarity and decision readiness.

## Relationship to Other Skills

- Use `governance-ppt-deck-writing` for committee decision framing, risks, controls, remediation, and governance review.
- Use `executive-summary-writing` for the leadership message and decision ask.
- Use `analytics-storytelling` for visual simplification, attention guidance, and decluttered narrative.
- Use `governance-writing-style-guide` for consistent terms, modal language, and accountability wording.

## Deck Structure Standard

Use this flow unless the user provides a stronger order:

1. Title and purpose.
2. Why this architecture is needed.
3. Core principle or thesis.
4. Reference architecture visual.
5. Layer-by-layer explanation.
6. Shared controls or common backbone.
7. Worked example.
8. Reuse pattern across domains.
9. Readiness gates or adoption sequence.
10. Decision request and next steps.
11. Appendix for definitions, detailed controls, templates, or source notes.

## Slide Writing Rules

- Use takeaway-oriented slide titles.
- Anchor the deck around one primary architecture visual.
- Explain complex visuals progressively; do not force the audience to decode the full model at once.
- Distinguish foundation layers from optional capabilities.
- Make dependencies explicit: what must be true before the next layer can be trusted.
- Use one architecture concept per slide.
- Keep implementation detail in the appendix unless it affects the decision.
- Show the worked example as proof of fit, not as the scope boundary.
- End with an explicit decision request or adoption path.

## Output Template

```markdown
# Architecture Deck Outline: [Topic]

## Slide 1: [Title]
- Purpose:
- Audience:
- Decision or outcome:

## Slide 2: [Why now]
- Takeaway:
- Context:
- Risk of inaction:

## Slide 3: [Core principle]
- Principle:
- Implication:

## Slide 4: [Reference architecture]
- Visual:
- Speaker note:

## Slide 5+: [Layer explanation]
- Layer:
- What it governs:
- What it enables:
- Readiness requirement:

## Slide N: [Worked example]
- Example:
- Why it was selected:
- What it proves:

## Slide N+1: [Adoption path]
- Step 1:
- Step 2:
- Step 3:

## Final slide: [Decision request]
- Decision needed:
- Recommended action:
- Owner:
- Timing:
```

## Acceptance Criteria

- Deck can be understood without the presenter reading the source document aloud.
- The reference visual is introduced before details and revisited through the story.
- Each layer has a distinct purpose, owner implication, and readiness dependency.
- Optional capabilities are clearly marked as optional or readiness-gated.
- The worked example supports reuse instead of narrowing the architecture.
- The final decision request is explicit and actionable.
