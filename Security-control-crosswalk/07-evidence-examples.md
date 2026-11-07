## Evidence Examples

The table below gives one example of evidence an auditor would typically request for each control. Actual requests vary by auditor and scope.

| # | Control | Example evidence | What it proves |
|---|---|---|---|
| 1 | Access control | A quarterly user access review: an export of users and their roles from the identity system, signed off by each manager, plus tickets showing access removed for 5 sampled leavers | Access is reviewed regularly and removed when people leave |
| 2 | Multi-factor authentication | A screenshot or export of the identity provider's policy showing MFA required for all users, plus a report showing every account is enrolled | MFA is enforced, not just available |
| 3 | Encryption | Cloud storage settings showing encryption at rest enabled (for example, AES-256), plus a website scan report confirming secure connections (TLS 1.2 or higher) | Data is protected both when stored and when sent |
| 4 | Logging and monitoring | A SIEM (security monitoring tool) screenshot showing log sources connected and log retention set, plus one sample alert with a ticket showing someone investigated it | Activity is recorded, watched, and acted on |
| 5 | Incident response | An approved incident response plan with a version and date, plus a report from a practice exercise (a "tabletop") or a ticket timeline from a real incident | The plan exists and has been tested |
| 6 | Vendor management | A vendor inventory with risk ratings, one completed vendor review (for example, notes from reading a vendor's SOC 2 report), and a signed data processing agreement | Vendors are assessed and bound by contract |
| 7 | Backup and recovery | A backup job report showing successful runs, plus a record of a restore test with the date, what was restored, and the result | Backups work and can actually be restored |
| 8 | Change management | A sample of change tickets showing the request, approval, testing, and deployment date for each | Changes are authorized and tested before going live |
| 9 | Vulnerability management | A vulnerability scan report ranked by severity, plus tickets showing critical findings fixed within the time the policy sets | Weaknesses are found and fixed on schedule |
| 10 | Security awareness training | A completion report (for example, 98% of staff finished this year), the training content, and results from a phishing simulation | Staff are trained and the training is tracked |

### Framework-specific evidence notes

- **PCI DSS logging (Requirement 10):** audit logs must be kept for at least 12 months, with the most recent 3 months immediately available for analysis.
- **PCI DSS scanning (Requirement 11.3):** external vulnerability scans must be run at least quarterly by an Approved Scanning Vendor (ASV), a company certified by the PCI Security Standards Council.
- **PCI DSS incident response (Requirement 12.10):** the plan must be reviewed and tested at least once a year, which is why the incident response row asks for test evidence.
