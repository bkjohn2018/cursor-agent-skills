# Phase 3: Review – Check

**Goal**: Verify accuracy, completeness, clarity, and compliance *before* approval. Identify gaps and nonconformities early.

**ISO 9001 alignment**: Clause 7.5.2 requires review and approval "for suitability and adequacy" before release. Early review prevents misuse and rework.

---

## Steps

### 1. Technical Accuracy Review

**Who**: Subject matter expert, process owner, or system administrator

**Check**:
- Do procedures match how the process actually works today?
- Are system screenshots current (screens change after upgrades)?
- Are calculations correct? (formulas, thresholds, tolerances)
- Are role names and titles current?
- Are account numbers, GL codes, reporting line names correct?
- Have recent policy or regulatory changes been incorporated?
- Are references to external documents (SOX requirements, audit standards) accurate?

**How to identify gaps**:
- Walk through the documented procedure step-by-step; does it match reality?
- Have the process owner execute the procedure using only the documentation—do they get stuck?
- Ask: "If someone new joined the team and read only this document, could they do this task?"

**Document findings**:
- List accuracy issues, missing steps, outdated references
- Note severity: critical (process breaks), major (user confused), minor (clarification needed)
- Log as nonconformity if gaps could cause errors or control weaknesses (e.g., "Missing approval step in high-risk control")

---

### 2. Completeness and Clarity Review

**Who**: Finance manager, process owner, target user (new hire or auditor)

**Check**:
- Are all required steps included?
- Are decision points clear? (if X, do Y; if not X, do Z)
- Are roles and responsibilities explicit?
- Are examples provided for complex procedures?
- Is the language plain? (can a non-expert understand it?)
- Are appendices and templates complete?
- Are assumptions stated? (e.g., "assumes daily bank feed is available")
- Are escalation paths clear? (what happens if variance exceeds limit?)

**How to identify gaps**:
- Ask first-time users: "What would you do if [edge case happens]?"
- Trace a procedure from start to finish—are there unexplained transitions?
- Compare the documented procedure to the actual process flow—does it match?

**Document findings**:
- Note missing steps, unclear language, incomplete examples
- Severity: critical (procedure cannot be executed), major (user likely confused), minor (could be clearer)

---

### 3. Control Design and Compliance Review

**Who**: Compliance/audit team, internal control specialist, CFO

**Check**:
- Does this procedure mitigate the intended risk?
- Is the control frequency appropriate for the risk level?
- Is the control performer independent (segregation of duties)?
- Is there sufficient evidence (audit trail, approvals, logs) that the control operated?
- Does the procedure meet regulatory or standard requirements?
- Are variances escalated appropriately?
- Is there a clear nonconformity reporting process?

**How to identify gaps**:
- Compare the procedure to the control design matrix or risk register
- Ask audit: "Does this procedure provide sufficient evidence?"
- Check compliance checklist: COSO, SOX, AICPA, industry standards

**Document findings**:
- Note control gaps, segregation of duties issues, audit trail weaknesses
- Severity: critical (control ineffective), major (audit exposure), minor (advisory improvement)

---

### 4. Compile Review Findings

**Review summary**:
- List all findings by category (accuracy, completeness, clarity, control, compliance)
- Assign severity (critical, major, minor)
- Identify who needs to take action (document owner, process owner, manager)
- Identify whether any finding is a documentation nonconformity: inaccurate, outdated, missing, unclear, inaccessible, uncontrolled, unapproved, or not followed
- Record whether immediate containment, revision, exception approval, or corrective action is required

**Example**:
```
REVIEW FINDINGS
─────────────────────────────────────────
ACCURACY
- Step 3: System screenshot outdated (prior to Jan 2025 system upgrade). CRITICAL.
- Step 7: GL code changed from 5100 to 5110 per 2024 COA update. CRITICAL.

CLARITY
- Step 5 unclear: "Reconcile variance" but doesn't say how or what tolerance. MAJOR.
- No example provided for edge case (when two vendors have same invoice number). MAJOR.

CONTROL DESIGN
- Manager approval missing for variances >$5,000. CRITICAL.

COMPLIANCE
- No reference to SOX requirement for monthly close sign-off. MAJOR.
─────────────────────────────────────────
```

---

### 5. Apply Documentation Quality Acceptance Criteria

Before recommending approval, confirm the document is:

