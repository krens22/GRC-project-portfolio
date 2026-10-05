# 5. Risk Assessment Findings

This section presents the risks identified for each in-scope supplier. Tier 1 and Tier 2 suppliers are assessed in detail (Section 5.2); Tier 3 and Tier 4 suppliers receive a light-touch review (Section 5.3). Risks are scored using the model in Section 3.4 and rated using the thresholds in Section 3.5. Each finding states the condition observed, the standard it is measured against, the resulting risk, and a recommendation.

## 5.1 Summary of Results
## 5.2 Detailed Findings
| Item | Detail |
|---|---|
| Service | Cloud hosting: servers, databases, storage, networking |
| Data or access | All production data; hosts the entire platform |
| Evidence reviewed | SOC 2 Type II report; hosting contract; security questionnaire |
**Existing controls observed:** multi-factor authentication for administrator accounts; encryption of data at rest; access logging; deployment across multiple zones within a Canadian region.

### 5.2.1 S-01 CumulusPeak Cloud (Tier 1)

# 5. Risk Assessment Findings

This section presents the risks identified for each in-scope supplier. Tier 1 and Tier 2 suppliers are assessed in detail (Section 5.2); Tier 3 and Tier 4 suppliers receive a light-touch review (Section 5.3). Risks are scored using the model in Section 3.4 and rated using the thresholds in Section 3.5. Each finding states the condition observed, the standard it is measured against, the resulting risk, and a recommendation.

## 5.1 Summary of Results

Twenty-seven risks were identified across the 11 suppliers assessed.

| Residual rating | Number of risks |
|---|---|
| Critical | 0 |
| High | 11 |
| Medium | 14 |
| Low | 2 |

Three risks (SC-004, SC-009, SC-023) were rated Critical before controls were considered, but fall to High once existing controls are taken into account. The highest residual risk is SC-012 (excessive and lingering repository access at Meridian Dev Studio, score 16), followed by four risks scored 15: SC-004 (privileged access misuse at SentryOps), SC-009 (malicious or vulnerable code from Meridian), SC-023 (known library vulnerabilities), and SC-024 (compromised libraries).
## 5.2 Detailed Findings

### 5.2.1 S-01 CumulusPeak Cloud (Tier 1)

| Item | Detail |
|---|---|
| Service | Cloud hosting: servers, databases, storage, networking |
| Data or access | All production data; hosts the entire platform |
| Evidence reviewed | SOC 2 Type II report; hosting contract; security questionnaire |

**Existing controls observed:** multi-factor authentication for administrator accounts; encryption of data at rest; access logging; deployment across multiple zones within a Canadian region.

| Risk ID | Risk | Inherent (L×I) | Residual (L×I) | Rating |
|---|---|---|---|---|
| SC-001 | Unauthorized access to production patient data through a compromised administrator account | 3 × 5 = 15 | 2 × 5 = 10 | High |
| SC-002 | Extended platform outage caused by a failure at the hosting provider | 3 × 4 = 12 | 2 × 4 = 8 | Medium |
| SC-003 | Late notification of a security incident by the supplier | 3 × 3 = 9 | 3 × 3 = 9 | Medium |

#### Finding 5.2.1-A: Incident notification window is longer than some customer commitments (SC-003)

- **Condition:** The hosting contract requires CumulusPeak to notify Harborline of a security incident within 72 hours.
- **Criteria:** Some Harborline clinic contracts require Harborline to notify clinics within 48 hours. ISO/IEC 27001 Annex A 5.20 expects supplier agreements to address information security requirements, including incident handling.
- **Risk:** Harborline could learn of an incident after its own deadline to notify clinics has passed, creating contractual and PHIPA exposure.
- **Recommendation:** Amend the contract to require notification within 24 hours of the supplier becoming aware of an incident.

#### Finding 5.2.1-B: Recovery from a hosting failure has not been tested against the supplier's outage scenarios (SC-002)

