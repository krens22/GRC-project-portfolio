## Section 4: Risk Register and Remediation

### 4.1 Rating Method

Each finding is rated on two factors. **Likelihood** is how probable it is that the weakness leads to a harmful event, or, where the weakness is already a compliance gap, whether the gap is occurring now. **Impact** is how serious the consequences would be for Brightwell and for the individuals whose data is involved, including regulatory penalties, operational disruption, and harm to customers or staff. Each factor is scored Low (1), Medium (2), or High (3), and the two scores are multiplied.

| Score | Rating |
|---|---|
| 1 to 2 | Low |
| 3 to 4 | Medium |
| 6 | High |
| 9 | Critical |

A vendor's overall risk rating is the rating of its highest open finding, consistent with the principle in Section 1.4 that the highest-risk answer decides.

### 4.2 Risk Register

| ID | Vendor | Finding | L | I | Rating | Required action |
|---|---|---|---|---|---|---|
| F-04 | PeopleMetrics | EU employee data stored in the US without SCCs | 3 | 3 | **Critical** | Execute Standard Contractual Clauses and complete a transfer assessment within 30 days. Until signed, no new EU employee data is sent. |
| F-01 | CloudNimbus | Breach notification up to 7 days | 2 | 3 | **High** | Amend contract to require notice within 48 hours of the vendor becoming aware. 60 days. |
| F-05 | PeopleMetrics | Automated scores used with no human review | 2 | 3 | **High** | Require manager review before any score informs a promotion or pay decision, and request an override feature from the vendor. 60 days. |
| F-07 | PeopleMetrics | Breach notification up to 5 business days | 2 | 3 | **High** | Amend contract to require notice within 48 hours. 60 days. |
| F-09 | MailBloom | MFA not required for administrator accounts | 2 | 3 | **High** | Brightwell enables MFA on its own admin accounts immediately. Vendor to enforce MFA by default within 60 days, or the issue is escalated. |
| F-11 | Brightwell (internal) | Employee privacy notice does not mention PeopleMetrics, automated scoring, or the US transfer | 3 | 2 | **High** | Update the notice and inform employees and their representatives before scores are used in further decisions. 60 days. |
| F-02 | CloudNimbus | No customer-managed encryption keys | 1 | 3 | Medium | Request a roadmap for customer-managed keys. 90 days. |
| F-06 | PeopleMetrics | No defined data retention period | 2 | 2 | Medium | Set a retention period and deletion process in the data processing agreement. 90 days. |
| F-10 | MailBloom | No independent penetration test in three years | 2 | 2 | Medium | Vendor to commission a test and share a summary of findings and fixes. 90 days. |
| F-12 | Brightwell (internal) | Free-text manager comments sent to PeopleMetrics may contain sensitive information | 1 | 3 | Medium | Stop sending free-text comments and give managers guidance on what not to record. 90 days. |
| F-03 | CloudNimbus | Subcontractor list not provided proactively | 2 | 1 | Low | Add a clause requiring a current list and notice of changes, bundled with the F-01 amendment. |
| F-08 | PeopleMetrics | SOC 2 Type I report only | 1 | 2 | Low | Request a Type II timeline. Reviewed at next annual assessment. |

### 4.3 Remediation Timelines

Target timelines depend on rating: 30 days for Critical, 60 days for High, 90 days for Medium, and the next scheduled review for Low. Where a vendor misses a deadline, the GRC team escalates to the business owner and the Privacy Lead. A finding that cannot be fixed by the deadline may be formally accepted by the business owner if the Privacy Lead agrees, with the reason, compensating controls, and a review date recorded.

### 4.4 Summary and Priorities

The register contains twelve findings: ten from vendor assessments and two internal Brightwell actions identified during the DPIA. One is Critical, five are High, four are Medium, and two are Low.

**F-04 is the priority.** EU employee data is already being transferred to the US without a legal safeguard, so this is a current compliance gap and not a possibility. It is also the main reason a DPIA is required for PeopleMetrics (Section 5).

**Several actions can be combined.** The breach notification, subcontractor, and retention findings are all fixed through contract terms. Sending one amendment request to each vendor is faster than raising each finding separately. For CloudNimbus, F-01 and F-03 go together. For PeopleMetrics, F-04, F-06, and F-07 go together.

**Two findings are candidates for risk acceptance.** F-02 and F-08 are Medium and Low, and the vendors may not be able to change them quickly. If the business owner accepts them, CloudNimbus's lack of customer-managed keys is partly offset by its encryption at rest and ISO 27001 certification, and PeopleMetrics's Type I report is partly offset by being reassessed in twelve months.

**Two findings are Brightwell's own to fix.** F-11 and F-12 do not depend on any vendor. They are owned by the EU HR Manager and can be completed without waiting for a contract change.

**Vendor risk ratings.** Applying the rule in 4.1, PeopleMetrics is rated Critical, CloudNimbus High, and MailBloom High. These are recorded in Appendix A.

### 4.5 Tracking

The register is maintained in a spreadsheet (Appendix C) with additional columns for the date opened, action owner, status, and due date. The GRC team reviews open findings monthly, and closed findings are kept for audit purposes.

---
