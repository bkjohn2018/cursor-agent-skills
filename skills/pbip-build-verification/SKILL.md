---
name: pbip-build-verification
description: Checks a built Power BI project (.pbip / TMDL / PBIR) against its approved `_brief/report-spec.md` (the `powerbi-report-planning` + `powerbi-report-design` output) and reports spec-versus-build divergence — field bindings, sort policy, color-map/conditional-formatting conformance, and semantic-model governance. Use when a Power BI report has been built or modified from an approved report spec and needs a pre-reload or pre-handoff check. Use dashboard-metric-semantics instead when the metric definitions themselves still need to be authored, not verified; use dashboard-frontend-implementation instead for generic (non-Power BI) dashboard UI; use powerbi-report-design instead to author or revise the brief itself.
disable-model-invocation: true
---

# PBIP Build Verification

## When to Use
- A `.pbip` report was built or modified from an approved `_brief/report-spec.md` and needs checking before Desktop reload or handoff.
- A build renders correctly on screen but you want to confirm it matches the spec, not just that it looks plausible.
- Remediating a prior build against a punch list, not generating one from scratch.
- No `_brief/report-spec.md` exists yet — use `powerbi-report-planning`/`powerbi-report-design` first; this skill has nothing to check a build against without it.

## Workflow
1. Locate the approved `_brief/report-spec.md` — specifically its embedded `Design Brief:` YAML (`color_map`, `pages[].layout_contract.placements[]` with `field_bindings`/`sort_policy`/`color_strategy`) and its `## Model requirements` section — and the target `.pbip` project's `*.SemanticModel/definition/` and `*.Report/definition/pages/**/visuals/*.json`.
2. Check the semantic model — 5 items. `report-spec.md`'s `## Model requirements` section only lists new/changed measures and columns in prose; it is not a governance contract. For structural governance, check against `semantic-model-authoring`'s own `modeling-guidelines.md` defaults instead — these are that skill's stated rules, not an invented standard, so a failure here means the build didn't follow guidance already available to it:
   - **Date table governance**: a named calendar table exists; auto date/time (`LocalDateTable_*`, `DateTableTemplate_*`) is removed, not just unused.
   - **Hidden columns**: every raw column an explicit measure aggregates is `isHidden`; no aggregatable raw column sits visible next to its measure.
   - **Naming**: table/column/measure names are business-friendly, not source-system names — cross-check any explicit new-measure/new-column names the report spec's `## Model requirements` names.
   - **Format strings**: every measure has one, matching the spec's stated precision/sign convention where the spec is explicit.
   - **Descriptions**: every visible object has a `///` description that states something non-obvious, not a restatement of the name.
3. Check each visual against the brief's `placements[]` entry for it — 4 items:
   - **Field bindings**: the `queryRef`(s) in each role projection match the placement's `field_bindings`, not a lookalike or a raw column standing in for a measure.
   - **Sort policy**: matches `placements[].sort_policy` (`value_desc` / `value_asc` / `category_asc` / `natural_order` / `none`). **Known schema gap**: this enum has no magnitude/absolute-value option. If the page's `purpose` calls for ranking by contribution or magnitude (e.g. a YoY driver chart) and the placement only has a signed `sort_policy`, that is a **brief gap**, not a build error — the spec cannot currently express what the page needs. Report it as a brief gap for whoever owns `report-spec.md`, not as a build finding.
   - **Color strategy / conditional formatting**: the visual's conditional-formatting objects match `placements[].color_strategy` (`measure_match` / `gradient` / `unique` / `semantic` / `none`). `color_strategy` only records the *design decision* to use conditional formatting — `powerbi-report-design`'s own reference material stops at "use conditional formatting for traffic-light status, heatmaps, or threshold-based alerts" and never specifies the PBIR mechanics. Check those mechanics against Known-Unsafe Build Patterns below regardless of what `color_strategy` says.
   - **Color literals vs. `color_map`**: every hex value in `visual.json` resolves to a `color_map` entry for the measure it's coloring — `measure_match` means exact base-color reuse across every card/line/bar/map/table for that measure; `gradient` means tint-to-base for that same measure. This is `powerbi-report-design`'s own "Color-map contract" gotcha — audit for mismatches, including near-misses a screenshot won't catch (e.g. `#2F6BFF` vs. a `color_map` entry of `#1F5EFF`). **`color_map` is measure-scoped only** — a placement can declare `color_strategy: measure_match` while showing a color with no measure behind it (a card's own value text, a plain textbox). For those, there is nothing in `color_map` to check against; check the hex instead against the spec's "Design system summary" prose (structural text/surface roles), and flag it as a **brief gap** if the placement's `color_strategy` implies a `color_map` entry that doesn't exist.