- **Condition:** Harborline tests its disaster recovery plan once a year. The test does not simulate a failure of the hosting provider's region.
- **Criteria:** ISO/IEC 27001 Annex A 5.23 expects organizations to manage the risks of using cloud services, including continuity.
- **Risk:** A regional outage could last longer than expected because recovery steps have not been rehearsed for that scenario.
- **Recommendation:** Add a regional-failure scenario to the next annual disaster recovery test and record the recovery time achieved.

*(SC-001 is covered by existing controls and is addressed in the risk register and Section 8, because its residual rating is High but the controls observed meet expectations. See Section 6.)*

### 5.2.2 S-05 SentryOps Managed Services (Tier 1)

| Item | Detail |
|---|---|
| Service | 24/7 monitoring, service desk, patching support |
| Data or access | Privileged administrative access to internal systems |
| Evidence reviewed | ISO/IEC 27001 certificate; managed services contract; security questionnaire |

**Existing controls observed:** background checks on engineers; multi-factor authentication on remote administrator sessions.

| Risk ID | Risk | Inherent (L×I) | Residual (L×I) | Rating |
|---|---|---|---|---|
| SC-004 | Misuse or compromise of privileged access to Harborline systems | 4 × 5 = 20 | 3 × 5 = 15 | High |
| SC-005 | Late notification of a security incident by the supplier | 3 × 3 = 9 | 3 × 3 = 9 | Medium |

#### Finding 5.2.2-A: Shared administrator accounts and no scheduled access review (SC-004)

- **Condition:** Some SentryOps engineers share administrator accounts on Harborline systems, and Harborline does not review on a fixed schedule which SentryOps staff hold access.
- **Criteria:** ISO/IEC 27001 Annex A 5.16 (identity management), 5.18 (access rights), and 8.2 (privileged access rights) expect each user to be individually identifiable and access to be reviewed.
- **Risk:** Harborline cannot attribute an action to a specific person, and access that is no longer needed can persist unnoticed. Privileged access is a direct route to all patient data.
- **Recommendation:** Require named individual accounts for every SentryOps engineer within 60 days, store administrator credentials in a privileged access vault, and review the access list quarterly.

#### Finding 5.2.2-B: Open-ended incident notification and no right to audit (SC-005)

- **Condition:** The contract requires SentryOps to notify Harborline "promptly" with no time limit, and contains no right-to-audit clause.
- **Criteria:** ISO/IEC 27001 Annex A 5.20 (security in supplier agreements) and 5.22 (monitoring supplier services). Some clinic contracts require Harborline to notify clinics within 48 hours.
- **Risk:** Harborline could learn of an incident too late to meet its own notification duties, and has no contractual way to verify SentryOps' controls.
- **Recommendation:** Amend the contract to require notification within 24 hours and add a right to audit or to receive annual assurance reports.

### 5.2.3 S-06 GateKey Identity (Tier 1)

| Item | Detail |
|---|---|
| Service | Single sign-on and multi-factor login |
| Data or access | Staff and clinic user identities and credentials |
| Evidence reviewed | SOC 2 Type II report (14 months old); ISO/IEC 27001 certificate; contract; questionnaire |

**Existing controls observed:** encrypted credential storage; MFA for supplier administrators; redundant infrastructure across two regions; 24-hour incident notification; 99.9% uptime commitment.

| Risk ID | Risk | Inherent (L×I) | Residual (L×I) | Rating |
|---|---|---|---|---|
| SC-006 | Login outage locks staff and clinics out of the platform | 3 × 4 = 12 | 2 × 4 = 8 | Medium |
| SC-007 | Compromise of the identity provider leads to unauthorized access to production systems | 3 × 5 = 15 | 2 × 5 = 10 | High |
| SC-008 | Control weaknesses go undetected because assurance evidence is out of date | 3 × 3 = 9 | 2 × 3 = 6 | Medium |

#### Finding 5.2.3-A: No emergency access path if the identity provider is unavailable (SC-006)

- **Condition:** Harborline has no emergency ("break-glass") route into production systems that works without GateKey.
- **Criteria:** ISO/IEC 27001 Annex A 5.29 (security during disruption) and 5.30 (ICT readiness for continuity).
- **Risk:** In a GateKey outage, Harborline engineers could be unable to reach systems to diagnose or recover, prolonging the disruption for clinics.
- **Recommendation:** Create a small number of sealed emergency accounts with credentials held offline, restricted to named senior staff, and test them every quarter.

