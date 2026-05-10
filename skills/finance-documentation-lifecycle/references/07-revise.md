# Phase 7: Revise – Check & Act

**Goal**: Update when processes change, nonconformities emerge, or users identify gaps. Maintain version history and document reasons for change.

**ISO 9001 alignment**: Clause 8.5.6 (control of changes) and 10.3 (continual improvement). Revisions ensure documentation stays current and reflects actual process.

---

## Steps

### 1. Identify Need for Revision

**Triggers for revision**:

| Trigger | Example | Revision Type |
|---|---|---|
| **Process change** | System upgrade, new regulation, workflow redesign | Major (new version) |
| **User feedback** | Unclear step, missing example, confusing wording | Minor (clarification) |
| **Nonconformity/audit finding** | Procedure gap, missing approval, control weakness | Major (if affects control) |
| **Deviation pattern** | Same mistake by multiple users | Minor (clarification) |
| **System update** | Screenshots outdated, GL codes changed | Minor (data refresh) |
| **Scheduled review** | Annual review cycle; updating even if no issues | Minor or major (as needed) |
| **Corrective action** | Recurring documentation issue or control weakness | Major or process-level |

**Document the trigger**:
```
REVISION REQUEST LOG
─────────────────────────────────────────
Document:         GL Reconciliation SOP v2.0
Trigger Date:     2025-07-15
Trigger:          Process change (new variance escalation level per CFO directive)
Revision Type:    MAJOR
Requestor:        Jane Smith (Owner)
Priority:         HIGH (controls new CFO approval workflow)
Evidence Source:  Customer feedback log / audit finding / nonconformity log
Target Release:   September 1, 2025
─────────────────────────────────────────
```

---

### 2. Assess Scope and Priority

