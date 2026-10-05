
# 6. Risk Register and Heat Map

This section consolidates the 27 risks identified in Section 5. Scores follow the model in Section 3.4 and ratings follow the thresholds in Section 3.5. Treatment decisions shown here are proposed and are developed in Section 8.

## 6.1 Risk Register

The register is sorted by residual score, highest first. Ratings are based on the residual score.

| Risk ID | Supplier | Tier | Risk | Inherent | Residual | Rating | Proposed treatment | Proposed owner |
|---|---|---|---|---|---|---|---|---|
| SC-012 | S-07 Meridian Dev Studio | 1 | Excessive and lingering access to the code repository | 4 × 4 = 16 | 4 × 4 = 16 |  High | Mitigate | CISO |
| SC-004 | S-05 SentryOps Managed Services | 1 | Misuse or compromise of privileged access | 4 × 5 = 20 | 3 × 5 = 15 | High | Mitigate | CISO |
| SC-009 | S-07 Meridian Dev Studio | 1 | Malicious or vulnerable code introduced into production | 4 × 5 = 20 | 3 × 5 = 15 |  High | Mitigate | CISO |
| SC-023 | S-12 Open-source components | 2 | Known library vulnerability exploited in production | 4 × 5 = 20 | 3 × 5 = 15 |  High | Mitigate | Director of IT Operations |
| SC-024 | S-12 Open-source components | 2 | Malicious or compromised library introduced | 3 × 5 = 15 | 3 × 5 = 15 | High | Mitigate | Director of IT Operations |
| SC-010 | S-07 Meridian Dev Studio | 1 | Credential theft through unmanaged personal laptops | 4 × 4 = 16 | 3 × 4 = 12 | High | Mitigate | Director of IT Operations |
| SC-016 | S-03 PingRelay Messaging | 2 | Exposure of retained patient contact and appointment data | 4 × 4 = 16 | 3 × 4 = 12 |  High | Mitigate | Privacy Officer |
| SC-001 | S-01 CumulusPeak Cloud | 1 | Unauthorized access to production data via a compromised administrator account | 3 × 5 = 15 | 2 × 5 = 10 |  High | Accept (CISO approval) | CISO |
| SC-007 | S-06 GateKey Identity | 1 | Compromise of the identity provider leads to unauthorized access | 3 × 5 = 15 | 2 × 5 = 10 |  High | Accept (CISO approval) | CISO |
| SC-021 | S-08 VaultSafe Backup | 2 | Unauthorized access to backup copies | 3 × 5 = 15 | 2 × 5 = 10 |  High | Mitigate | Director of IT Operations |
| SC-022 | S-08 VaultSafe Backup | 2 | Slow or failed restore after a major incident | 3 × 5 = 15 | 2 × 5 = 10 | High | Mitigate | Director of IT Operations |
| SC-003 | S-01 CumulusPeak Cloud | 1 | Late notification of a security incident | 3 × 3 = 9 | 3 × 3 = 9 |  Medium | Mitigate | Director of Procurement |
| SC-005 | S-05 SentryOps Managed Services | 1 | Late notification of a security incident | 3 × 3 = 9 | 3 × 3 = 9 |  Medium | Mitigate | Director of Procurement |
| SC-011 | S-07 Meridian Dev Studio | 1 | Exposure of production-derived data in the test environment | 3 × 4 = 12 | 3 × 3 = 9 |  Medium | Mitigate | Director of IT Operations |
| SC-013 | S-07 Meridian Dev Studio | 1 | Missing contractual safeguards and independent assurance | 3 × 3 = 9 | 3 × 3 = 9 |  Medium | Mitigate | Director of Procurement |
| SC-015 | S-02 ClearView Video API | 2 | Outage halts virtual visits | 3 × 3 = 9 | 3 × 3 = 9 |  Medium | Mitigate | Director of IT Operations |
| SC-017 | S-03 PingRelay Messaging | 2 | Late or no notification of a security incident | 3 × 3 = 9 | 3 × 3 = 9 |  Medium | Mitigate | Director of Procurement |
| SC-018 | S-03 PingRelay Messaging | 2 | Reminder service outage | 3 × 3 = 9 | 3 × 3 = 9 |  Medium | Mitigate | Director of IT Operations |
| SC-025 | S-12 Open-source components | 2 | Unmaintained library has no fix available when needed | 3 × 3 = 9 | 3 × 3 = 9 |  Medium | Mitigate | Director of IT Operations |
| SC-002 | S-01 CumulusPeak Cloud | 1 | Extended outage caused by a hosting provider failure | 3 × 4 = 12 | 2 × 4 = 8 |  Medium | Mitigate | Director of IT Operations |
| SC-006 | S-06 GateKey Identity | 1 | Login outage locks staff and clinics out of the platform | 3 × 4 = 12 | 2 × 4 = 8 |  Medium | Mitigate | Director of IT Operations |
| SC-014 | S-02 ClearView Video API | 2 | Patient data handled outside Canada by unknown sub-processors | 3 × 4 = 12 | 2 × 4 = 8 | Medium | Mitigate | Privacy Officer |
| SC-008 | S-06 GateKey Identity | 1 | Control weaknesses undetected because assurance evidence is out of date | 3 × 3 = 9 | 2 × 3 = 6 |  Medium | Mitigate | Director of Procurement |
| SC-019 | S-04 PayBridge Processing | 2 | Payment processing outage | 3 × 3 = 9 | 2 × 3 = 6 |  Medium | Accept (Head of GRC approval) | Director of IT Operations |
| SC-020 | S-04 PayBridge Processing | 2 | Lapse in PCI compliance evidence goes unnoticed | 3 × 2 = 6 | 3 × 2 = 6 |  Medium | Mitigate | Director of Procurement |
| SC-026 | S-09 InsightLoop Analytics | 3 | Exposure or re-identification of usage data | 3 × 2 = 6 | 2 × 2 = 4 |  Low | Mitigate | Privacy Officer |
| SC-027 | S-11 TerraTech Hardware Supply | 4 | Tampered or counterfeit hardware | 2 × 2 = 4 | 2 × 2 = 4 |  Low | Accept (risk owner) | Director of IT Operations |