#### Finding 5.2.3-B: Assurance report is older than 12 months (SC-008)

- **Condition:** The most recent GateKey SOC 2 Type II report was issued 14 months ago, and a newer report has not been requested.
- **Criteria:** ISO/IEC 27001 Annex A 5.22 expects suppliers' services to be monitored and reviewed regularly.
- **Risk:** Harborline is relying on evidence that may no longer reflect current controls. (The current ISO 27001 certificate limits this risk.)
- **Recommendation:** Request the latest SOC 2 report now and add an annual renewal reminder for all Tier 1 and 2 suppliers.

### 5.2.4 S-07 Meridian Dev Studio (Tier 1)

| Item | Detail |
|---|---|
| Service | Additional developers working on new features |
| Data or access | Access to source code and test environments |
| Evidence reviewed | Security questionnaire; contract; signed NDAs. No independent assurance report available |

**Existing controls observed:** Harborline engineers review all code before release; contractors connect to repositories through a VPN.

| Risk ID | Risk | Inherent (L×I) | Residual (L×I) | Rating |
|---|---|---|---|---|
| SC-009 | Malicious or vulnerable code introduced into the production platform | 4 × 5 = 20 | 3 × 5 = 15 | High |
| SC-010 | Credential theft through unmanaged personal laptops | 4 × 4 = 16 | 3 × 4 = 12 | High |
| SC-011 | Exposure of production-derived data in the test environment | 3 × 4 = 12 | 3 × 3 = 9 | Medium |
| SC-012 | Excessive and lingering access to the code repository | 4 × 4 = 16 | 4 × 4 = 16 | High |
| SC-013 | Missing contractual safeguards and independent assurance | 3 × 3 = 9 | 3 × 3 = 9 | Medium |

#### Finding 5.2.4-A: Contractors use unmanaged personal laptops (SC-010)

- **Condition:** Meridian developers use personal laptops with no endpoint management, connecting to Harborline repositories through a VPN.
- **Criteria:** ISO/IEC 27001 Annex A 8.1 (user endpoint devices) and 6.7 (remote working).
- **Risk:** A laptop infected with malware could expose repository credentials, giving an attacker a path into Harborline's source code. A VPN protects the connection but not the device.
- **Recommendation:** Require contractors to use Harborline-managed devices or a managed virtual desktop, with disk encryption and endpoint protection enforced.

#### Finding 5.2.4-B: Broad repository access with no removal process (SC-012)

- **Condition:** All contractor developers hold write access to the main code repository, and there is no formal process to remove access when contractor staff leave the project.
- **Criteria:** ISO/IEC 27001 Annex A 5.15 (access control), 5.18 (access rights), and 6.5 (responsibilities after termination or change).
- **Risk:** A departed or unneeded contractor could keep the ability to change production code. This is the highest residual risk in the assessment because no control currently reduces it.
- **Recommendation:** Limit contractors to the branches they need, require Harborline approval for every merge to the main branch, and review contractor access monthly with a same-day removal process for leavers.

#### Finding 5.2.4-C: Production-derived data in the test environment (SC-011)

- **Condition:** The test environment contains partially masked copies of production data, accessible to Meridian developers.
- **Criteria:** ISO/IEC 27001 Annex A 8.33 (test information) and 8.11 (data masking).
- **Risk:** Patient information could be exposed to offshore contractors working on unmanaged devices. Partial masking reduces but does not remove the impact.
- **Recommendation:** Replace production-derived data with fully synthetic test data within 90 days.

#### Finding 5.2.4-D: No contractual security requirements or independent assurance (SC-009, SC-013)

