## Appendix A: SOC 2 Type II report excerpts (fictional)

> *These excerpts were constructed for this portfolio exercise. VigilGrid Security Inc., Harcourt & Lindqvist LLP, and all report contents are fictional. They are condensed from the format of a real SOC 2 Type II report.*

### A.1 Independent service auditor's report

Prepared by: Harcourt & Lindqvist LLP (fictional)
Report type: SOC 2 Type II
Period covered: October 1, 2025 to March 31, 2026
Report issued:
Criteria covered: Security, Availability, Confidentiality

In our opinion, except for the matters described in the paragraph below, the controls were suitably designed and operated effectively throughout the period to provide reasonable assurance that VigilGrid's service commitments and system requirements were achieved.

Basis for qualification: Controls related to the removal of user access (CC6.3) did not operate effectively for the full period, as described in Section IV.

### A.2 System description
Services in scope:

24/7 security monitoring by the VigilGrid Security Operations Center (SOC)
Collection and storage of endpoint telemetry from customer devices
Alert triage, analyst-led investigation, and customer notification

Services not included in this description:

The Automated Response module (host isolation and process termination), generally available since December 2025, is under evaluation for inclusion in the next reporting period.
The Customer Portal mobile application.

Infrastructure: Customer telemetry is hosted in the US-East region of a major public cloud provider. Telemetry is retained for 13 months.


**Subservice organizations (carve-out method):**
| Subservice organization |  Function  |
| -------- | -------- | 
| Public cloud provider  | Hosting and storage |    
| Threat intelligence data provider | Indicator feeds used for detection |   
| Overnight SOC staffing partner  |  Tier 1 analyst coverage, 22:00 to 06:00 UTC  |  
Controls at these organizations are excluded from the scope of this report.

### A.3 Tests of controls and results 

|  Ref |  Control  |  Test Performed  | Result |
| -------- | -------- | -------- |
| CC6.2 | Privileged access to the production SOC console is reviewed quarterly by management  |  Inspected review records for both quarters in the period |	Exceptions noted. Reviews were not performed in either quarter (Q4 2025, Q1 2026). | 
| CC6.3 | Access is removed within 24 hours of employee termination  |  Inspected a sample of 25 of 61 terminations | Exceptions noted. For 2 of 25, access was removed after 5 and 9 days. | 
| CC7.2 | Systems are monitored for anomalies and alerts are reviewed  |  Inspected monitoring configuration and sample alert tickets |	No exceptions noted.  |  
| CC7.3 | Security incidents are evaluated, contained and communicated per the incident response plan| Inspected the incident response plan and tabletop exercise records |	No exceptions noted. No security incidents occurred during the period.|
|CC8.1 | Changes to detection rules and production code are tested and peer-reviewed before release | Inspected a sample of 40 of 312 changes	| Exception noted. 1 of 40 was an emergency change released without peer review. |
| CC9.2 | Management assesses risks of subservice organizations annually | Inspected vendor assessment records | Exception noted. No assessment was completed for the overnight SOC staffing partner.|
| A1.2 | Backups are performed and restoration is tested | Inspected backup logs and restore test	| No exceptions noted.|
| C1.2 | Customer data is deleted within 90 days of contract termination|Inquired of management; inspected the deletion procedure | No exceptions noted. No customer terminations occurred during the period; operating effectiveness was not tested.|

### A.4 Management's responses to exceptions
CC6.2: Management acknowledges the missed reviews, which resulted from staff turnover. Managers performed informal spot checks of administrator accounts during these quarters.

CC6.3: The two instances involved contractors whose offboarding tickets were routed to the wrong queue. The accounts were disabled upon discovery. No unauthorized activity was identified.

CC8.1: The emergency change addressed an active detection failure and was reviewed retroactively by the engineering lead.

CC9.2: The assessment is scheduled for Q3 2026.

### A.5 Complementary user entity controls
VigilGrid's controls assume that customers have implemented the following:

Install the VigilGrid agent on all in-scope endpoints and apply agent updates within 30 days of release.
Forward logs from all required sources to VigilGrid.
Maintain a current list of authorized contacts for incident escalation and response approval, and notify VigilGrid of changes within 24 hours.
Restrict access to VigilGrid API keys and the customer portal to authorized personnel.
Evaluate whether monitoring and response actions on endpoints comply with applicable local labor and privacy laws.