**Revision scope** (what's changing):

**Minor revisions** (clarification, data refresh):
- Language clarification (Step X is unclear)
- System screenshots updated
- GL codes or role titles refreshed
- Examples updated for realism
- Cross-references to related documents added/corrected
- Typically 1–2 weeks; document owner can do; may not need full re-review

**Major revisions** (process or control change):
- New or removed steps
- Changed roles or responsibilities
- New approval requirement or escalation path
- Changed frequency or variance limit
- Changed system or tool
- Typically 3–4 weeks; requires full review and re-approval

**Priority**:
- **HIGH**: Affects control design, audit finding, compliance, or user safety/compliance
- **MEDIUM**: Affects clarity or user efficiency; should be addressed in next cycle
- **LOW**: Nice-to-have improvement; address opportunistically

**Customer impact**:
- Who is affected: preparer, reviewer, approver, manager, auditor, analyst?
- What is the impact: error, delay, rework, audit finding, inconsistent execution, or loss of confidence?
- Is the issue isolated, or does it show a broader documentation lifecycle weakness?

---

### 3. Determine Whether Corrective Action Is Required

Open a corrective action when documentation issues are recurring, high-risk, audit-significant, or caused by a lifecycle weakness rather than a one-time drafting error.

**Corrective action workflow**:
1. **Define the problem**: State the recurring documentation issue and customer/control impact.
2. **Contain the issue**: Give temporary guidance, remove uncontrolled copies, or notify users of known gaps.
3. **Analyze root cause**: Determine whether the cause is ownership, review cadence, storage control, approval workflow, training, or weak customer feedback capture.
4. **Plan corrective action**: Assign owner, due date, evidence required, and effectiveness check.
5. **Implement and verify**: Update documentation or lifecycle controls; confirm the issue does not recur.
6. **Retain evidence**: Store problem statement, root cause, action plan, approval, implementation proof, and effectiveness check.

**Corrective action record**:
```
CORRECTIVE ACTION RECORD
─────────────────────────────────────────
Issue:              Repeated user confusion on variance escalation
Source:             Feedback log + two control review findings
Root Cause:         Procedure lacked decision table and examples
Containment:        Owner sent interim guidance to AR/AP leads
Corrective Action:  Add escalation decision table; update training notes
Owner / Due Date:   Jane Smith / 2025-08-15
Effectiveness Check: No repeat findings in next monthly control review
Evidence Location:  [Link/path]
─────────────────────────────────────────
```

---

### 4. Incorporate Changes

**For minor revisions**:
- Document owner updates directly
- Note change in changelog (date, what changed, why)
- Bump minor version (1.0 → 1.1)
- May only need document owner review before re-release

**For major revisions**:
- Document owner incorporates feedback and process changes
- Return to Phase 3 (Review) for full review cycle
- Bump major version (1.0 → 2.0)
- Complete approval process (Phase 4) before release
- Note all changes in changelog
- Link changes to feedback, nonconformity, audit finding, corrective action, or process change evidence where applicable

**Changelog example**:
```
VERSION HISTORY – GL Reconciliation SOP
─────────────────────────────────────────
v2.0 (2025-09-01)  MAJOR: Added CFO approval requirement for variances >$10,000
                   Updated variance tolerance thresholds per finance policy change
                   Owner: Jane Smith | Approved: CFO, 2025-08-30

v1.1 (2025-07-15)  MINOR: Clarified Step 5 wording; updated system screenshots
                   Owner: Jane Smith | Released: 2025-07-20

v1.0 (2024-05-01)  Initial version
                   Owner: Jane Smith | Approved: Finance Manager, 2024-05-01
─────────────────────────────────────────
```

---

### 5. Conduct Review (For Major Revisions)

**Return to Phase 3**:
- Technical accuracy review (process owner walks through with documentation)
- Completeness and clarity review (does it cover new/changed steps?)
- Control design review (if change affects control, does it now work properly?)
- Compliance review (does new version meet regulatory/standard requirements?)

**Document review findings**:
- No significant findings → recommend approval
- Minor findings → note for clarification in next version
- Critical findings → request rework

---

### 6. Obtain Re-Approval (For Major Revisions)

**Return to Phase 4**:
- Route revised document to approvers (same authority as original, or higher if scope changed)
- Document approval date, approver, any conditions
- Announce revision to finance team

**For minor revisions**:
- Document owner may release directly (if authority granted in original approval)
- Or notify manager: "Updated version 1.1 released; minor clarifications only"
- Update metadata header with release date

---

### 7. Track and Communicate Revision

**Manage version transition**:
- Archive prior version separately (marked "superseded")
- Update document storage location with new version
- Update master documentation registry (version number, effective date)
- Update any linked procedures that reference this document

**Communicate to finance team**:
- Email or team message announcing revision
- Highlight what changed and why
- Link to new version
- Note any new training needs (if significant change)
- Effective date (immediate or staggered?)

**Example**:
```
PROCEDURE UPDATED: GL Reconciliation SOP v2.0

Effective Date: September 1, 2025
Location: [Link]
Owner: Jane Smith (jane.smith@company.com)

CHANGES FROM v1.1:
- Added CFO approval requirement for variances exceeding $10,000
  (Previously escalated to Finance Manager)
- Updated variance tolerance thresholds:
  • GL variance ≤$1,000: Manager approval
  • GL variance $1,001–$10,000: Finance Manager approval
  • GL variance >$10,000: CFO approval

QUESTIONS? See Jane Smith.
```

---

## Revision Checklist

Before releasing a revised version, confirm:

- [ ] Revision trigger documented (process change, user feedback, nonconformity, etc.)
- [ ] Revision scope and priority assessed
- [ ] Customer impact assessed
- [ ] Corrective action opened for recurring, high-risk, or lifecycle-driven issues
- [ ] Changes incorporated and clearly marked
- [ ] Version number updated (1.0 → 1.1 or 2.0)
- [ ] Changelog updated (what changed, when, why, by whom)
- [ ] For major revisions: full review cycle completed
- [ ] For major revisions: formal re-approval obtained
- [ ] Prior version archived separately (marked "superseded")
- [ ] Master registry updated with new version
- [ ] Finance team notified of changes
- [ ] Linked documents updated with cross-reference (if applicable)
- [ ] Revision, exception, and corrective action evidence retained

---

## Common Pitfalls

| Pitfall | Why It Matters | How to Avoid |
|---|---|---|
| Changes made informally | Nobody knows version is updated; old version persists | Always bump version; update metadata; mark old version superseded |
| No changelog | Auditor can't trace what changed and why | Maintain detailed changelog; include date, author, reason for each change |
| Major change treated as minor | Skips review/approval; control gaps; audit exposure | Use trigger framework; major process changes require full review + re-approval |
| No communication | Users don't know procedure changed; old version still followed | Announce revision with email or team message; highlight key changes |
| Revision loses approval | New version approved by different authority; inconsistent governance | Use same approval chain unless scope requires additional authority |

---

## Output: Updated and Controlled Documentation

By the end of this phase, you should have:

1. **Revised document** with changes incorporated (for major) or clarified (for minor)
2. **Updated version number** (1.0 → 1.1 or 2.0)
3. **Detailed changelog** (what changed, when, why, by whom, and source evidence)
4. **Corrective action record** where recurring or high-risk issues were found
5. **For major revisions**: Completed Phase 3 review and Phase 4 approval
6. **Prior version archived** separately (marked "superseded")
7. **Finance team notification** of changes and effective date

---

**Next phase**: [08-retire.md](08-retire.md)