- **Condition:** The contract has no right-to-audit clause, no restriction on subcontracting, and no secure-coding requirements. Meridian provides no independent assurance report.
- **Criteria:** ISO/IEC 27001 Annex A 5.20 (supplier agreements), 5.22 (monitoring), 8.25 (secure development life cycle), and 8.28 (secure coding).
- **Risk:** Harborline cannot verify how Meridian develops code or controls its staff, and Meridian could pass work to unvetted subcontractors.
- **Recommendation:** Amend the contract to require secure-coding practices, prohibit subcontracting without written approval, and grant audit rights. Add automated code scanning to Harborline's release process.

### 5.2.5 S-02 ClearView Video API (Tier 2)

| Item | Detail |
|---|---|
| Service | Video call engine embedded in the app |
| Data or access | Video visit metadata; live call traffic |
| Evidence reviewed | SOC 2 Type II report; penetration test summary letter; contract; questionnaire |

**Existing controls observed:** video traffic encrypted in transit; calls are not recorded; 99.9% uptime commitment.

| Risk ID | Risk | Inherent (L×I) | Residual (L×I) | Rating |
|---|---|---|---|---|
| SC-014 | Patient data handled outside Canada by unknown sub-processors | 3 × 4 = 12 | 2 × 4 = 8 | Medium |
| SC-015 | Outage halts virtual visits | 3 × 3 = 9 | 3 × 3 = 9 | Medium |

#### Finding 5.2.5-A: Data location and sub-processors are not known (SC-014)

- **Condition:** Call traffic may be relayed through servers in the United States as well as Canada, and ClearView has not provided a list of its sub-processors.
- **Criteria:** ISO/IEC 27001 Annex A 5.19 and 5.20 (security in supplier relationships and agreements). Harborline hosts its platform in a Canadian region, and clinic customers may expect patient-related data to stay there.
- **Risk:** Harborline cannot confirm who handles patient visit data or where, which creates privacy and contractual exposure.
- **Recommendation:** Obtain a sub-processor list and data-flow description, and negotiate a clause limiting call relay and metadata storage to Canada where feasible.

#### Finding 5.2.5-B: No fallback if the video provider fails (SC-015)

- **Condition:** There is no alternative video provider or documented workaround if ClearView is unavailable.
- **Criteria:** ISO/IEC 27001 Annex A 5.30 (ICT readiness for business continuity).
- **Risk:** Virtual visits stop until ClearView recovers. Booking and reminders are unaffected, so impact is rated Moderate.
- **Recommendation:** Document a fallback procedure (for example, clinics switching to phone visits) and evaluate a secondary provider.

### 5.2.6 S-03 PingRelay Messaging (Tier 2)

| Item | Detail |
|---|---|
| Service | Appointment reminders to patients by SMS and email |
| Data or access | Patient names, phone numbers, appointment times |
| Evidence reviewed | SOC 2 Type I report; questionnaire; contract |

**Existing controls observed:** encryption in transit between Harborline and PingRelay; role-based access to message logs.

| Risk ID | Risk | Inherent (L×I) | Residual (L×I) | Rating |
|---|---|---|---|---|
| SC-016 | Exposure of patient contact and appointment data held by the supplier | 4 × 4 = 16 | 3 × 4 = 12 | High |
| SC-017 | Late or no notification of a security incident | 3 × 3 = 9 | 3 × 3 = 9 | Medium |
| SC-018 | Reminder service outage | 3 × 3 = 9 | 3 × 3 = 9 | Medium |

#### Finding 5.2.6-A: Long data retention with no deletion obligation (SC-016)

- **Condition:** PingRelay keeps message logs (names, phone numbers, appointment times) for 24 months, and the contract has no requirement to delete data at the end of the relationship. Reminders are sent as standard SMS, and the carriers used are not disclosed.
- **Criteria:** ISO/IEC 27001 Annex A 5.34 (privacy and protection of personal information) and 8.10 (information deletion). PIPEDA expects personal information to be kept only as long as necessary.
- **Risk:** More patient data is exposed for longer than needed if PingRelay is breached.
- **Recommendation:** Negotiate a retention period of 90 days or less, a deletion-at-exit clause, and disclosure of SMS carriers. Reduce the detail in reminder text (for example, avoid visit type).

#### Finding 5.2.6-B: No incident notification clause and limited assurance (SC-017)