- **Accurate**: Matches the current finance/accounting process, systems, roles, and requirements
- **Current**: Uses the latest approved process, policy, screenshots, data definitions, thresholds, and references
- **Approved-ready**: Review findings are resolved or documented as accepted exceptions
- **Accessible**: Intended users can find and retrieve it where and when needed
- **Usable**: Finance/accounting users can perform the task or make the decision without avoidable confusion
- **Protected**: The controlled copy is protected from unauthorized change and uncontrolled copies are identified
- **Traceable**: Metadata, ownership, version history, change rationale, and review evidence are complete
- **Retained**: Required review evidence and exception decisions are stored according to policy

If any acceptance criterion fails, do not recommend release unless an authorized exception decision is documented with risk, approver, expiration date, and follow-up action.

---

### 6. Schedule Review Meeting (For High-Risk or Complex Documentation)

**Attendees**:
- Document owner
- Process owner
- Finance manager
- Compliance/audit rep (if high-risk)
- Key users (1–2 people who execute the procedure daily)

**Agenda**:
- Walk through findings (accuracy, completeness, clarity, control, compliance)
- Discuss severity and priority for fixes
- Assign responsibility and timeline for remediation
- Decide: approve as-is, approve with notes, request revisions, reject for major rework

**Document outcomes**:
- Meeting minutes (who attended, what was discussed, decisions made)
- Revised task list (what needs fixing, owner, timeline)

---

### 7. Request Revisions or Approve with Feedback

**Revisions needed** (critical and major findings):
- Return to document owner with specific feedback
- Provide timeline for revision (usually 1–2 weeks)
- Document what feedback was given and why
- Log documentation nonconformities and link them to revision actions

**Minor feedback**:
- Can often be noted and addressed in next review cycle
- Or approve with annotated feedback for owner to incorporate
- Retain the decision rationale when minor issues are deferred

---

## Review Checklist

Before approving, confirm:

**Accuracy**:
- [ ] Procedure matches current process (verified with owner)
- [ ] System names, screenshots, screenshots current
- [ ] Account numbers, GL codes, role titles current
- [ ] Regulations, policies, audit standards referenced accurately

**Completeness**:
- [ ] All required steps included
- [ ] Decision points clear (if/then branches)
- [ ] Roles and responsibilities named
- [ ] Examples provided for complex tasks
- [ ] Edge cases addressed
- [ ] Appendices and templates complete

**Clarity**:
- [ ] Plain language (no unexplained jargon)
- [ ] Readable format (headings, white space, numbered steps)
- [ ] Assumptions stated
- [ ] Cross-references to related documents

**Control and Compliance**:
- [ ] Control design sound (objective, frequency, evidence, segregation of duties)
- [ ] Regulatory/standard requirements met
- [ ] Variance escalation process clear
- [ ] Nonconformity reporting process defined

**Metadata**:
- [ ] Owner identified
- [ ] Version and date recorded
- [ ] Approval chain defined
- [ ] Review cadence set

**Acceptance and Evidence**:
- [ ] Quality acceptance criteria met or exception documented
- [ ] Review evidence retained (findings, reviewers, dates, decisions)
- [ ] Nonconformities logged with owner and action
- [ ] Finance/accounting user feedback considered

---

## Common Pitfalls

| Pitfall | Why It Matters | How to Avoid |
|---|---|---|
| Skipping technical review | Procedure doesn't match reality; users frustrated; control fails | Have process owner walk through with documentation only |
| No compliance review | Audit finds gaps; control fails SOX or other requirement | Engage compliance/audit early; use control matrix as checklist |
| Unclear findings | Owner doesn't know what to fix; documentation fails to improve | Use specific examples; link findings to user impact or control risk |
| No review meeting (small docs) | Owner unsure about priority; misses key feedback; document still wrong | Document summary of findings in writing; prioritize critical + major items |
| User not in review | Approved document still confuses users; not used as intended | Include 1–2 actual users in review; ask them to try the procedure |

---

## Output: Review Findings and Recommendations

By the end of this phase, you should have:

1. **Technical accuracy checklist** completed (system screens, codes, role names verified)
2. **Completeness and clarity assessment** (all steps present, language clear, examples provided)
3. **Control design review** completed (risk mitigation, independence, evidence, variance escalation)
4. **Compliance checklist** completed (regulations, standards, audit requirements)
5. **Prioritized findings list** (critical, major, minor; assigned to owner)
6. **Quality acceptance decision** (meets criteria, requires revision, or exception approved)
7. **Recommendation**: Approve, approve with feedback, request revisions, or reject

---

**Next phase**: [04-approve.md](04-approve.md)
