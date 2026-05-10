# Phase 4: Approve – Check & Act

**Goal**: Obtain formal sign-off from authorized manager/owner. Document approval decision, date, and authority.

**ISO 9001 alignment**: Clause 7.5.2 requires review and approval before documented information is released. Approval confirms suitability and adequacy.

---

## Steps

### 1. Prepare Approval Packet

**What to submit for approval**:
- Final (revised) documentation
- Review findings summary (from Phase 3)
- Changes made in response to review feedback
- Metadata header (owner, version, effective date, audience)
- Quality acceptance criteria status (accurate, current, approved-ready, accessible, usable, protected, traceable, retained)
- Open nonconformities, exceptions, or deferred issues with risk and follow-up owner

**Approval form** (or email summary):
```
APPROVAL REQUEST
─────────────────────────────────────────
Document Title:           [Title]
Document Version:         [e.g., v1.0, v2.1]
Document Owner:           [Name, Role]
Prepared/Revised Date:    [Date]

PURPOSE:
[Why this document exists; what process it covers]

SCOPE OF CHANGES (if revision):
[New sections, policy/system changes, deletions]

REVIEW SUMMARY:
[Findings from Phase 3; actions taken to address them]

APPROVAL REQUESTED FROM:
[ ] Finance Manager (Name: __________)
[ ] Compliance/Audit Lead (Name: __________)
[ ] CFO (Name: __________) [if high-risk control]
[ ] Process Owner (Name: __________) [optional verification]

EFFECTIVE DATE (if approved):
[Date this version becomes official]

DOCUMENT OWNER CERTIFIES:
☐ Review feedback has been addressed or noted
☐ Technical accuracy verified
☐ Metadata is complete
☐ Related documents are linked
☐ Storage location and access control defined
☐ Evidence retention location defined
☐ Any exceptions or deferred issues are documented with risk and due date
─────────────────────────────────────────
```

---

### 2. Route to Appropriate Approvers

**Approval authority depends on risk level**:

| Risk Level | Approvers | Typical Timeline |
|---|---|---|
| **High-risk control** (audit critical, SOX, fraud risk) | Finance Manager + CFO + Compliance/Audit | 2 weeks |
| **Medium-risk procedure** (affects multiple users, compliance requirement) | Finance Manager + Document Owner | 1 week |
| **Low-risk reference** (informational, no control requirement) | Document Owner only | 2–3 days |

**Routing method**:
- Email approval form with document attached
- Or submit via document management system / approval workflow tool
- Provide deadline for response (e.g., "Please review by [date]")

---

### 3. Collect Sign-Off

**Each approver confirms**:
- ☐ Technical accuracy (if applicable to their role)
- ☐ Completeness and clarity
- ☐ Compliance with regulations/standards (if compliance role)
- ☐ Control design appropriate to risk (if audit role)
- ☐ Ready for finance team to use

**Sign-off formats**:
- Email approval with explicit statement: "I approve this document as-is" or "I approve with the following comments"
- Approval form signature (printed and scanned) or electronic signature
- Digital workflow system (Sharepoint approval, form submission tool)

**Record**:
- Approver name, title, date of approval
- Any conditional approvals ("approved pending revision of Step 5")
- Comments or rationale (optional but recommended for audit trail)
- Exception decisions, expiration dates, and required follow-up actions

---

### 4. Document Approval Decision

**Approval metadata** (add to document header):
```
APPROVAL RECORD
─────────────────────────────────────────
Approval Date:           [Date approved]
Approved By (Name):      [Approver name + title]
Approval Status:         [APPROVED]
Effective Date:          [When this version officially applies]
Conditional Approvals:   [If any; e.g., "approved pending revision of Step 5 by [date]"]
Comments:                [Optional; any notes from approver]
Next Review Date:        [When to formally review again; usually 1 year or per trigger]
─────────────────────────────────────────
```

---

### 5. Handle Conditional or Rejected Approvals

**Conditional approval** (e.g., "approved pending revision"):
- Document the condition
- Assign responsibility and deadline for addressing it
- Re-submit for approval once condition is met
- This counts as a new version revision
- Retain the approval condition and completion evidence with the document lifecycle record

**Rejected approval**:
- Document reason for rejection
- Return to document owner with specific feedback
- May require major rework (go back to Phase 2) or clarification (Phase 3)
- Resubmit after rework
- Log the rejection as a documentation nonconformity if the document was inaccurate, outdated, missing required content, unclear, uncontrolled, or not suitable for use

---

### 6. Announce Approval and Readiness

**Once approved**:
- Send message to finance team: "This procedure is now approved and in effect as of [date]"
- Indicate storage location and how to access
- Note any training requirements or transition date
- Provide contact for questions

**Example message**:
```
PROCEDURE APPROVED: GL Reconciliation SOP

The GL Reconciliation Standard Operating Procedure has been approved 
and is effective immediately [or: effective June 1, 2025].

Document Location: [Sharepoint link or Wiki page]
Document Owner: Jane Smith (jane.smith@company.com)
Version: 2.0 | Approved: [Date] | Next Review: [Date]

Key changes from prior version:
- Updated variance tolerance thresholds
- Added new approval workflow for variances >$10,000
- Clarified month-end close deadline

Contact Jane Smith with questions or feedback.
```

---

## Approval Checklist

Before releasing, confirm:

- [ ] Approval packet complete (document, review summary, changes log)
- [ ] Approvers identified based on risk level
- [ ] Approval form or routing submitted
- [ ] All required approvers have signed off
- [ ] Conditional approvals documented (if any) with remediation plan
- [ ] Exception decisions documented with risk, approver, expiration date, and follow-up
- [ ] Approval metadata updated in document header
- [ ] Effective date documented
- [ ] Finance team notified of approval and location
- [ ] Related documents updated with cross-reference (if applicable)
- [ ] Approval evidence retained in the agreed evidence location

---

## Common Pitfalls

| Pitfall | Why It Matters | How to Avoid |
|---|---|---|
| Unclear who approves | Approval stalls; multiple people think others are approving | Define approval authority by risk level upfront (Phase 1) |
| Conditional approval not tracked | Condition never addressed; document remains incomplete | Assign responsibility and deadline; re-review when condition met |
| Approval but no metadata update | Document says "draft" even after approval; users unsure if current | Update header with approval date, approver, effective date before release |
| No announcement | Users don't know document is approved; old version still circulates | Send team message with location, owner contact, key changes |
| Too many approvers | Approval timeline drags; process becomes bottleneck | Limit to 2–3 key approvers per risk level; avoid unnecessary layers |

---

## Output: Formal Approval Record

By the end of this phase, you should have:

1. **Signed-off approval packet** (document owner, finance manager, CFO, and/or compliance approvers)
2. **Approval metadata** in document header (date, approver, effective date, next review date)
3. **Approval decision record** (for audit trail; who approved, when, any conditions)
4. **Exception or rejection evidence** where applicable (risk, owner, due date, disposition)
5. **Team notification** (finance team informed of approval, location, contact)

---

**Next phase**: [05-publish-store.md](05-publish-store.md)
