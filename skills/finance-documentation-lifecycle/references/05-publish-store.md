# Phase 5: Publish/Store – Do

**Goal**: Place documentation in its authoritative location. Ensure access control, discoverability, and protection from unintended alteration.

**ISO 9001 alignment**: Clause 7.5.3 requires documented information to be "available and suitable for use" and "adequately protected" from loss of confidentiality, improper use, or loss of integrity.

---

## Steps

### 1. Confirm Storage Location and Access

**Select authoritative storage**:
- **Sharepoint/Teams**: Centralized, versioned, role-based access control
- **Wiki (internal or GitHub)**: Searchable, linked, easy to update
- **Document management system**: Heavy control; suitable for high-risk docs
- **Intranet or internal knowledge base**: Discoverable, but may require more manual updates

**Access control**:
- **View access**: Who can read? (all finance staff, specific roles, select individuals)
- **Edit access**: Who can modify? (document owner only, owner + manager, broader review group)
- **Delete/archive access**: Who can retire or remove? (owner + CFO only)
- **Share access**: Can users download, print, email it? (usually yes, but track distribution for sensitive docs)

**Document location clearly**:
- Final document stored at a **permanent, clear URL** or path
- Old/superseded versions archived in a secondary location (not deleted, but marked "superseded")
- No duplicate versions floating in email, shared drives, or personal folders

---

### 2. Create Document Index or Registry

**Maintain a master list** of all finance documentation:

```
FINANCE DOCUMENTATION REGISTRY
─────────────────────────────────────────
Document Title         | Version | Owner       | Effective | Next Review | Status    | Storage Location
GL Reconciliation SOP  | 2.0     | Jane Smith  | 2025-05   | 2026-05    | Approved  | [Link]
Close Checklist        | 1.1     | John Lee    | 2024-12   | 2025-12    | Approved  | [Link]
Vendor Master Data...  | 3.0     | Sarah Jones | 2025-01   | 2025-06    | Approved  | [Link]
─────────────────────────────────────────
```

**Benefits**:
- Users know where to find procedures (instead of searching)
- Finance leadership can monitor version status
- You can track review due dates
- Auditors can verify documentation universe exists and is current

**Update frequency**: When a new document is approved or an existing one is revised.

---

### 3. Establish Version Control and Archive

