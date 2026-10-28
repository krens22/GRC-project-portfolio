## Appendix A: Vendor Inventory

### A.1 Core Details

| Vendor | Service | Data accessed | Data location | Business owner | Tier | Tier rationale |
|---|---|---|---|---|---|---|
| PayrollPro | Payroll processing | SINs, bank details, salaries | Canada, US | HR Director | Tier 1: Critical | Highly sensitive financial data; an outage stops payroll |
| CloudNimbus | Cloud hosting | All customer and employee data | Canada, Ireland | Head of Engineering | Tier 1: Critical | Holds everything and runs the website; an outage stops sales |
| ShopStream | Payment processing | Payment tokens, customer details | US, Canada | Finance Director | Tier 1: Critical | Payment data; an outage stops checkout |
| PeopleMetrics | HR analytics | EU employee performance data | US | EU HR Manager (Dublin) | Tier 2: High | Personal data of lower sensitivity; failure has a workaround |
| HelpDeskly | Customer support | Names, emails, order issues | US | Customer Support Manager | Tier 2: High | Customer personal data, no financial data |
| MailBloom | Email marketing | Customer emails, preferences | US | Marketing Manager | Tier 2: High | Large customer email list, no financial data |
| DataLens BI | Analytics dashboards | Pseudonymized order data | Canada | Head of Analytics | Tier 3: Medium | Pseudonymized data only, no direct system access |
| MeetSphere | Video conferencing | Meeting content, attendee names | US | IT Manager | Tier 3: Medium | Can capture confidential discussions, but limited personal data |
| OfficeBrew | Office refreshments | None | Not applicable | Office Manager | Tier 4: Low | No data or system access |
| PixelStock | Stock photography | None | Not applicable | Marketing Manager | Tier 4: Low | No data or system access |

### A.2 Assessment Tracking

| Vendor | Assessment type | DPIA required | Status | Risk rating | Next review |
|---|---|---|---|---|---|
| PayrollPro | SIG Lite + SOC 2 report | No | Not started | Pending | October 2027 |
| CloudNimbus | CSA CAIQ + ISO 27001 certificate | No | Complete | High | October 2027 |
| ShopStream | SIG Lite + PCI DSS attestation | No | Not started | Pending | October 2027 |
| PeopleMetrics | SIG Lite | Yes | Complete | Critical | October 2027 |
| HelpDeskly | SIG Lite | No | Not started | Pending | October 2027 |
| MailBloom | SIG Lite | No | Complete | High | October 2027 |
| DataLens BI | Short 10-question form | No | Not started | Pending | October 2028 |
| MeetSphere | Short 10-question form | No | Not started | Pending | October 2028 |
| OfficeBrew | Basic onboarding check | No | Complete | Low | At onboarding only |
| PixelStock | Basic onboarding check | No | Complete | Low | At onboarding only |

---
