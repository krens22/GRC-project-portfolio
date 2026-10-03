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
> **Classification:** Confidential | **Version:** 0.1 | **Document ID:** HHS-GRC-TPRM-001

# 5. Risk Assessment Findings

This section presents the risks identified for each in-scope supplier. Tier 1 and Tier 2 suppliers are assessed in detail (Section 5.2); Tier 3 and Tier 4 suppliers receive a light-touch review (Section 5.3). Risks are scored using the model in Section 3.4 and rated using the thresholds in Section 3.5. Each finding states the condition observed, the standard it is measured against, the resulting risk, and a recommendation.

## 5.1 Summary of Results

<Complete after all suppliers are assessed: a table of risks by rating, and the top risks.>

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
### 5.2.3 S-06 GateKey Identity (Tier 1)
### 5.2.4 S-07 Meridian Dev Studio (Tier 1)
### 5.2.5 S-02 ClearView Video API (Tier 2)
### 5.2.6 S-03 PingRelay Messaging (Tier 2)
### 5.2.7 S-04 PayBridge Processing (Tier 2)
### 5.2.8 S-08 VaultSafe Backup (Tier 2)
### 5.2.9 S-12 Open-source components (Tier 2)
## 5.3 Light-Touch Review (Tier 3 and 4)
## 5.4 Cross-Cutting Themes
## 5.5 Industry Incident Reference Cases
