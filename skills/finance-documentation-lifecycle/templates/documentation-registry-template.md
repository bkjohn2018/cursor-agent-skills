# Finance Documentation Registry Template

Use this registry to maintain a master list of all finance and accounting documentation. This helps:
- **Users find procedures** (searchable by title, type, or process)
- **Leadership track compliance** (see which docs are approved, which are stale)
- **Auditors verify documentation universe** (all procedures are documented, controlled, and current)

---

## Registry Structure

Copy this table into a Sharepoint list, Excel spreadsheet, or Wiki. Update quarterly or whenever a document is added, revised, retired, or receives material customer feedback or nonconformity findings.

```
FINANCE DOCUMENTATION REGISTRY
════════════════════════════════════════════════════════════════════════════════════════════════════════════

DOC ID | Document Title              | Version | Owner      | Type    | Status    | Copy Status | Effective | Next Review | Risk  | Storage Location
────────────────────────────────────────────────────────────────────────────────────────────────────────
AR-001 | GL Reconciliation SOP       | 2.0     | J. Smith   | SOP     | Approved  | Controlled  | 2025-09   | 2026-09     | HIGH  | [Link]
AR-002 | GL Chart of Accounts        | 1.1     | J. Smith   | Ref     | Approved  | Controlled  | 2024-12   | 2025-12     | MED   | [Link]
AP-001 | Invoice Processing SOP      | 1.0     | M. Johnson | SOP     | Approved  | Controlled  | 2025-03   | 2026-03     | HIGH  | [Link]
AP-002 | Vendor Master Procedures    | 2.1     | M. Johnson | Proc    | Approved  | Controlled  | 2025-08   | 2026-02     | MED   | [Link]
FIN-001| Monthly Close Checklist     | 1.4     | J. Lee     | Check   | Approved  | Controlled  | 2025-07   | 2025-12     | HIGH  | [Link]
HR-001 | Payroll Control Procedures  | 1.0     | S. Brown   | Proc    | Draft     | Controlled  | —         | —           | HIGH  | [Link]
────────────────────────────────────────────────────────────────────────────────────────────────────────

LEGEND:
Document Type: SOP = Standard Operating Procedure | Proc = Process Narrative | Ref = Reference | Check = Checklist | Guide = Reporting Guide | Data = Data Definition
Status: Draft = Not approved | Approved = In effect | Superseded = Replaced by newer version | Retired = Discontinued
Copy Status: Controlled = authoritative current/approved version | Uncontrolled = reference copy only | Archive = retained historical version
Risk Level: HIGH = Control critical to financial reporting | MED = Compliance or efficiency | LOW = Informational
────────────────────────────────────────────────────────────────────────────────────────────────────────
```

---

## Column Definitions

| Column | Purpose | Example |
|---|---|---|
| **DOC ID** | Unique identifier for easy reference | AR-001, AP-002, FIN-001 |
| **Document Title** | Clear, searchable title | GL Reconciliation SOP (not "Procedure 1") |
| **Version** | Major.minor version number | 1.0, 1.1, 2.0 |
| **Owner** | Who maintains and updates the document | Jane Smith, John Lee |
| **Type** | Category for grouping | SOP, Process, Checklist, Guide, Data Definition |
| **Status** | Is it current, draft, or retired? | Approved, Draft, Superseded, Retired |
| **Copy Status** | Whether the listed link is controlled, uncontrolled, or archive | Controlled, Uncontrolled, Archive |
| **Effective Date** | When this version became official (YYYY-MM) | 2025-09, 2025-08 |
| **Next Review Date** | When to formally review again (YYYY-MM) | 2026-09 (1 year), 2025-12 |
| **Risk Level** | How critical is this to controls and compliance? | HIGH, MEDIUM, LOW |
| **Storage Location** | Link or path to authoritative copy | [Sharepoint link], [Wiki page] |

Recommended optional columns:

| Column | Purpose | Example |
|---|---|---|
| **Feedback Channel** | Where finance/accounting users report issues | SOP feedback form, ticket queue |
| **Last Feedback Review** | Last date customer feedback was reviewed | 2025-09-30 |
| **Open Nonconformities** | Count or link to documentation nonconformities | 2 open, [NC log] |
| **Corrective Action** | Link to CAPA/corrective action record if recurring issue exists | CA-2025-014 |
| **Evidence Location** | Link to review, approval, revision, retirement, exception evidence | [Evidence folder] |

---

## How to Use This Registry

### 1. Add New Document
- When a new procedure is approved, add a row
- Complete all columns; set Status = "Approved"
- Set Next Review = 1 year from effective date (or per review trigger)

### 2. Update Existing Document
- When revising a procedure, update Version number
- Update Effective Date to revision date
- Update Next Review date
- Update Status if changed (e.g., Draft → Approved)
- Link revision evidence, customer feedback, nonconformity, or corrective action record when relevant

### 3. Retire Document
- When discontinuing a procedure, keep the row but change Status = "Retired"
- Note retirement date in comments (optional "Comments" column)
- Archive the document in a separate folder; update Storage Location or add comment "(Archived)"
- Change Copy Status to "Archive" and record retirement evidence location

### 4. Monitor Review Dates
- Monthly: Check which documents are due for review (Next Review date approaching)
- Quarterly: Review overall registry; ensure no approved docs are stale (>2 years without review)
- Annually: Comprehensive governance review (all docs have owner, approval, review schedule)
- Quarterly: Review customer feedback and nonconformity trends for recurring documentation issues

