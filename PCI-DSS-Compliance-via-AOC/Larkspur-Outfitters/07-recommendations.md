---
title: Recommendations
prev: 06-risk-assessment.html
next: appendix-a.html
---

## 7. Recommendations

### Decision: Conditional Approval

| Service | Decision | Condition |
|---|---|---|
| One-time card processing | **Approve** | None beyond standard onboarding |
| Card-on-file storage | **Approve** | Tokenization must be used (see Action 3) |
| Recurring billing | **Hold** | Approve only when Actions 1 and 2 are satisfied |

Larkspur can launch standard checkout and card-on-file storage now. The subscription program goes live once PayStream has shown that recurring billing is secure.

### Recommended Actions

| # | Action | Owner | Target |
|---|---|---|---|
| 1 | **Request written confirmation and evidence from PayStream.** Ask whether the Recurring Billing Manager handles cardholder data, what controls protect it, and when it will be assessed. Request the relevant sections of the Report on Compliance and any interim evidence, such as a penetration test summary. | Information Security | Send within 5 business days; response due in 15 |
| 2 | **Make recurring billing approval conditional on that evidence.** If PayStream cannot show adequate controls or a dated plan for assessment, keep the service on hold or run subscriptions through a different assessed provider. | Information Security and E-commerce Team | Decision within 10 business days of vendor response |
| 3 | **Use tokenization as a compensating control.** Configure the integration so Larkspur's systems and the billing service only ever receive tokens from the Secure Vault, never real card numbers. | E-commerce Team and IT | Before recurring billing goes live |
| 4 | **Add contract language.** Require PayStream to notify Larkspur of any security incident, provide an updated AOC each year, and add Recurring Billing Manager to its next assessment. | Procurement and Legal | Before contract signature |
| 5 | **Track the vendor in the register.** Record risk TPRM-PS-001, set a reminder to request PayStream's renewed AOC before February 2027, and review the risk when the vendor responds. | Information Security | Within 5 business days |

### Contingency

If PayStream does not respond with acceptable evidence by the deadline, the recommendation changes to: **do not use Recurring Billing Manager.** Larkspur could implement recurring charges itself using stored tokens from the assessed Secure Vault, or evaluate another provider whose recurring billing service is covered by its AOC.

### Residual Risk

If Actions 1 to 5 are completed, residual risk for recurring billing falls from High to Low (Section 7).
