## 7. Risk Assessment

### Rating Method

Each gap is rated on two questions, using a simple three-level scale.

- **Likelihood:** How probable is it that a security problem occurs in the unassessed service?
- **Impact:** How serious would the consequences be for Larkspur if it did?

| | Impact: Low | Impact: Medium | Impact: High |
|---|---|---|---|
| **Likelihood: High** | Medium | High | High |
| **Likelihood: Medium** | Low | Medium | High |
| **Likelihood: Low** | Low | Low | Medium |

### Risk 1: Recurring billing service has not been independently assessed

| Factor | Rating | Reasoning |
|---|---|---|
| Likelihood | **Medium** | The service shares a vendor with two assessed services that passed with no open items, which is a positive sign. However, it is a newer product, no assessor has tested it, and PayStream has not yet provided evidence of its controls. |
| Impact | **High** | If the service handles cardholder data, a weakness could expose the saved cards of every subscriber. Consequences include card brand fines, breach notification costs, and loss of customer trust. A failure would hit all subscribers at once, not a single order. |
| **Inherent risk** | **High** | Medium likelihood combined with high impact. |

### Risk after Planned Controls (Residual Risk)

Section 8 recommends conditions that reduce this risk. If they are implemented, the rating changes as follows.

| Factor | Rating | Why it changes |
|---|---|---|
| Likelihood | Low | Larkspur only stores and sends tokens, so recurring billing has no real card numbers to lose. Vendor evidence reduces the remaining uncertainty. |
| Impact | Medium | A compromised token is far less useful to an attacker than a real card number, though some operational and reputational harm remains. |
| **Residual risk** | **Low** | Low likelihood combined with medium impact. |

### Risk Register Entry

| Field | Entry |
|---|---|
| Risk ID | TPRM-PS-001 |
| Description | PayStream Recurring Billing Manager not included in PCI DSS assessment |
| Inherent risk | High |
| Residual risk (with controls) | Low |
| Owner | Larkspur Information Security (risk); E-commerce Team (business) |
| Treatment | Mitigate: conditional approval, tokenization, vendor evidence request |
| Review date | Within 30 days of vendor response, or before launch of recurring billing, whichever is earlier |
| Status | Open |

1. Does the Recurring Billing Manager store, process, or transmit cardholder data, or does it only use tokens from the Secure Vault?
2. What security controls currently protect the service, and is there independent evidence (for example, a penetration test summary)?
3. When will the service be included in an assessment, and who is the assessor?