## 6.2 Heat Maps

Each cell shows the risk numbers placed there (the "SC-" prefix is omitted). Colours follow the bands in Section 3.5.


### 6.2.1 Inherent risk (before controls)

Each cell shows the rating for that likelihood and impact combination. Where risks fall in a cell, the rating is in bold, followed by the risk numbers (the "SC-" prefix is omitted).

| Likelihood ↓ / Impact → | 1 Negligible | 2 Minor | 3 Moderate | 4 Major | 5 Severe |
|---|---|---|---|---|---|
| **5 Almost certain** | Medium | High | High | Critical | Critical |
| **4 Likely** | Low | Medium | High | **High:** 010, 012, 016 | **Critical:** 004, 009, 023 |
| **3 Possible** | Low | **Medium:** 020, 026 | **Medium:** 003, 005, 008, 013, 015, 017, 018, 019, 025 | **High:** 002, 006, 011, 014 | **High:** 001, 007, 021, 022, 024 |
| **2 Unlikely** | Low | **Low:** 027 | Medium | Medium | High |
| **1 Rare** | Low | Low | Low | Low | Medium |

### 6.2.2 Residual risk (after existing controls)

| Likelihood ↓ / Impact → | 1 Negligible | 2 Minor | 3 Moderate | 4 Major | 5 Severe |
|---|---|---|---|---|---|
| **5 Almost certain** | Medium | High | High | Critical | Critical |
| **4 Likely** | Low | Medium | High | **High:** 012 | Critical |
| **3 Possible** | Low | **Medium:** 020 | **Medium:** 003, 005, 011, 013, 015, 017, 018, 025 | **High:** 010, 016 | **High:** 004, 009, 023, 024 |
| **2 Unlikely** | Low | **Low:** 026, 027 | **Medium:** 008, 019 | **Medium:** 002, 006, 014 | **High:** 001, 007, 021, 022 |
| **1 Rare** | Low | Low | Low | Low | Medium |