- **Condition:** The contract has no incident notification clause, and PingRelay's only assurance report is a SOC 2 Type I, which checks control design on one date but not whether controls worked over time.
- **Criteria:** ISO/IEC 27001 Annex A 5.20 and 5.22.
- **Risk:** Harborline may not hear about an incident at all, and has weaker evidence of the supplier's controls than for other Tier 2 suppliers.
- **Recommendation:** Add a 24-hour notification clause and require a SOC 2 Type II report within 12 months.

#### Finding 5.2.6-C: Single provider for reminders (SC-018)

- **Condition:** Reminders depend on PingRelay alone, with no backup provider.
- **Criteria:** ISO/IEC 27001 Annex A 5.30.
- **Risk:** An outage delays reminders for all clinics, which may increase missed appointments, though care itself is not stopped.
- **Recommendation:** Document a manual fallback (such as email-only reminders) and assess adding a secondary messaging provider.

### 5.2.7 S-04 PayBridge Processing (Tier 2)

| Item | Detail |
|---|---|
| Service | Clinic subscription and patient co-pay payments |
| Data or access | Payment data (card details stay with PayBridge) |
| Evidence reviewed | PCI DSS Attestation of Compliance; SOC 2 Type II report; contract |

**Existing controls observed:** card data tokenized and never stored by Harborline; fraud monitoring; strong access controls; 24-hour incident notification; annual audit reports provided.

| Risk ID | Risk | Inherent (L×I) | Residual (L×I) | Rating |
|---|---|---|---|---|
| SC-019 | Payment processing outage | 3 × 3 = 9 | 2 × 3 = 6 | Medium |
| SC-020 | Lapse in PCI compliance evidence goes unnoticed | 3 × 2 = 6 | 3 × 2 = 6 | Medium |

PayBridge's controls and contract terms meet expectations. The only gap is on Harborline's side.

#### Finding 5.2.7-A: No process to track renewal of the supplier's PCI attestation (SC-020)

- **Condition:** PayBridge's PCI DSS attestation expires in four months, and Harborline has no process to track renewals.
- **Criteria:** ISO/IEC 27001 Annex A 5.22 expects regular monitoring of supplier services and their assurance evidence.
- **Risk:** If PayBridge's attestation lapsed, Harborline might not notice and would be unable to evidence payment compliance to customers.
- **Recommendation:** Add expiry dates for all supplier assurance reports to the supplier register, with a reminder 90 days before each expires.

### 5.2.8 S-08 VaultSafe Backup (Tier 2)

| Item | Detail |
|---|---|
| Service | Encrypted offsite backups |
| Data or access | Encrypted copies of production data |
| Evidence reviewed | SOC 2 Type II report; contract; questionnaire |

**Existing controls observed:** backups encrypted in transit and at rest; stored in a separate Canadian region; nightly schedule.

| Risk ID | Risk | Inherent (L×I) | Residual (L×I) | Rating |
|---|---|---|---|---|
| SC-021 | Unauthorized access to backup copies | 3 × 5 = 15 | 2 × 5 = 10 | High |
| SC-022 | Slow or failed restore after a major incident | 3 × 5 = 15 | 2 × 5 = 10 | High |

#### Finding 5.2.8-A: Encryption keys are controlled by the supplier (SC-021)

- **Condition:** VaultSafe manages the encryption keys for Harborline's backups; Harborline does not hold them.
- **Criteria:** ISO/IEC 27001 Annex A 8.24 (use of cryptography).
- **Risk:** Anyone who compromises VaultSafe could potentially read backup copies of all production data.
- **Recommendation:** Move to customer-managed keys, so Harborline can revoke access and VaultSafe cannot decrypt the data alone.

#### Finding 5.2.8-B: No full restore has ever been performed (SC-022)

- **Condition:** Harborline has never performed a full restore from VaultSafe backups; the annual disaster recovery test restores only part of the data.
- **Criteria:** ISO/IEC 27001 Annex A 8.13 (information backup) and 5.30 (ICT readiness for business continuity).
- **Risk:** After an event such as ransomware, the restore could take far longer than planned or fail, leaving clinics without the platform for days.
- **Recommendation:** Run a full restore test within six months, record the time taken, and repeat annually.

