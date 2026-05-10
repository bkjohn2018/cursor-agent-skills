# Phase 2: Structure – Plan & Create

**Goal**: Organize content so users can find and understand it. Establish metadata standards and format.

**ISO 9001 alignment**: Clause 7.5.2 (creating and updating) requires proper identification, description, format, and media. Structure determines whether documentation is used or ignored.

---

## Steps

### 1. Choose Structure and Format

**Format decision**:
- **SOP/Process narrative**: Numbered steps, decision trees, flow diagrams, appendices
- **Control documentation**: Objective, frequency, evidence, variance limits, escalation
- **Data definition**: Table (field name, description, source system, calculation, owner, update frequency)
- **Reporting guide**: Steps, screenshots, data source, acceptance criteria, approval level, deadline
- **Reconciliation procedure**: Account description, normal balance, typical variance, reconciliation steps, variance tolerance, approval authority

**Medium**:
- Digital (best for version control, discoverability, accessibility)
- Printed (if required for regulated procedures or for offline teams)
- Hybrid (digital master, printed for training/offline reference)

**Access and discoverability**:
- Is this published on a shared Wiki, Sharepoint, internal website?
- Will users search for it by keyword?
- Is it linked from a process map or procedure index?
- Is it emailed to users or self-service?

---

### 2. Create Metadata Header

Every finance document should open with a metadata block so users immediately know:

```
METADATA
─────────────────────────────────────────
Document Title:              [Exact title]
Document ID/Version:         [e.g., AR-001, v2.1]
Effective Date:              [Date this version applies]
Owner (Role + Name):         [AR Manager, Jane Smith; jane.smith@company.com]
Last Updated:                [Date last revised]
Next Review Date:            [When to formally review again]
Approved By:                 [Approver name + title + date]
Approval Status:             [Draft | Approved | Superseded | Retired]
Audience:                    [Finance team, audit team, AR staff, CFO]
Process/System References:   [Related SOPs, systems, accounts, reports]
─────────────────────────────────────────
```

**Why metadata matters**:
- Users instantly know if this is current, approved, and who to contact
- Auditors can verify approval and ownership
- You can track versions and retirement dates
- Search systems can index it

---

### 3. Write or Organize Content

**For SOPs and procedures**:
- **Context section**: Why this procedure exists, when to use it, what outcome is expected
- **Roles and responsibilities**: Who does what
- **Detailed steps**: Numbered, sequential, including decision points
- **Examples**: Real or realistic scenarios (use anonymized data)
- **Appendices**: Forms, templates, lists, system screenshots, escalation contacts
- **Related documentation**: Cross-references to linked procedures or policies

**For control documentation**:
- **Control objective**: What risk does this control mitigate?
- **Frequency**: How often does the control operate?
- **Performer**: Who executes the control?
- **Procedure**: Step-by-step how the control is executed
- **Evidence**: What artifacts prove the control operated? (reports, approvals, logs)
- **Variance limits**: What deviations trigger escalation?
- **Escalation path**: Who approves variances?

**For data definitions**:
- **Field/dataset name**
- **Description** (business meaning, not technical jargon)
- **Source system** (where the data originates)
- **Calculation formula** (if derived)
- **Owner** (who maintains this data?)
- **Update frequency** (daily, monthly, on-demand)
- **Retention** (how long to keep)
- **Sensitivity/access** (confidential, public, role-restricted)

**For reporting guides**:
- **Report name and purpose**
- **Data source and refresh schedule**
- **Key metrics and definitions**
- **How to interpret results**
- **Who prepares, reviews, approves**
- **Deadline for delivery**
- **Known limitations or data quality issues**
- **Who to contact with questions**

---

### 4. Apply Accessibility and Clarity Standards

**Clarity**:
- **Headings and subheadings**: Organize by task/decision, not by ISO clause or system
- **Plain language**: Avoid jargon or define it in a glossary
- **Active voice**: "You record the entry in the ledger" not "The entry is recorded"
- **Consistent terminology**: Use the same term throughout (don't switch between "vendor" and "supplier")
- **White space**: Paragraph breaks, bullets, tables—make it scannable

**Accessibility**:
- Use sufficient contrast (dark text on light background)
- Include alt text for diagrams and screenshots
- Use readable fonts (sans-serif, 11–12 pt minimum)
- Avoid walls of text; use tables, lists, numbered steps
- Test readability with non-expert user (someone from finance team, not the author)

---

### 5. Build in Version Control

**Header version scheme**:
- **Major.Minor** (e.g., 1.0, 1.1, 2.0)
- Or **v[date]** (e.g., v2025-05-02) if tracking by revision date
- Or **[name]_v[number]** (e.g., AR-001_v1.2)

**Changelog** (append to document or keep in metadata):
```
VERSION HISTORY
─────────────────────────────────────────
v1.0 (2024-01-15)  Initial version. Owner: Jane Smith
v1.1 (2024-05-10)  Clarified variance limit, added escalation path. Owner: Jane Smith
v2.0 (2025-01-20)  Major revision: system upgrade, new approval workflow. Approved by: CFO
─────────────────────────────────────────
```

---

### 6. Identify and Link Related Documentation

**Document the relationship**:
- **Precondition**: What must happen before this procedure (e.g., "see GL Chart of Accounts SOP")
- **Related SOPs**: Cross-reference similar procedures
- **System references**: If documented procedure depends on system screenshots/data, note system name, version
- **Compliance references**: Link to regulation, standard, policy that drives this documentation
- **Appendices or external docs**: Form templates, reference data, external guidance

---

## Content Quality Checklist

Before moving to review, confirm:

- [ ] Metadata header complete (owner, version, approval status, audience, effective date)
- [ ] Purpose and scope clear in opening
- [ ] Organized for user task (not ISO structure)
- [ ] All steps numbered, sequential, or clearly branched
- [ ] Roles and responsibilities named
- [ ] Examples provided (real or realistic)
- [ ] Appendices or templates included
- [ ] Plain language (no jargon, or jargon defined)
- [ ] Accessible format (headings, white space, readable font, sufficient contrast)
- [ ] Related documents linked or referenced
- [ ] Version and change history recorded
- [ ] No confidential data in examples; anonymized if needed
- [ ] Diagrams/screenshots have alt text

---

## Common Pitfalls

| Pitfall | Why It Matters | How to Avoid |
|---|---|---|
| Mirroring ISO structure | ISO says not to do this; users confused when structure doesn't match their process | Organize by user task, decision point, or role—not by ISO clause |
| Too technical or too basic | Users skip over documentation that doesn't match their level | Ask a representative user to read draft; time how long it takes to find key info |
| Missing metadata | Users unsure if version is current, who owns it, when to review | Use metadata template; make it the first thing on every document |
| No version control | Multiple versions circulate; nobody knows which is current | Number versions; keep changelog; store only authoritative version in shared location |
| Orphaned documentation | Related documents exist but aren't linked; users discover them by accident | Map all finance procedures; add "related documents" section to each |
| Confidential data in examples | Privacy breach; audit finding; compliance violation | Use anonymized, realistic examples or remove sensitive numbers |

---

## Output: Structured Documentation

By the end of this phase, you should have:

1. **Drafted content** organized for your audience (SOP, control doc, data definition, etc.)
2. **Metadata header** with owner, version, status, approval path
3. **Clear structure** (headings, numbered steps, decision trees)
4. **Accessibility standards** applied (contrast, white space, plain language)
5. **Related documents** linked or listed
6. **Version control** in place (version number, changelog)

---

**Next phase**: [03-review.md](03-review.md)
