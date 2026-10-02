<details>
  <summary>Notes</summary>
  <p>It defines the scoring rules, and every later section depends on it. Once it's written, don't change it mid-report, or your scores stop being comparable.</p>
</details> 


# 3. Methodology

## 3.1 Frameworks Used
This assessment uses three frameworks:
1. NIST SP-161 Rev 1(Cybersecurity Supply Chain Risk Management): guides how supplier risk is identified and assessed.
2. ISO/IEC 27001:2022, annex A(controls 5.19-5.23): the supplier relationship and supply-chain related controls.
3. NIST Cybersecurity Framework 2.0, Govern function: informs the governance and monitoring recommendations.
   
## 3.2 Assessment Approach
This assessment follows six steps:
1. Inventory all current suppliers supporting the patient platform.
2. Tier suppliers by criticality (Section 3.3).
3. Collect evidence through questionnaires and document review (contracts, security reports).
4. Identify risks for each supplier across four categories: cyber, privacy, continuity, and compliance.
5. Score risks for likelihood and impact (Section 3.4).
6. Analyze gaps and recommend treatment for each risk.

## 3.3 Supplier Tiering Criteria
<details>
  <summary>Notes</summary>
  <p>
Tiering means sorting suppliers into groups by how much they matter, so you spend the most effort on the ones that could hurt you most. Base it on two questions: **how badly would we suffer if this supplier failed**, and **how sensitive is the data or access they hold? ** 
  </p>
</details>

Suppliers are grouped into four tiers according to how much Harborline depends on them and how much sensitive data or access they hold. Tiering determines how much assessment effort each supplier receives.
| Tier | Label | Criteria (any one is sufficient) |
|---|---|---|
| 1 | Critical | The patient platform cannot operate without the supplier and no quick replacement exists; **or** the supplier has privileged administrative access to, or controls authentication for, production systems |
| 2 | High | A major platform function depends on the supplier; **or** the supplier stores or processes identifiable patient data, payment transactions, or source code; **or** the supplier's software runs inside the platform; **or** the supplier holds copies of production data |
| 3 | Medium | Disruption would be limited and workarounds exist; the supplier handles only de-identified or low-sensitivity data |
| 4 | Low | The supplier has no direct data or system access and is easily replaced |

### 3.3.1 Assessment depth by tier

| Tier | Assessment depth |
|---|---|
| 1 and 2 | Detailed assessment: full questionnaire, review of contracts and assurance reports, individual risk analysis |
| 3 and 4 | Light-touch review: short questionnaire and summary risk rating |

### 3.3.2 Judgment and overrides
Where a supplier's tier does not reflect its real importance, the assessor may adjust it, provided the reason is documented in the supplier inventory (Section 4).

**Illustrative example** (the full assessment of this supplier appears in Section 5)
- *CumulusPeak Cloud* hosts the entire platform, so it meets the Tier 1 operational criterion.
- *InsightLoop Analytics* receives only de-identified usage data and could be replaced without disrupting care, so it is **Tier 3**.

| Supplier  |  Tier  | Reason  |
| -------- | -------- | -------- |
| CumulusPeak Cloud |  1  |  Platform cannot run without it  |
| SentryOps Managed Services |  1  |  Privileged administrative access |
| GateKey Identity |  1  |  Controls authentication  |
| Meridian Dev Studio |  1 |  Access to source code  |
| ClearView Video API |  2  | Live patient traffic   |
| PingRelay Messaging |  2  |  Contains PII  |
| PayBridge Processing  |  2  |  handles payment transactions  |
| VaultSafe Backup  |  2  |  Has copies of production data  |
| Open-source components  |  2  | Software runs inside the platform |
| InsightLoop Analytics |  3 | De-identified data only  |
| TerraTech Hardware Supply | 4 | No direct data access  |

***De-identified data** refers to a dataset where all personally identifiable information (PII) has been removed, masked, or modified so that the remaining information cannot be easily linked back to a specific individual.*


## 3.4 Risk Scoring Model

Each supplier risk is scored using a 5×5 likelihood and impact model, so that risks can be compared consistently and prioritized.

**Risk score = Likelihood × Impact**

Each factor is rated from 1 to 5, producing a score between 1 and 25. Ratings are based on a 12-month outlook.

### 3.4.1 Likelihood Scale

