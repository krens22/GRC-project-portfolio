## 9. Final recommendation

### 9.1 Recommendation

**Approve with conditions.**

VigilGrid's SOC 2 Type II report provides meaningful assurance over monitoring, availability, backup and recovery, but it carries a qualified opinion on access removal, shows repeated weaknesses in access governance, and leaves several features and providers outside its scope. For a Tier 1 vendor with privileged access to every Meridian endpoint, these findings are manageable but not ignorable. Approval is therefore conditional on the actions below, and the contract should not be signed until the first group is complete.

### 9.2 Conditions

**A. Before signing the contract**
| # | Condition | Closes | Owner |
|---|---|---|---|
| 1 | Receive a bridge letter covering April 1, 2026 to the present | G2 | Procurement / TPRM |
| 2 | Receive evidence that the CC6.3 offboarding fix is working and that the Q2 and Q3 2026 privileged access reviews were performed | G1 | TPRM |
| 3 | Receive the completed assessment of the overnight staffing partner, plus its assurance report or equivalent | G5 | TPRM |
| 4 | Sign a DPA with a data transfer mechanism for EU employee data | G6 | Legal / Privacy |
| 5 | Receive a penetration test summary | Evidence gap | Security |

**B. Before go-live**
| # | Condition | Closes | Owner |
|---|---|---|---|
| 6 | Complete the DPIA and issue employee notices in Ireland, Canada, and the US | G6 | Privacy / HR |
| 7 | Launch Automated Response in alert-only mode, with a critical-systems exclusion list | G3 | Security |
| 8 | Prohibit use of the mobile app until it is covered by an audit | G4 | Security |
| 9 | Document devices that cannot run the agent and the alternative monitoring for each | G9 | IT Operations |
| 10 | Configure alerts on VigilGrid tenant logins and API key use | G1 | Security |

**C. Contract terms**
- Incident notification within a defined window (for example, 24 hours of confirmation)
- Data deletion within 90 days of termination, with written certification
- Right to receive future SOC 2 reports and notice of material changes
- Notice and approval rights over changes to subservice organizations
- Limits on data retention and hosting region for EU data

### 9.3 Ongoing oversight

| Activity | Frequency | Owner |
|---|---|---|
| Review the next SOC 2 report, checking that CC6.2, CC6.3 and CC9.2 are clean | Annually, on receipt | TPRM |
| Reassess VigilGrid if it reports a security incident or a material change | Event-driven | TPRM |
| Verify Meridian's own CUEC evidence | Quarterly | Security |
| Review the Automated Response pilot before widening it | After the pilot period | Security |

### 9.4 What would change this recommendation

The recommendation should change to **reject** if:
- VigilGrid cannot or will not provide the bridge letter or evidence of remediation under conditions 1 to 3.
- The bridge letter discloses a security incident or new control failures.
- The next SOC 2 report repeats the access exceptions.

### 9.5 Risk acceptance

Gap G10 (one emergency change without peer review) is accepted at low residual risk. This acceptance must be recorded and signed by the appropriate Meridian risk owner, and revisited if the next report shows a pattern.

**Reviewer:** Karen Fernandes   **Date:** October 5, 2026
**Risk owner sign-off:**