Existing controls moved risks mainly to the left (lower likelihood). Impact stayed the same for 26 of the 27 risks; the one exception is SC-011, where partial masking of test data lowers the impact from Major to Moderate.

## 6.3 Summary Views

### 6.3.1 Risks by rating

| Rating | Inherent | Residual |
|---|---|---|
| Critical (17-25) | 3 | 0 |
| High (10-16) | 12 | 11 |
| Medium (5-9) | 11 | 14 |
| Low (1-4) | 1 | 2 |
| **Total** | **27** | **27** |

### 6.3.2 Risks by supplier

| Supplier | Tier | Risks | Highest residual score | Rating |
|---|---|---|---|---|
| S-07 Meridian Dev Studio | 1 | 5 | 16 |  High |
| S-05 SentryOps Managed Services | 1 | 2 | 15 |  High |
| S-12 Open-source components | 2 | 3 | 15 |  High |
| S-03 PingRelay Messaging | 2 | 3 | 12 |  High |
| S-01 CumulusPeak Cloud | 1 | 3 | 10 |  High |
| S-06 GateKey Identity | 1 | 3 | 10 |  High |
| S-08 VaultSafe Backup | 2 | 2 | 10 |  High |
| S-02 ClearView Video API | 2 | 2 | 9 | Medium |
| S-04 PayBridge Processing | 2 | 2 | 6 | Medium |
| S-09 InsightLoop Analytics | 3 | 1 | 4 | Low |
| S-11 TerraTech Hardware Supply | 4 | 1 | 4 | Low |

### 6.3.3 Key observations

- No risk is rated Critical after controls. Three risks (SC-004, SC-009, SC-023) were Critical before controls and fall to High.
- Eleven risks are rated High: six relate to Tier 1 suppliers and five to Tier 2 suppliers. None relate to Tier 3 or 4.
- Meridian Dev Studio carries the highest residual score (SC-012, 16) and the most risks (5), three of them rated High.
- Existing controls reduced the score of 16 risks. The other 11 are unchanged because no current control reduces them, including two High risks (SC-012 and SC-024).
- Eight risks have a Severe impact (SC-001, SC-004, SC-007, SC-009, SC-021, SC-022, SC-023, SC-024) and are reviewed by the CISO under Section 3.5.3.
- Two High risks (SC-001, SC-007) are proposed for acceptance because existing controls meet expectations. Under Section 3.5.2, accepting a High risk requires CISO approval.

<details>
  <summary>Notes</summary>
  <p>Each cell comes from the risk's inherent score in the register, which is likelihood × impact.

Example, SC-016: inherent is 4 × 4, so likelihood 4 (row "4 Likely") and impact 4 (column "4 Major"), which is the cell showing High: 010, 012, 016. Its score of 16 sits in the High band (10 to 16).

Do this for any risk and confirm it appears in exactly one cell. Then run these checks:

Count: the risk numbers across all cells should add up to 27. Here the cells hold 3 + 3 + 3 + 9 + 4 + 5 + 2 + 1 = 30 minus the three I counted twice in the row 4 and row 3 groups? No, the simple way is by row: row 4 has 6 risks, row 3 has 20, row 2 has 1, and 6 + 20 + 1 = 27.
Ratings by cell: the three Critical risks (004, 009, 023) are the only ones scoring 20. All three are likelihood 4 × impact 5.
Summary table: it must match 6.3.1, which shows inherent counts of 3 Critical, 12 High, 11 Medium, and 1 Low. In this map, High is 3 + 4 + 5 = 12, Medium is 9 + 2 = 11, and Low is 1.</p>
</details>