### 5.2.9 S-12 Open-source components (Tier 2)

| Item | Detail |
|---|---|
| Service | Libraries and frameworks used within the platform |
| Data or access | Run inside Harborline's own code |
| Evidence reviewed | Interview with the engineering lead; repository security alert settings. No software bill of materials (SBOM) exists |

**Existing controls observed:** automated vulnerability alerts enabled in the code repository; code review before merging changes.

| Risk ID | Risk | Inherent (L×I) | Residual (L×I) | Rating |
|---|---|---|---|---|
| SC-023 | A known vulnerability in a library is exploited in production | 4 × 5 = 20 | 3 × 5 = 15 | High |
| SC-024 | A malicious or compromised library is introduced | 3 × 5 = 15 | 3 × 5 = 15 | High |
| SC-025 | An unmaintained library has no fix available when needed | 3 × 3 = 9 | 3 × 3 = 9 | Medium |

#### Finding 5.2.9-A: No structured inventory of software components (SC-023, SC-025)

- **Condition:** The platform uses about 450 third-party libraries, direct and indirect, with no SBOM. About 40 have had no release in over two years.
- **Criteria:** ISO/IEC 27001 Annex A 5.9 (inventory of assets) and 5.21 (managing the ICT supply chain); NIST SP 800-161.
- **Risk:** When a new vulnerability is announced, Harborline cannot quickly tell whether it is affected, and unmaintained libraries may never receive a fix.
- **Recommendation:** Generate an SBOM automatically in the build process, store it, and review the list of unmaintained libraries each quarter.

#### Finding 5.2.9-B: Vulnerability alerts have no owner or deadline (SC-023)

- **Condition:** Automated alerts are enabled, but no one is named as responsible for them and there is no deadline for fixing issues.
- **Criteria:** ISO/IEC 27001 Annex A 8.8 (management of technical vulnerabilities).
- **Risk:** Alerts can sit unaddressed, leaving known weaknesses open in production.
- **Recommendation:** Name an owner and set fix deadlines by severity (for example, critical within 7 days, high within 30 days).

#### Finding 5.2.9-C: No approval process for adding new libraries (SC-024)

- **Condition:** Developers can add new libraries without review of their source, maintenance, or reputation.
- **Criteria:** ISO/IEC 27001 Annex A 5.21 and 8.28 (secure coding).
- **Risk:** A malicious or typo-squatted library (a fake package with a name close to a real one) could enter the platform unnoticed.
- **Recommendation:** Introduce a lightweight approval step for new dependencies, with an approved-sources list and automated scanning.

## 5.3 Light-Touch Review (Tier 3 and 4)

| Risk ID | Supplier | Tier | Risk | Inherent | Residual | Rating | Note |
|---|---|---|---|---|---|---|---|
| SC-026 | S-09 InsightLoop Analytics | 3 | Exposure or re-identification of usage data | 3 × 2 = 6 | 2 × 2 = 4 | Low | User identifiers are hashed before sending, but usage events include IP addresses and de-identification has not been independently verified. Recommend removing IP addresses from events and verifying the de-identification method. |
| SC-027 | S-11 TerraTech Hardware Supply | 4 | Tampered or counterfeit hardware | 2 × 2 = 4 | 2 × 2 = 4 | Low | Devices ship directly to Harborline IT and are configured and encrypted before issue. No material gaps. |

<details>
<summary>Notes</summary>
<p>
Inherent vs. residual in practice. SC-004, SC-009, and SC-023 started at 20 (Critical), but existing controls (MFA, code review, automated alerts) lowered the likelihood to 3. That's why they're High now. Under your 3.5 rules, decisions are based on the residual score, so these go to the CISO, not the Risk Committee.

Residual equals inherent when nothing helps. SC-012 stays at 16 because Meridian has no control over repository access. Example of the opposite: SC-019 (PayBridge outage) falls from 9 to 6 because PayBridge's strong controls reduce likelihood. Reading a table, the gap between the two numbers tells you how well controls are working.

