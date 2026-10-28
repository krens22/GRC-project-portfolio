## Crosswalk Table

Ratings: **D = Direct** (the control directly addresses the requirement) and **S = Supporting** (it helps, but the requirement expects more).

### Batch 1

| # | Control | SOC 2 (2017 TSC) | ISO 27001:2022 | PCI DSS v4.0.1 | GDPR |
|---|---|---|---|---|---|
| 1 | Access control: only authorized people can access systems and data, based on job need | CC6.1, CC6.2, CC6.3 (D) | A.5.15, A.5.18, A.8.2, A.8.3 (D) | Req 7, Req 8 (D) | Art. 32 (S) |
| 2 | Multi-factor authentication (MFA) | CC6.1, CC6.6 (D) | A.8.5 (D) | Req 8.4 (D) | Art. 32 (S) |
| 3 | Encryption of data at rest and in transit | CC6.1, CC6.7 (D) | A.8.24 (D) | Req 3, Req 4 (D) | Art. 32(1)(a) (D) |
| 4 | Logging and monitoring of system activity | CC7.2, CC7.3 (D) | A.8.15, A.8.16 (D) | Req 10 (D) | Art. 32, Art. 33 (S) |

#### What each reference means

**Control 1, access control**
- *SOC 2:* CC6.1 is the general rule about restricting access, CC6.2 covers approving and setting up user accounts, and CC6.3 covers giving people only the access their role needs and removing it when they leave.
- *ISO:* A.5.15 is the access control policy, A.5.18 covers granting and reviewing access rights, A.8.2 covers extra care for admin accounts, and A.8.3 covers restricting who can reach specific information.
- *PCI:* Requirement 7 is "need to know" access to card data, and Requirement 8 is identifying and authenticating each user.
- *GDPR:* Article 32 requires appropriate security for personal data. It doesn't mention access control by name, so this is Supporting.

**Control 2, MFA**
- *SOC 2:* CC6.1 covers authentication, and CC6.6 covers protecting access from outside the network, such as remote logins.
- *ISO:* A.8.5 is secure authentication, which is where MFA belongs in the 2022 version.
- *PCI:* Requirement 8.4 specifically requires MFA, for example for all access into the card data environment and for remote access.
- *GDPR:* Article 32 again, Supporting, since it never names MFA.

**Control 3, encryption**
- *SOC 2:* CC6.1 includes protecting stored data, and CC6.7 covers protecting data while it's being sent or moved.
- *ISO:* A.8.24 is the use of cryptography.
- *PCI:* Requirement 3 protects stored card data, and Requirement 4 protects it in transit over open networks.
- *GDPR:* This is the one place GDPR is explicit. Article 32(1)(a) names "pseudonymisation and encryption" as example measures, so it is rated D.

**Control 4, logging and monitoring**
- *SOC 2:* CC7.2 covers watching systems for unusual activity, and CC7.3 covers evaluating those events to decide if they are incidents.
- *ISO:* A.8.15 is logging, and A.8.16 is monitoring activities.
- *PCI:* Requirement 10 is entirely about logging and monitoring access.
- *GDPR:* Article 32 supports it, and Article 33 requires reporting a breach within 72 hours, which is impossible if you can't detect one. That is an indirect link, so it's Supporting.


### Batch 2

| # | Control | SOC 2 (2017 TSC) | ISO 27001:2022 | PCI DSS v4.0.1 | GDPR |
|---|---|---|---|---|---|
| 5 | Incident response: a plan to detect, respond to, and recover from security incidents | CC7.3, CC7.4, CC7.5 (D) | A.5.24, A.5.25, A.5.26, A.5.27, A.6.8 (D) | Req 12.10 (D) | Art. 33, Art. 34 (D) |
| 6 | Vendor (third-party) management: assessing and monitoring suppliers that handle your data | CC9.2 (D) | A.5.19, A.5.20, A.5.21, A.5.22 (D) | Req 12.8, 12.9 (D) | Art. 28 (D) |
| 7 | Backup and recovery of data | A1.2, A1.3 (D) | A.8.13, A.5.30 (D) | Req 9.4.1, 12.10.1 (S) | Art. 32(1)(c) (D) |
| 8 | Change management: changes to systems are approved, tested, and documented | CC8.1 (D) | A.8.32, A.8.9 (D) | Req 6.5 (D) | Art. 25, Art. 32 (S) |