| Score | Level | Description |
|---|---|---|
| 1 | Rare | Strong, verified controls; no relevant incident history; event not expected within 12 months |
| 2 | Unlikely | Good controls with minor gaps; event could occur but is not expected |
| 3 | Possible | Some controls missing or unverified; event could reasonably occur |
| 4 | Likely | Known weaknesses with no remediation planned; event probably will occur |
| 5 | Almost certain | Active weaknesses or repeated incidents; event is expected to occur |

### 3.4.2 Impact Scale

Impact is assessed across four dimensions. The overall impact score is the **highest** rating across the dimensions.

| Score | Level | Patient data and privacy | Service availability | Compliance and legal | Business and reputation |
|---|---|---|---|---|---|
| 1 | Negligible | No data exposed | Under 1 hour, non-critical feature | No regulatory interest | No customer notice |
| 2 | Minor | No identifiable data exposed | 1 to 4 hours of disruption | Internal policy breach only | Isolated customer complaints |
| 3 | Moderate | Limited exposure of personal data | 4 to 24 hours; some clinics affected | Reportable to a clinic customer | Several customers raise concerns |
| 4 | Major | Patient health data exposed for one or more clinics | 1 to 3 days of platform outage | Breach notification to regulator likely | Customers escalate; contract at risk |
| 5 | Severe | Large-scale exposure of patient health records | Over 3 days; clinics cannot see patients | Regulatory investigation or penalties (e.g. under PHIPA) | Loss of multiple clinic customers; public attention |

### 3.4.3 Risk Score Matrix

| Likelihood ↓ / Impact → | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| **5** | 5 | 10 |  15 | 20 |  25 |
| **4** |  4 | 8 | 12 |  16 | 20 |
| **3** | 3 |  6 |  9 | 12 |  15 |
| **2** |  2 | 4 |  6 |  8 |  10 |
| **1** |  1 | 2 | 3 |  4 |  5 |

### 3.4.4 Inherent and Residual Risk

- **Inherent risk** is the score before considering the controls currently in place at the supplier or at Harborline.
- **Residual risk** is the score after those controls are taken into account.

Both are recorded for each risk, so that the effect of existing controls is visible.

**Illustrative example** (the full assessment of this supplier appears in Section 5)
 CumulusPeak Cloud**
- *Risk:* unauthorized access to production patient data through a compromised administrator account.
- *Inherent:* Likelihood 3 (Possible) × Impact 5 (Severe) = **15 (High)**.
- *Controls considered:* MFA for administrators, encryption at rest, access logging.
- *Residual:* Likelihood 2 (Unlikely) × Impact 5 (Severe) = **10 (High)**.


## 3.5 Risk Rating Thresholds

Risk thresholds reflect Harborline's risk appetite, meaning the level of risk the organization is willing to accept. Because Harborline handles patient health information, its appetite for risk is low. The thresholds below convert each risk score into a rating and define the response expected at each level.

### 3.5.1 Rating Bands

| Score | Rating | Expected response | Escalation |
|---|---|---|---|
| 1-4 |  Low | Accept and monitor at the next scheduled supplier review | Risk owner |
| 5-9 | Medium | Treatment plan agreed and completed within 12 months | Head of GRC |
| 10-16 |  High | Treatment plan agreed within 60 days and completed within 6 months | CISO |
| 17-25 |  Critical | Treatment plan agreed within 30 days; interim safeguards put in place immediately | Risk Committee |

### 3.5.2 Risk Acceptance Authority

Accepting a risk means formally deciding to live with it instead of treating it. The higher the rating, the more senior the approver:

| Rating | May be accepted by |
|---|---|
| Low | Risk owner |
| Medium | Head of GRC |
| High | CISO |
| Critical | Risk Committee only |

### 3.5.3 Impact Override

Any risk with an impact rating of 5 (Severe) is reviewed by the CISO, regardless of its overall score. This ensures that unlikely but catastrophic events, such as a large-scale exposure of patient records, are not overlooked.

### 3.5.4 Application of Thresholds

- Thresholds are applied to both inherent and residual scores.
- Treatment and acceptance decisions are based on the **residual** score, as it reflects the risk remaining after existing controls.
- Rating bands are the same as those shown in the risk score matrix (Section 3.4.3) and the heat map (Section 6).

**Illustrative example:** a supplier risk with a residual score of 10 (Likelihood 2 × Impact 5) is rated High. A treatment plan must be agreed within 60 days, and because the impact is Severe, the CISO also reviews it under the override.