4. For anything the build attempts that has no documented-safe PBIR encoding, check it against Known-Unsafe Build Patterns first, then report it as an explicit build gap with the reason — do not guess an undocumented fix and do not silently drop it.
5. Report only. Do not edit model, report, or spec files during verification, and do not fix a brief gap by inventing schema the spec doesn't have — findings go back to whoever owns the build (build gaps) or whoever owns `report-spec.md` (brief gaps), the same separation `governance-bundle-qa-agent` uses against its own bundle.

## Known-Unsafe Build Patterns
Carry these forward as standing checks, not historical notes — each one passed `powerbi-report-author validate` clean and only broke at Desktop render or reload, and none of them appear in `powerbi-report-design`'s own gotchas/anti-patterns lists (those cover visual/design quality; these are DAX-query-engine and TMDL-parser structural failures):
- **TopN filter ordered by a DAX measure.** `OrderBy` inside a TopN filter's subquery must be a raw-column `Aggregation`, not a `Measure` expression — documented as a Desktop crash (`SemanticQueryRewriter.rewriteOrderBy`), not a silent failure. If the ranking value is a measure, TopN-by-N has no documented-safe encoding; report it as a build gap.
- **Conditional `dataPoint.fill` with no selector.** Renders successfully but paints every data point the same color regardless of the rule. Requires `"selector": {"data": [{"dataViewWildcard": {"matchingOption": 0}}]}` to evaluate per point.
- **`isAvailableInMdx: false` on a `sortByColumn` target.** Breaks the column it sorts with `does not have an attribute hierarchy enabled`. Check every hidden column against what references it (sort-by, hierarchy, variation) before disabling its MDX availability.
- **TMDL `///` description trailing an object's properties instead of leading them.** Parses for some placements, throws `Unexpected line type: Empty!` for others depending on what follows. Always place the description directly above the `table`/`column`/`measure` line, never after.
- **Comparing a `date`-typed source column to a `#datetime(...)` M literal.** Throws `We cannot apply operator < to types DateTime and Date` at refresh, not at validation. Match the literal constructor to the source column's actual type.
- **A measure and a hidden column sharing the same name in one table.** Passes `powerbi-report-author validate` clean, then fails Desktop *load itself* (not render, not reload) with `The '<name>' measure cannot be created because a column with the same name already exists`. Check every measure name against every column name in its own table, including hidden ones — a friendly-named measure paired with an identically-friendly-named raw column is the trap (e.g. measure `Units In` over hidden column `Units In`); keep the raw column's name distinct (its source-cased name, e.g. `UnitsIn`, is usually enough).
- **Visual-level `filterConfig` nested inside `visual` instead of as its sibling.** `powerbi-report-author validate` catches this cleanly (`/visual must NOT have additional properties (property: "filterConfig")`) — but if a build skipped that validation step, the schema error is the tell.

## Output Template
```markdown
# Build Verification Report

## Scope
- Report spec: [path to _brief/report-spec.md]
- Build: [.pbip path]
- Checked: [date]

## Semantic model
| Check | Status | Finding |
|---|---|---|
| Date table governance | Pass/Gap | |
| Hidden columns | Pass/Gap | |
| Naming | Pass/Gap | |
| Format strings | Pass/Gap | |
| Descriptions | Pass/Gap | |

## Visuals
| Visual | Field bindings | Sort policy | Color strategy / conditional formatting | Color literals vs. color_map |
|---|---|---|---|---|

## Known-unsafe patterns encountered
- ...

## Build gaps (spec asks for something the build didn't safely express)
- ...

## Brief gaps (the page needs something report-spec.md's schema can't express — e.g. magnitude sort)
- ...
```

## Quality Checklist
- Every finding cites a file and, where possible, a property path — not a general impression.
- Every "Pass" was checked against `report-spec.md`'s actual stated value, not assumed from a render that looked right.
- Build gaps and brief gaps are never conflated — they have different owners.
- Every dropped requirement is logged as a gap with a reason, never silently omitted.
- The report contains no fixes — only findings, routed back to whoever owns the build or the spec.
- Known-Unsafe Build Patterns is checked explicitly, not relied on to be remembered.

## Relationship to Other Skills
- Consumes `_brief/report-spec.md` as produced by `powerbi-report-planning` (the locked spec) and `powerbi-report-design` (the embedded `Design Brief:` YAML, per its own `references/design-brief.md` contract) — both are Claude Code plugin skills (`microsoft/skills-for-fabric`, `powerbi-authoring` bundle), a different host than this Cursor skill library. This skill checks their output; it does not replace or re-implement them.
- Checks model structure against `semantic-model-authoring`'s `modeling-guidelines.md`, and PBIR mechanics against `powerbi-report-authoring`'s own validation loop having already run (`powerbi-report-author validate` clean is a prerequisite, not a substitute — see Known-Unsafe Build Patterns for what it doesn't catch).
- Checks metric definitions authored by `dashboard-metric-semantics` for internal consistency, but does not author them.
- PBIP/TMDL-specific, unlike `dashboard-frontend-implementation`'s generic web-component scope — the two don't overlap.
