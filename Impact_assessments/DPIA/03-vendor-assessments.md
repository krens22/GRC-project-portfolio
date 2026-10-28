## Section 3: Vendor Assessments

### 3.1 Approach

Each vendor is assessed using the method set out for its tier in Section 1.4. Tier 1 and Tier 2 vendors complete the Standardized Information Gathering Lite questionnaire (SIG Lite), a general security and privacy questionnaire published by Shared Assessments. Cloud vendors complete the Cloud Security Alliance's Consensus Assessments Initiative Questionnaire (CAIQ), which adds cloud-specific questions on areas such as encryption key management and separation between customers. Tier 3 vendors complete a ten-question custom form covering policy, access control, encryption, data location, security testing, training, incident notification, data retention, independent certification, and recovery planning. Tier 4 vendors receive an onboarding check confirming that the company is legitimate and has no known breaches.

Standard questionnaires are used where possible because many vendors already hold a completed copy, which shortens turnaround and makes responses comparable across vendors. For Tier 1 vendors, the questionnaire is supplemented by an independent assurance document such as a SOC 2 report or ISO 27001 certificate, because a questionnaire records what the vendor says about itself and an audit report records what an independent party has verified.

Responses are rated against Brightwell's expectations as meeting, partially meeting, or not meeting the requirement. Only responses that affect risk are carried into the findings below. The completed questionnaires are retained in Appendix B.

### 3.2 Assessments Completed

Three vendors have completed assessments: CloudNimbus (Tier 1), PeopleMetrics (Tier 2), and MailBloom (Tier 2). OfficeBrew and PixelStock completed the Tier 4 check with no concerns.

**CloudNimbus.** CloudNimbus completed the CAIQ and provided a current ISO 27001 certificate. Its controls over core protections are sound: customer data is encrypted at rest (AES-256) and in transit (TLS 1.2 or higher), each customer's data is logically separated from others, and the separation is tested annually. Three weaknesses were identified. CloudNimbus commits to notifying customers of a breach within seven days of confirmation, which is incompatible with the 72-hour deadline that GDPR sets for notifying the regulator, because Brightwell could learn of an incident only after that deadline has passed. Encryption keys are managed solely by CloudNimbus, and customers cannot hold their own, which limits Brightwell's ability to protect data if the vendor itself is compromised. The list of subcontractors with access to Brightwell data is provided only on request, so changes could go unnoticed.

**PeopleMetrics.** PeopleMetrics completed SIG Lite and provided a SOC 2 Type I report. The assessment identified the most significant gaps of the three vendors. EU employee data is stored exclusively in US data centers, and Standard Contractual Clauses, the pre-approved contract terms that give EU data a legal safeguard when transferred outside the EU, are not in place. Performance scores are generated automatically and used without any human review step. The vendor has no defined data retention period and keeps data until the contract ends. Breach notification takes up to five business days. The SOC 2 Type I report confirms that controls were suitably designed at a single point in time, but it does not test whether they operated effectively over a period, which a Type II report would. The combination of cross-border transfer, large-scale evaluation of employees, and automated scoring meets the DPIA triggers in Section 1.5, and the DPIA is presented in Section 5.

**MailBloom.** MailBloom completed SIG Lite. Its handling of the data itself is adequate: databases and backups are encrypted, staff complete annual security training with completion records, unsubscribe requests are honored within 48 hours with an audit log, and customer data can be deleted within 30 days of a request. Two weaknesses were identified. Multi-factor authentication is not required for administrator accounts and is offered to customers only as an option, so a stolen password alone could give an attacker control of the platform and the customer email list. MailBloom has also not had an independent penetration test in three years, which means weaknesses introduced since then have not been tested by an outside party.

### 3.3 Findings

The findings below are carried into the risk register in Section 4, where each is rated and assigned a remediation action.

| ID | Vendor | Finding |
|---|---|---|
| F-01 | CloudNimbus | Breach notification takes up to seven days, exceeding the GDPR 72-hour window |
| F-02 | CloudNimbus | No customer-managed encryption keys |
| F-03 | CloudNimbus | Subcontractor list not provided proactively |
| F-04 | PeopleMetrics | EU employee data stored in the US without Standard Contractual Clauses |
| F-05 | PeopleMetrics | Automated performance scores used with no human review |
| F-06 | PeopleMetrics | No defined data retention period |
| F-07 | PeopleMetrics | Breach notification takes up to five business days |
| F-08 | PeopleMetrics | SOC 2 Type I report only |
| F-09 | MailBloom | Multi-factor authentication not required for administrator accounts |
| F-10 | MailBloom | No independent penetration test in three years |

Two further findings, F-11 and F-12, concern Brightwell's own practices and were identified during the DPIA. They are recorded in Section 4 and explained in Section 5.

### 3.4 Outstanding Assessments

PayrollPro, ShopStream, HelpDeskly, DataLens BI, and MeetSphere have not yet been assessed, as noted in Section 2.5. Tier 1 assessments for PayrollPro and ShopStream are the priority. PayrollPro will complete SIG Lite and provide a SOC 2 report, and ShopStream will complete SIG Lite and provide its PCI DSS attestation, the industry standard evidence that payment card data is handled securely.

---
