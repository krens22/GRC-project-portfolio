## 6. Exceptions

### 6.1 Summary of exceptions

| Ref | Control | What the auditor found | Severity | Management response |
|---|---|---|---|---|
| CC6.3 | Access removed within 24 hours of termination | 2 of 25 sampled terminations had access removed after 5 and 9 days (the qualified-opinion item) | **High** | Partially credible |
| CC6.2 | Quarterly review of privileged access to the production SOC console | Not performed in either quarter of the period (Q4 2025, Q1 2026) | **High** | Not credible |
| CC9.2 | Annual risk assessment of subservice organizations | No assessment completed for the overnight SOC staffing partner | **High** | Partially credible |
| CC8.1 | Peer review of changes to detection rules and code | 1 of 40 sampled changes was an emergency change released without peer review | **Medium** | Partially credible |

### 6.2 Analysis of each exception

**CC6.3: Delayed access removal (High).**
Two of 25 sampled terminations kept access for 5 and 9 days against a 24-hour policy, a failure rate of 8% in the sample. Because the auditor only tested a sample of 61 terminations, other late removals may exist. The risk to Meridian is that a former contractor could retain access to systems that hold telemetry from every customer, including Meridian. Management attributes the delays to tickets routed to the wrong queue and states no unauthorized activity was identified, but it provides no evidence of how that was determined (such as a log review). Management's fix is also unstated: the response says the accounts were disabled, but not what changed to stop the misrouting. *Rating: partially credible.*

**CC6.2: Missed privileged access reviews (High).**
The quarterly review of who holds administrator access to the SOC console did not happen in either quarter of the period. This is a complete control failure, not an occasional lapse. It also compounds the CC6.3 failure: access reviews are the safety net that would catch someone whose access wasn't removed on time, and with both controls failing, nothing was positioned to catch a lingering account. Management cites "informal spot checks," but these are undocumented and the auditor still recorded an exception, which suggests they did not meet the standard of the control. The cause given is staff turnover, which is a reason but not a fix. *Rating: not credible.*

**CC9.2: No assessment of the overnight staffing partner (High).**
VigilGrid never assessed the risk of the partner that covers 22:00 to 06:00 UTC, one third of each day's monitoring. This exception links to Section 5: the partner is both carved out of the audit and unreviewed by VigilGrid, so no one has evidence of its controls. Management states the assessment is scheduled for Q3 2026. Q3 ended on September 30, so it should now be complete, and a clear follow-up is to ask for the finished assessment. *Rating: partially credible, pending evidence of completion.*

**CC8.1: Emergency change without peer review (Medium).**
One of 40 sampled changes to detection rules or code was released without peer review. Detection rules decide what alerts Meridian receives, so a poorly tested change could create blind spots. However, emergency changes are sometimes legitimate, and management says the engineering lead reviewed it afterward. Two follow-up questions: does VigilGrid's policy formally allow emergency changes with a post-release review, and was the reviewer independent of the person who made the change? *Rating: partially credible.*

### 6.3 Controls reported with no exceptions but limited testing

| Ref | Control | Why a clean result gives limited assurance |
|---|---|---|
| CC7.3 | Incident response | No security incidents occurred, so the auditor reviewed only the plan and a tabletop exercise (design). Whether the process works under real pressure is untested. |
| C1.2 | Customer data deletion within 90 days of contract end | No customers left during the period, so the deletion process was never tested in practice. This matters to Meridian at contract exit. |

### 6.4 Exceptions conclusion
The four exceptions cluster around access management and oversight of third parties. Together, CC6.2 and CC6.3 mean VigilGrid could neither remove access promptly nor detect lingering access through review, which is significant for a vendor with privileged reach into customer environments. The remaining exceptions (CC9.2 and CC8.1) show weaker oversight of the overnight partner and an informal approach to emergency changes. Management's responses explain causes but generally lack evidence of remediation.

Two controls with clean results, incident response and data deletion, were not tested in operation. Neither is a failure, but Meridian should not treat them as proven.

**Actions required:**
1. Request evidence that the CC6.3 offboarding process was fixed, plus the result of any access log review covering the affected accounts.
2. Request the current privileged access review records for Q2 and Q3 2026 and confirm the control is operating.
3. Request the completed risk assessment of the overnight staffing partner.
4. Ask for VigilGrid's emergency change policy and confirm who reviewed the CC8.1 change.
5. Seek contractual commitments on data deletion and incident notification, since neither was operationally tested.