The impact override applies. Under 3.5.3, any risk with impact 5 is reviewed by the CISO regardless of rating. Eight risks score impact 5: SC-001, SC-004, SC-007, SC-009, SC-021, SC-022, SC-023, SC-024. All of them are already High, so the override changes nothing in practice. It would matter only if a likelihood-1 risk with impact 5 appeared.

PayBridge shows balance. It has two Medium risks and no gap on the supplier's side, which keeps the report from reading as "every vendor is terrible."

Findings trace back to risks. Each finding names its risk ID, so a reader can go from a recommendation to a score to the register. Keep that habit. When you build Section 6, every risk ID must appear exactly once in the register.

Wording check. The "Criteria" lines cite ISO 27001 Annex A control numbers. Verify each one against the standard when you finalize, since you'll be asked about them in an interview.
</p>
</details>


## 5.4 Cross-Cutting Themes

Several findings in Section 5.2 share a common cause. Six themes are described below. Together they indicate that the main weaknesses lie in how Harborline manages suppliers across their lifecycle, rather than in any single supplier.

### Theme 1: Inconsistent incident notification terms

- **Observation:** Suppliers' contractual commitments to notify Harborline of a security incident vary widely.
- **Evidence:** Of the nine suppliers with notification terms, two (GateKey Identity, PayBridge Processing) commit to 24 hours; five (CumulusPeak Cloud, ClearView Video API, VaultSafe Backup, Meridian Dev Studio, InsightLoop Analytics) commit to 72 hours; SentryOps Managed Services must notify "promptly" with no time limit; PingRelay Messaging has no notification clause. Related findings: SC-003, SC-005, SC-013, SC-017.
- **Root cause:** Harborline has no standard set of security terms that every supplier contract must include.
- **Implication:** Some clinic contracts require Harborline to notify clinics within 48 hours. Seven suppliers' terms do not support that commitment.

### Theme 2: Limited oversight and out-of-date assurance

- **Observation:** Harborline has little ability to verify supplier controls after onboarding.
- **Evidence:** No right-to-audit clause (SentryOps, Meridian); assurance report older than 12 months (GateKey, SC-008); weaker Type I report only (PingRelay, SC-017); no independent assurance at all (Meridian, SC-013); no tracking of attestation expiry dates (PayBridge, SC-020).
- **Root cause:** Suppliers are reviewed when they are onboarded but not again afterwards, and expiry dates for assurance reports are not tracked.
- **Implication:** Harborline may rely on evidence that no longer reflects a supplier's current controls.

### Theme 3: Single points of failure with no fallback

- **Observation:** Several suppliers support functions that Harborline cannot continue without, and no alternative arrangement exists.
- **Evidence:** No emergency access if GateKey fails (SC-006); no alternative video provider (SC-015); no backup messaging provider (SC-018); disaster recovery tests that do not cover a hosting-region failure (SC-002) or a full restore (SC-022).
- **Root cause:** Continuity planning does not extend to critical suppliers, and the annual disaster recovery test covers only part of the platform.
- **Implication:** A single supplier outage could stop care at many clinics for longer than Harborline expects.

### Theme 4: Privileged and broad access that is not tightly controlled

- **Observation:** Suppliers hold more access than they need, or access that is not individually accountable.
- **Evidence:** Shared administrator accounts (SentryOps, SC-004); write access to the main repository for all contractors and no removal process for leavers (Meridian, SC-012); unmanaged personal laptops (Meridian, SC-010); backup encryption keys held by the supplier (VaultSafe, SC-021).
- **Root cause:** Supplier access is reviewed informally rather than on a fixed schedule, and there is no standard for how suppliers connect to Harborline systems.
- **Implication:** Privileged access is a direct route to patient data, and without individual accountability Harborline cannot investigate misuse.

### Theme 5: Limited visibility of where data goes and how long it is kept