#### What each reference means

**Control 5, incident response**
- *SOC 2:* CC7.3 evaluates security events to decide whether they are incidents, CC7.4 covers responding to confirmed incidents, and CC7.5 covers recovering from them.
- *ISO:* A.5.24 is planning and preparation, A.5.25 is deciding whether an event is an incident, A.5.26 is the response itself, A.5.27 is learning from incidents afterward, and A.6.8 is how staff report events.
- *PCI:* Requirement 12.10 requires a documented incident response plan and the ability to act on it immediately.
- *GDPR:* Article 33 requires notifying the authority within 72 hours of a personal data breach, and Article 34 covers telling affected individuals. Your incident process is how a company meets these deadlines, so it is rated D.

**Control 6, vendor management**
- *SOC 2:* CC9.2 is the criterion about assessing and managing risks from vendors and business partners.
- *ISO:* A.5.19 to A.5.22 cover security in supplier relationships, security terms in supplier contracts, the ICT supply chain, and monitoring supplier services.
- *PCI:* Requirement 12.8 covers managing third-party service providers, and 12.9 covers those providers' responsibility to support your compliance.
- *GDPR:* Article 28 says that if a company uses a vendor to process personal data (a "processor"), it needs a written contract and must choose vendors with sufficient safeguards. This one is explicit.

**Control 7, backup and recovery**
- *SOC 2:* A1.2 covers environmental protections and data backup processes, and A1.3 covers testing recovery procedures. These sit in the Availability category.
- *ISO:* A.8.13 is information backup, and A.5.30 is ICT readiness for business continuity.
- *PCI:* PCI DSS has no general backup requirement. Requirement 9.4.1 only covers securing offline backup media that contains card data, and 12.10.1 requires the incident response plan to include data backup processes. That's why it's S.
- *GDPR:* Article 32(1)(c) explicitly names the "ability to restore the availability and access to personal data in a timely manner" after an incident, so it's D.

**Control 8, change management**
- *SOC 2:* CC8.1 covers authorizing, testing, approving, and documenting changes.
- *ISO:* A.8.32 is change management, and A.8.9 is configuration management (keeping systems in a known, approved state).
- *PCI:* Requirement 6.5 covers managing changes to system components securely, including approval and testing.
- *GDPR:* No article is about change management. Article 32 (security) and Article 25 (data protection by design) support it, so it's S.

### Batch 3

| # | Control | SOC 2 (2017 TSC) | ISO 27001:2022 | PCI DSS v4.0.1 | GDPR |
|---|---|---|---|---|---|
| 9 | Vulnerability management: regularly finding, ranking, and fixing weaknesses in systems | CC7.1 (D) | A.8.8 (D) | Req 6.3, Req 11.3 (D) | Art. 32(1)(d) (S) |
| 10 | Security awareness training for staff | CC1.4, CC2.2 (D) | A.6.3 (D) | Req 12.6 (D) | Art. 32(4), Art. 39(1)(b) (S) |

#### What each reference means

**Control 9, vulnerability management**
- *SOC 2:* CC7.1 covers having procedures to detect new vulnerabilities and unexpected configuration changes. It's in the Security category, so your scope stays consistent.
- *ISO:* A.8.8 is management of technical vulnerabilities. It's a very direct match: find them, assess the risk, and act.
- *PCI:* Requirement 6.3 covers identifying security vulnerabilities and fixing them (including installing critical patches quickly), and Requirement 11.3 covers regular vulnerability scans. *Example:* running a monthly scan with a tool like Nessus and patching the critical findings.
- *GDPR:* Article 32(1)(d) asks for a process for "regularly testing, assessing and evaluating" how well your security measures work. Vulnerability scanning is one way to do that, but the article never mentions vulnerabilities or patching, so it is rated S.

**Control 10, security awareness training**
- *SOC 2:* CC1.4 is about attracting and developing competent people, and CC2.2 covers communicating to staff what their security responsibilities are.
- *ISO:* A.6.3 is information security awareness, education, and training.
- *PCI:* Requirement 12.6 requires an ongoing security awareness program for all personnel. *Example:* annual training plus phishing simulations.
- *GDPR:* Article 32(4) says people working under your authority should only process personal data on your instructions, and Article 39(1)(b) lists staff awareness and training as a task of the Data Protection Officer (DPO), if you have one. It's indirect, so S.
