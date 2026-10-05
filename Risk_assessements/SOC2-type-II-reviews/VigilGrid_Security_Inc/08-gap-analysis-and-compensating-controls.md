## 8. Gap analysis and compensating controls

### 8.1 Gap register

| ID | Gap | Source | Risk to Meridian | Response | Residual risk |
|---|---|---|---|---|---|
| G1 | Access removal failed and privileged access reviews not performed (CC6.3, CC6.2) | Sec. 6 | Former or unauthorized VigilGrid staff could reach the console holding Meridian's data | Compensating control and contractual protection (see 8.2) | Medium |
| G2 | No audit coverage from April 1, 2026 to present | Sec. 4 | Control failures or incidents since March are unknown | Bridge letter required before signing | Low, once received |
| G3 | Automated Response module not audited | Sec. 5 | A misfire could isolate critical systems and halt operations | Compensating control (see 8.2) | Low |
| G4 | Mobile app not audited | Sec. 5 | Alert data or approvals exposed through an unassessed app | Compensating control: prohibit use of the app | Low |
| G5 | Overnight staffing partner carved out and never assessed (CC9.2) | Sec. 5, 6 | One third of monitoring done by a party nobody has reviewed | Remediation request plus contractual protection | Medium |
| G6 | Privacy not audited; EU employee data in a US cloud; 13-month retention | Sec. 4, 7 | GDPR exposure and misuse of employee activity data | Compensating control and contractual protection (see 8.2) | Medium until completed |
| G7 | Incident response never tested in practice (CC7.3) | Sec. 6.3 | Slow or confused response in a real attack | Contractual protection and a joint exercise | Low to Medium |
| G8 | Data deletion never tested (C1.2) | Sec. 6.3 | Meridian data lingers after the contract ends | Contractual protection | Low to Medium |
| G9 | Devices that cannot run the agent (CUEC 1) | Sec. 7 | Blind spots attackers can use | Compensating control | Low to Medium |
| G10 | Emergency change without peer review (CC8.1) | Sec. 6 | Possible detection blind spot from one change | **Risk acceptance**, pending the vendor's emergency change policy | Low |

### 8.2 Compensating controls for the key gaps

**G1: Access weaknesses at the vendor (Medium residual).**
Meridian can't fix VigilGrid's offboarding, so the goal is to limit the damage if a stale account is misused.
- Run the agent with least privilege, and require Meridian approval for high-impact response actions.
- Alert on logins to Meridian's VigilGrid tenant and on API key use from unexpected locations.
- Require a quarterly written access review attestation from VigilGrid.
- Evidence: alert rules, approval logs, and the attestations.
*Why residual risk stays Medium:* these measures limit and detect problems but don't prevent weaknesses inside VigilGrid.

**G3: Automated Response (Low residual).**
- Launch in alert-only mode and later enable it on a small pilot group.
- Keep an exclusion list of critical systems (for example, the warehouse management system) that Meridian controls and VigilGrid cannot override.
- Test in a non-production environment first.

**G6: Privacy and EU data (Medium until completed).**
- Complete a DPIA and sign a DPA that includes a data transfer mechanism (SCCs or confirmation of the vendor's Data Privacy Framework certification).
- Issue employee notices before go-live.
- Configure data minimization (collect only what detection needs) and ask to shorten the 13-month retention or host EU data in an EU region.
- This is the one gap that must be closed before launch rather than managed afterward, because it's a legal obligation.

**G10: Accepted risk.**
Not every finding needs a safeguard. One sampled emergency change out of 40, with a documented retroactive review, is low impact. The sensible response is to accept it formally, name who accepted it, and revisit if the next report shows a pattern.

### 8.3 Gap analysis conclusion
The gaps fall into three groups. The first is **unaudited features and periods** (G2, G3, G4), which are manageable through a bridge letter and by limiting how Meridian uses the service at launch. The second is **VigilGrid's internal weaknesses** (G1, G5, G7, G8), which Meridian cannot fix directly and must address through limits on privileges, detection of misuse, and contract terms. The third is **legal and privacy exposure** (G6), which is Meridian's own obligation and cannot be handled after go-live.

With the proposed measures in place, no gap is rated higher than Medium residual risk. Two (G1 and G5) will remain at Medium because Meridian can reduce but not eliminate exposure to weaknesses inside VigilGrid, and these should be reassessed against the next SOC 2 report.

**Actions required:**
1. Make the bridge letter and DPA conditions of signing.
2. Launch Automated Response in alert-only mode and prohibit the mobile app until each is covered by an audit.
3. Complete the DPIA and employee notices before any EU data is collected.
4. Record formal risk acceptance for G10, and assign owners and due dates to all other items.