**Current version**:
- Stored with clear filename (e.g., "GL_Reconciliation_SOP_v2.0.docx")
- Metadata header marks it as "APPROVED"
- URL/path is stable (doesn't change with new versions)

**Prior versions** (archive):
- Stored separately with version and supersession date (e.g., "GL_Reconciliation_SOP_v1.1_Superseded_2025-05.docx")
- Mark as "SUPERSEDED" in metadata
- Keep accessible for audit trail and historical reference
- Retain per retention policy (typically 3–7 years)

**Never allow**:
- Multiple "current" versions
- "Final_Final_FINAL_v3" naming conventions
- Undefined older versions in main storage

---

### 4. Control Official and Uncontrolled Copies

**Controlled copy**:
- The authoritative version stored in the approved location.
- Marked with document ID, version, approval status, effective date, owner, and storage location.
- Protected by access control, version history, and approval workflow where available.
- The only version valid for official finance/accounting use.

**Uncontrolled copy**:
- Any printed copy, emailed attachment, local download, exported PDF, or personal-drive copy outside the authoritative location.
- Mark as "UNCONTROLLED COPY - FOR REFERENCE ONLY" with the print/download date when distribution is necessary.
- Direct users back to the controlled copy before performing work.
- Avoid using uncontrolled copies for control execution unless an exception is approved and retained.

**Evidence to retain**:
- Access control record.
- Publication notice.
- Version archive record.
- Any approved exception allowing temporary use of an uncontrolled copy.

---

### 5. Add Document to Indexes and Cross-References

**Make it discoverable**:
- Add to **finance procedures index** or wiki table of contents
- Link from **process map** or flow diagram (if this SOP is part of a larger process)
- Add to **role-based guides** (if this procedure applies to AR team, add to "AR Procedures" section)
- Include in **onboarding checklist** (if new hires need to read this)
- Reference in **related documents** section of linked procedures

**Search and metadata**:
- Title is clear and searchable (not "Finance_Procedure_001")
- Keywords in metadata (e.g., "reconciliation, GL, month-end, 9000 account")
- If stored in wiki or knowledge base, add tags (e.g., #reconciliation #close #control)

---

### 6. Configure Access Control

**Role-based access** (example):
- **View access**: All finance staff, external audit, internal audit
- **Edit access**: Document owner, finance manager
- **Delete/archive access**: CFO, document owner
- **Sensitive docs** (e.g., fraud investigation SOP): Restrict to CFO, audit, compliance only

**Implement in storage system**:
- Sharepoint: Use group permissions (e.g., "Finance Readers" can view, "Finance Procedure Owners" can edit)
- Wiki: Use page-level access settings or folder permissions
- Document management: Configure role-based access in system

**Document access rules**:
```
ACCESS CONTROL RECORD
─────────────────────────────────────────
Document Title:     GL Reconciliation SOP
Storage Location:   [Sharepoint link]

View Access:        All Finance staff (Finance_Users group)
                    Internal Audit (Audit group)
                    External Audit (Ad hoc, request via Finance Manager)

Edit Access:        Document Owner (Jane Smith)
                    Finance Manager (John Lee)

Delete/Archive:     CFO (Sarah Brown)

Last Updated:       2025-05-02
Reviewed By:        Finance Manager
─────────────────────────────────────────
```

---

### 7. Protect from Unintended Alteration

**Technical controls**:
- **Read-only for viewers** (if your system supports it): Users can read and download, but cannot edit
- **Version control enabled**: System tracks who made what changes and when
- **Approval workflow** (if available): Changes require approval before release
- **Backup and recovery**: System backs up documents; old versions retrievable if accidentally deleted

**Procedural controls**:
- Only document owner and manager can edit
- Changes documented with date and reason (in version history or changelog)
- Major changes trigger review and re-approval before release
- Minor clarifications noted in changelog but may not require full re-approval

---

## Publishing Checklist

Before releasing, confirm:

- [ ] Document storage location finalized (Sharepoint, Wiki, etc.)
- [ ] Metadata header complete and accurate
- [ ] Access control configured (view, edit, delete permissions)
- [ ] Version number and effective date in document and filename
- [ ] Prior version archived separately
- [ ] Controlled copy marked and authoritative location identified
- [ ] Uncontrolled copy handling defined, if printed/downloaded copies are used
- [ ] Document added to master registry or index
- [ ] Cross-references added to related procedures
- [ ] Onboarding/role-based guides updated
- [ ] Finance team notified of location and how to access
- [ ] Backup/recovery process in place (if not automatic in your system)
- [ ] Read-only or approval workflow protection configured (if available)
- [ ] Publication, access, archive, and exception evidence retained

---

## Common Pitfalls

| Pitfall | Why It Matters | How to Avoid |
|---|---|---|
| No permanent storage location | Versions proliferate; old versions circulate | Choose one location; make URL/path stable; retire old versions to archive |
| Document not indexed/findable | Users can't find it; old version persists; uncontrolled versions emerge | Add to master registry; link from process map; include in search metadata |
| Multiple "current" versions | Confusion about which is authoritative; users follow outdated procedures | Name clearly; mark superseded; keep only latest version in main location |
| No access control | Sensitive data exposed; procedures modified without approval; audit trail lost | Define view/edit permissions; use system access controls; limit edit to owner + manager |
| Archive too aggressive | Users can't find old procedures; audit trail incomplete; history lost | Archive prior versions separately; mark "superseded"; retain per policy (3–7 years) |
| Users don't know where to find it | Documentation exists but isn't used | Announce location; add to index; send link in team message; include in onboarding |

---

## Output: Published and Protected Documentation

By the end of this phase, you should have:

1. **Document in permanent, authoritative storage location** (with stable URL/path)
2. **Access control configured** (view, edit, delete permissions defined)
3. **Version control and archive in place** (prior versions archived separately)
4. **Controlled/uncontrolled copy rules defined** (official copy marked; uncontrolled copies labeled and limited)
5. **Document indexed or registered** (added to master list, linked from related procedures)
6. **Finance team notification sent** (location, contact, how to access)

---

**Next phase**: [06-use.md](06-use.md)
