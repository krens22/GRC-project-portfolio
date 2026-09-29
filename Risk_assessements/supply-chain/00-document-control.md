<details>
<summary><b>Footnotes</b></summary>

It follows the logic of a real risk assessment: what are we assessing and why (Sections 1-2), how (Section 3), what did we find (Sections 4-7), what do we do about it (Sections 8-9).

</details>

## Company Fact sheet

|| Item | Detail |
|---|---|
| Legal name | Harborline Health Systems Inc. |
| Headquarters | Toronto, Ontario (downtown office), hybrid workforce |
| Founded | 2017 |
| Employees | About 250 |
| What it does | Cloud platform for online appointment booking, patient reminders, and virtual care visits |
| Customers | About 400 clinics across Ontario |
| Patients served | About 1.5 million patient records |
| Revenue model | Monthly subscription per clinic |
| Annual revenue | About $38M CAD |

### Data handling info
- Patient names, contact details, and Ontario health card numbers.
- Appointment history and visit type.
- Video visit metadata (times, durations, participants), but not the recorded content, since Harborline doesn't record calls.
- Clinic staff login details
- Payment data (handled through the payment processor, not stored in full by Harborline).

### Regulatory and contractual info
- **PHIPA** (Ontario health privacy law): Harborline acts as an "electronic service provider" for clinics, which means it must protect health data on their behalf and support their compliance.
- **PIPEDA**: federal privacy law for its commercial activities.

- Customer contracts: many clinics require breach notification within a set window and evidence of security controls.
- Security framework: Harborline is working toward ISO 27001 certification and has completed a SOC 2 Type I report. It is not yet certified, which is realistic for a growing company and leaves room for findings.

### Technological overview
- Harborline's web and mobile apps are hosted in a ** public cloud**(Canada region).
- **Microservices architecture** with a heavy use of **open-source libraries**.
- Single sign-on and MFA for employees and clinic staff.
- Nightly backups and a documented disaster recovery plan tested once a year.

### Governance
|  Roles | Responsibilities | 
| -------- | -------- | 
| CISO    | Owns security and this assessment   | 
|Head of GRC   | Reviews the report     | 
| Director of Procurement | Manages vendor contracts | 
| Director of IT Operations | Manages technical vendor relationships | 
| Privacy Officer |Oversees PHIPA/PIPEDA compliance | 

### Current Third-party risk practices
- Vendor list exists(spreadsheet) maintained by procurement but not always up to date.
- Security questionnaires are sent to new vendors, but there's no **re-review** after onboarding.
- Contracts vary; some include breach-notification clauses, others don't.
- No formal tiering of vendors by criticality.
- Vendor access to systems is reviewed informally, not on a schedule.
- No one tracks the open-source software components (SBOM) in a structured way.

| # | Supplier (fictional) | Type | What they provide | Data or access they have |
|---|---|---|---|---|
| 1 | CumulusPeak Cloud | Cloud hosting | Servers, databases, storage, networking | All production data; hosts the entire platform |
| 2 | ClearView Video API | Telehealth component | Video call engine embedded in the app | Video visit metadata; live call traffic |
| 3 | PingRelay Messaging | SMS/email delivery | Appointment reminders to patients | Patient names, phone numbers, appointment times |
| 4 | PayBridge Processing | Payment processor | Clinic subscription and patient co-pay payments | Payment data (card details stay with PayBridge) |
| 5 | SentryOps Managed Services | Managed IT/security provider | 24/7 monitoring, service desk, patching support | Privileged admin access to internal systems |
| 6 | GateKey Identity | Identity and MFA | Single sign-on and multi-factor login | Staff and clinic user identities and credentials |
| 7 | Meridian Dev Studio | Offshore software contractor | Extra developers working on new features | Access to source code and test environments |
| 8 | VaultSafe Backup | Backup and recovery | Encrypted offsite backups | Copies of production data (encrypted) |
| 9 | InsightLoop Analytics | Product analytics | Usage tracking to improve the product | De-identified usage data |
| 10 | PayrollPoint HR | HR and payroll platform | Payroll and employee records | Employee personal and financial information |
| 11 | TerraTech Hardware Supply | Hardware reseller | Employee laptops and office network equipment | Physical devices; no data access |
| 12 | Open-source components | Software dependencies | Hundreds of libraries and frameworks inside the platform | Runs inside Harborline's own code |
