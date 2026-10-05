## 5. Scope and carve-outs

### 5.1 Service scope: what the audit covers versus what Meridian needs

| Service component | Covered by the audit? | Meridian relies on it? | Assessment |
|---|---|---|---|
| 24/7 SOC monitoring | Yes (partially; see 5.2) | Yes, core service | Acceptable, with a caveat on overnight coverage |
| Endpoint telemetry collection and storage | Yes | Yes | Acceptable |
| Alert triage, investigation, and notification | Yes | Yes | Acceptable |
| **Automated Response module** (host isolation, process termination) | **No** | Yes, expected as part of "response" | **Gap** |
| **Customer Portal mobile app** | **No** | Likely (alerts and approvals) | **Gap** |
| Privacy practices | **No** (criterion not included) | Yes (employee data, including EU staff) | **Gap** |

### 5.2 Subservice organizations (carve-out method)

| Subservice organization | Function | Tested in this report? | Why it matters to Meridian |
|---|---|---|---|
| Public cloud provider | Hosts and stores all telemetry (US-East region) | No | All Meridian activity data lives here; data location is relevant to EU staff |
| Threat intelligence data provider | Supplies indicator feeds used for detection | No | Poor or tampered feeds could weaken detection |
| Overnight SOC staffing partner | Tier 1 analyst coverage, 22:00 to 06:00 UTC | No | One third of daily monitoring is performed by a party outside the audit |

### 5.3 Scope conclusion
The audit supports VigilGrid's core monitoring and investigation services but does not cover two features Meridian is likely to depend on: the Automated Response module and the mobile app. The Automated Response module is the more significant gap. It was released in December 2025, during the audit period, yet it is excluded from the system description, so a feature with the power to isolate Meridian's devices has no independent assurance behind it.

The carve-out of the overnight staffing partner also matters. Roughly a third of each day's monitoring is performed by this partner, and Section 6 shows that VigilGrid never completed a risk assessment of it. Meridian therefore has no evidence, from the audit or from VigilGrid's own oversight, of how overnight alerts are handled.

**Actions required:**
1. Ask VigilGrid whether Meridian can use the service without the Automated Response module and mobile app, or require the next report to cover them.
2. Request the overnight staffing partner's own assurance (a SOC 2 report or equivalent) and a description of the access its analysts have to customer data.
3. Request the cloud provider's and threat feed provider's assurance reports, or confirm VigilGrid reviews them.
4. Confirm the data hosting region and the transfer mechanism for EU employee data (addressed under Section 8).