### 5. Share and Communicate
- Finance team bookmark this registry for easy procedure lookup
- Leadership uses it for compliance/governance reporting
- Auditors use it to verify documentation universe is controlled and current
- Document owners use it to verify open feedback, nonconformities, corrective actions, and exceptions are not aging without response

---

## Sample Completed Registry (Finance Department)

```
FINANCE DOCUMENTATION REGISTRY – Q3 2025
════════════════════════════════════════════════════════════════════════════════════════════════════════════

DOC ID | Document Title                    | Vers | Owner        | Type    | Status       | Copy Status | Effective | Next Review | Risk  | Comments
────────────────────────────────────────────────────────────────────────────────────────────────────────
AR-001 | GL Reconciliation SOP             | 2.0  | Jane Smith   | SOP     | Approved     | Controlled  | 2025-09   | 2026-09     | HIGH  | Revised for new variance limits
AR-002 | GL Chart of Accounts              | 1.1  | Jane Smith   | Ref     | Approved     | Controlled  | 2024-12   | 2025-12     | MED   | Data refresh annually
AR-003 | Revenue Recognition Guide         | 1.0  | Jane Smith   | Guide   | Approved     | Controlled  | 2025-04   | 2026-04     | HIGH  | New for ASC 606 transition
AP-001 | Invoice Processing SOP            | 1.0  | Mike Johnson | SOP     | Approved     | Controlled  | 2025-03   | 2026-03     | HIGH  | 
AP-002 | Vendor Master Management          | 2.1  | Mike Johnson | Proc    | Approved     | Controlled  | 2025-08   | 2026-02     | MED   | Updated for new vendor portal
AP-003 | Expense Approval Matrix           | 1.0  | Mike Johnson | Ref     | Draft        | Controlled  | —         | —           | MED   | Pending Finance Manager approval
FIN-001| Monthly Close Checklist           | 1.4  | John Lee     | Check   | Approved     | Controlled  | 2025-07   | 2025-12     | HIGH  | Updated close calendar; due for Q4 review
FIN-002| Variance Analysis & Reporting     | 2.0  | John Lee     | Guide   | Approved     | Controlled  | 2025-01   | 2026-01     | MED   | 
HR-001 | Payroll Control Procedures        | 1.0  | Sarah Brown  | Proc    | Draft        | Controlled  | —         | —           | HIGH  | Under review; pending Audit approval
BANK-001| Bank Reconciliation SOP          | 1.2  | Emma Davis   | SOP     | Superseded   | Archive     | 2025-08   | —           | HIGH  | Superseded by BANK-002 (2025-09)
BANK-002| Bank Reconciliation SOP          | 2.0  | Emma Davis   | SOP     | Approved     | Controlled  | 2025-09   | 2026-09     | HIGH  | New system upload feature
────────────────────────────────────────────────────────────────────────────────────────────────────────

GOVERNANCE SUMMARY (as of July 2025):
- Total Procedures: 12 (10 Approved, 2 Draft, 0 Retired)
- Due for Review (Q4 2025): FIN-001, AR-002
- Draft (Pending Approval): AP-003 (awaiting Finance Manager), HR-001 (awaiting Audit)
- Overdue for Review: None
- Stale Documentation (>2 years): None
- Action Items: 
  ☐ Approve AP-003 and HR-001
  ☐ Schedule Q4 reviews for AR-002, FIN-001
  ☐ Archive BANK-002 v1.2 (mark superseded)
────────────────────────────────────────────────────────────────────────────────────────────────────────
```

---

## Tips for Maintaining Your Registry

1. **Keep one source of truth**: Choose one location (Sharepoint, Excel, Wiki) and update it consistently; don't maintain multiple copies.

2. **Link to documents**: Make Storage Location column clickable links so users can instantly access procedures.

3. **Color-code status**: Use conditional formatting to highlight:
   - **Green** = Approved and current
   - **Yellow** = Draft or due for review
   - **Red** = Stale (not reviewed in 2+ years)

4. **Sort by risk level**: Help users prioritize; high-risk controls need more frequent review and tighter governance.

5. **Use for onboarding**: New finance team members bookmark this registry to quickly find all procedures for their role.

6. **Share governance summary**: Quarterly report to Finance leadership:
   - How many procedures are approved and current?
   - Any overdue reviews?
   - Any drafts pending approval?
   - Any recurring customer feedback themes?
   - Any open nonconformities or corrective actions?
   - This demonstrates governance maturity to auditors.

7. **Retire thoughtfully**: When retiring, keep the row in registry marked "Retired" with archive date; don't delete. Auditors need historical record.

---

## Excel Formula Tips (If Using Spreadsheet)

```
Review Due Soon: =IF(AND([Status]="Approved", TODAY()>EDATE([Next Review Date],-1)), "YES", "")
  → Highlights when review is due within 30 days

Overdue: =IF(AND([Status]="Approved", TODAY()>[Next Review Date]), "OVERDUE", "")
  → Highlights if review date has passed

Color by Status: Use conditional formatting
  Approved + TODAY() <= [Next Review] = Green
  Draft = Yellow
  TODAY() > [Next Review] = Red
  Retired = Gray
```

---

**Maintain this registry as a living document. It's your governance dashboard.**