- **Observation:** Harborline does not have a clear picture of how its suppliers handle patient-related data.
- **Evidence:** Possible call relay outside Canada and no sub-processor list (ClearView, SC-014); 24-month message log retention and undisclosed SMS carriers (PingRelay, SC-016); production-derived data in the test environment (Meridian, SC-011); IP addresses in analytics data (InsightLoop, SC-026).
- **Root cause:** There is no record of sub-processors, data locations, or retention periods for each supplier.
- **Implication:** Harborline cannot confirm to clinics where their patients' data is, or demonstrate that it is kept only as long as necessary.

### Theme 6: Software supply chain controls are immature

- **Observation:** Harborline cannot see or control what third-party code runs inside its platform.
- **Evidence:** No software bill of materials for about 450 libraries; alerts without an owner or fix deadline; no approval step for new libraries (open-source components, SC-023 to SC-025); contractor code introduced without contractual secure-coding requirements (Meridian, SC-009).
- **Root cause:** Dependency management is left to individual developers without a defined process.
- **Implication:** When a new vulnerability is announced in a widely used library, Harborline cannot quickly tell whether it is affected.

### Summary of root causes

| Root cause | Themes affected | Current practice it reflects (Section 2.6) |
|---|---|---|
| No standard contract baseline for suppliers | 1, 2, 5 | Contract terms vary by supplier |
| No review of suppliers after onboarding | 2, 3 | Questionnaires sent at onboarding only |
| No continuity planning for critical suppliers | 3 | Annual disaster recovery test is partial |
| Informal access governance | 4 | Supplier access reviewed informally |
| No inventory of data flows and software components | 5, 6 | No structured component inventory; no sub-processor record |

These root causes are addressed in the treatment plan in Section 8.

## 5.5 Industry Incident Reference Cases

The following publicly reported incidents illustrate the types of risk identified in this assessment. They are included to show that these risks are not theoretical and are not a comparison with any Harborline supplier.

| Incident | What happened | Lesson | Related Harborline risks |
|---|---|---|---|
| **Okta customer support breach (2023)** | An attacker used stolen credentials to access Okta's customer support case system and obtained files customers had uploaded, some containing session tokens. Several Okta customers were targeted afterwards. | Identity providers are high-value targets, and data shared with a supplier's support team can itself be a route in. | SC-006, SC-007 (GateKey) |
| **Kaseya VSA ransomware (2021)** | Attackers exploited vulnerabilities in Kaseya's remote management software and used it to deploy ransomware to customers of managed service providers. | A provider's own management tools can become a route into all of its customers. | SC-004, SC-005 (SentryOps) |
| **Change Healthcare ransomware (2024)** | A ransomware attack on a major US healthcare technology provider disrupted claims and payment processing across much of the US health system for weeks. Reporting indicated attackers entered through a remote access system without multi-factor authentication. | Heavy dependence on one provider can turn a single supplier incident into an industry-wide outage. | SC-002, SC-015, SC-018 |
| **MOVEit Transfer and BORN Ontario (2023)** | A vulnerability in a widely used file transfer product was exploited, affecting many organizations. Ontario's BORN registry, which holds maternal and newborn health data, reported that the health information of about 3.4 million people was affected. | Health data in Ontario can be exposed through a third-party tool, creating privacy-regulator and public attention. | SC-003, SC-005, SC-017 |
| **Target data breach (2013)** | Attackers entered Target's network using credentials stolen from a refrigeration and HVAC contractor, and later reached payment systems. | A supplier's access credentials can be a way in, even when the supplier has nothing to do with the data that is stolen. | SC-010, SC-012 (Meridian) |
| **Log4Shell (2021) and xz Utils (2024)** | A critical flaw in the widely embedded Log4j library left many organizations unable to tell quickly whether they used it. Separately, a hidden backdoor was planted in the xz compression library over a long period and found before wide release. | Without an inventory of components, vulnerabilities are hard to locate. Trust in open-source maintainers can also be exploited. | SC-023, SC-024, SC-025 (open-source components) |

<details>
<summary>Notes</summary>
<p>
Checks before you commit
 Every risk ID mentioned exists in 5.2 and 5.3
 Themes 1 to 6 numbers match the evidence sheet
 Every real incident has a source in Appendix E
 No claim about a real company goes beyond what the source states

</p>
</details>

*Sources are listed in Appendix E.*

