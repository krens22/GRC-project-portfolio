## 5. Scope Findings

Each service Larkspur needs (Section 3) was compared against the services PayStream's AOC lists as assessed (Appendix A, Parts 2a and 2b).

| # | Service Larkspur needs | AOC listing | Covered by assessment? | Result |
|---|---|---|---|---|
| 1 | One-time card processing | PayStream Gateway (Part 2a) | Yes | Covered |
| 2 | Card-on-file storage | PayStream Secure Vault (Part 2a) | Yes | Covered |
| 3 | Recurring billing | Recurring Billing Manager (Part 2b) | **No** | **Gap** |

### Finding 1: Recurring billing is not covered by the PCI DSS assessment

PayStream's AOC states "Compliant" overall, but Part 2b lists the Recurring Billing Manager as provided but not assessed. The vendor's stated reason is that the service was released after the assessment scope was finalized and is planned for the next annual assessment.

This means no independent assessor has tested the controls around the one service Larkspur needs most for the subscription program. Because that service triggers monthly charges against stored customer cards, it is likely to interact with cardholder data. Whether it does is not stated in the AOC and must be confirmed with the vendor.

### Finding 2: The "Compliant" status could be misread

The overall status is accurate but easy to over-read. It applies only to the services in Part 2a. A reader who sees "Compliant" and stops there could wrongly conclude that all PayStream services, including recurring billing, are covered.

### Observation: Fraud Screening Add-on (not a finding)

The Fraud Screening Add-on is also unassessed, but it is provided by a separate third party and Larkspur has not requested it. It is therefore outside the scope of this review. If Larkspur later wants fraud screening, it should be reviewed separately.

### Open questions for PayStream

1. Does the Recurring Billing Manager store, process, or transmit cardholder data, or does it only use tokens from the Secure Vault?
2. What security controls currently protect the service, and is there independent evidence (for example, a penetration test summary)?
3. When will the service be included in an assessment, and who is the assessor?
