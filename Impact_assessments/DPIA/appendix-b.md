## Appendix B: Completed Questionnaires

The tables below are excerpts of the completed questionnaires, showing the responses that affect risk and a sample of those that meet expectations.

### B.1 Short Custom Form (Tier 3 vendors)

1. Do you have a written information security policy that is reviewed at least once a year?
2. Is multi-factor authentication (MFA) required for all staff who can access customer data?
3. Is our data encrypted when stored and when sent over the internet?
4. Where is our data stored, and which subcontractors can access it?
5. Do you run a penetration test (a hired, authorized attack on your own systems to find weaknesses) at least once a year?
6. Do all staff complete security training at least once a year?
7. How quickly will you tell us about a security incident affecting our data?
8. How long do you keep our data, and can you delete it on request?
9. Do you hold an independent certification or audit report (SOC 2, ISO 27001)?
10. Do you have a tested plan to recover if your service goes down?

### B.2 CloudNimbus (CSA CAIQ excerpt)

| Area | Question | Vendor response | Rating |
|---|---|---|---|
| Encryption | Is customer data encrypted at rest and in transit? | Yes. AES-256 at rest, TLS 1.2 or higher in transit. | Meets |
| Key management | Can the customer control its own encryption keys? | No. Keys are managed by CloudNimbus only. | Partially meets |
| Tenant isolation | Is each customer's data logically separated from others? | Yes. Separate virtual networks and storage per customer, tested annually. | Meets |
| Incident response | How soon is the customer told about a breach? | Within 7 days of confirmation. | Gap |
| Subcontractors | Is a current list of subcontractors provided? | Provided on request only. | Partially meets |
| Assurance | Does the vendor hold an independent certification? | ISO 27001 certificate, current. | Meets |

### B.3 PeopleMetrics (SIG Lite excerpt)

| Area | Question | Vendor response | Rating |
|---|---|---|---|
| Data location | Where is customer data stored? | US-based data centers only. | Gap |
| Transfer safeguards | Are Standard Contractual Clauses (SCCs) signed for EU data? | Not yet in place. | Gap |
| Data retention | Is there a defined retention period and deletion process? | Data kept until the contract ends, no fixed period. | Partially meets |
| Automated decisions | Can scores be reviewed by a human before use? | Scores are generated automatically with no review step. | Gap |
| Incident response | How soon is the customer told about a breach? | Within 5 business days. | Partially meets |
| Assurance | Does the vendor hold an independent audit report? | SOC 2 Type I only. | Partially meets |

### B.4 MailBloom (SIG Lite excerpt)

| Area | Question | Vendor response | Rating |
|---|---|---|---|
| Access control | Is MFA required for administrator accounts? | Not required. Optional for customers. | Gap |
| Security testing | Is an independent penetration test done every year? | No annual test. Last test was three years ago. | Gap |
| Encryption | Is stored customer data encrypted? | Yes. Databases and backups are encrypted. | Meets |
| Training | Do staff complete security training each year? | Yes, annually with a completion record. | Meets |
| Consent | Are unsubscribe requests honored and recorded? | Yes, within 48 hours, with an audit log. | Meets |
| Data deletion | Can customer data be deleted on request? | Yes, within 30 days. | Meets |

---
