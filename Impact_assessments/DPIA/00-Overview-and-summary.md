## Overview

### About Brightwell Home

Brightwell Home is an online retailer of sustainable home goods. It is headquartered in Toronto, with a small office in Dublin. It has about 450 employees, of whom about 40 are based in the EU, and about 800,000 customers across Canada, the European Union, and California.

Brightwell holds customer names, addresses, email addresses, order history, and payment tokens, as well as employee HR and payroll data. This places it under three privacy laws: GDPR (EU customers and staff), CCPA/CPRA (California customers), and PIPEDA (Canadian customers).

### Purpose and Objectives

Brightwell relies on outside vendors for payroll, hosting, payments, customer support, and marketing, but until now it has had no structured way to decide which vendors create the most risk or how closely each should be reviewed. This report documents a third-party risk management program built from the ground up by the GRC team. Its objectives are to:

1. define clear rules for ranking vendors by risk,
2. record every in-scope vendor in a single inventory,
3. assess vendors in proportion to the risk they create,
4. rate the weaknesses found and assign actions with deadlines, and
5. carry out a DPIA where a vendor's processing of personal data creates high risk for individuals.

### Scope

The report covers ten vendors, of which eight handle Brightwell data. Three of them have been assessed so far. A DPIA is included for PeopleMetrics, the only vendor that met the DPIA triggers.

### Approach

The work followed the order of the report. Vendors were identified and tiered (Sections 1 and 2), assessed through questionnaires and supporting evidence (Section 3), and their findings were rated and assigned remediation actions (Section 4). The vendor with the highest-risk personal data processing was then assessed in depth through a DPIA (Section 5).


## Executive Summary

This report sets out Brightwell Home's third-party risk management program and the results of its first vendor reviews.

### Summary of Results

Brightwell Home works with ten vendors that handle its data or support its operations. This review tiered all ten by risk, assessed the three where the exposure is highest or most immediate (CloudNimbus, PeopleMetrics, and MailBloom), and carried out a Data Protection Impact Assessment (DPIA) on PeopleMetrics. The review produced twelve findings: ten from the vendor assessments and two internal Brightwell actions identified during the DPIA. One finding is Critical, five are High, four are Medium, and two are Low.

### Vendors by Tier

| Tier | Vendors | Assessment status |
|---|---|---|
| Tier 1: Critical | PayrollPro, CloudNimbus, ShopStream | CloudNimbus assessed. PayrollPro and ShopStream outstanding. |
| Tier 2: High | PeopleMetrics, HelpDeskly, MailBloom | PeopleMetrics and MailBloom assessed. HelpDeskly outstanding. |
| Tier 3: Medium | DataLens BI, MeetSphere | Outstanding |
| Tier 4: Low | OfficeBrew, PixelStock | Complete |

### Top Three Risks

**1. EU employee data is sent to the US without a legal safeguard (Critical).** PeopleMetrics stores Dublin employee data in the United States, and the contract terms that make this transfer lawful are not in place. PeopleMetrics also generates performance scores with no human review, and employees have not been told about either practice. This could lead to regulatory action and unfair decisions affecting staff.

**2. Vendors would notify Brightwell of a breach too late (High).** CloudNimbus takes up to seven days and PeopleMetrics up to five business days. GDPR gives Brightwell 72 hours to notify the regulator, so a breach at either vendor could put Brightwell in violation before it knows an incident has occurred.

**3. Two of the three most critical vendors have not been assessed.** PayrollPro (SINs and bank details) and ShopStream (payment data) have not been reviewed, so Brightwell has no documented assurance over them.

MailBloom's lack of required multi-factor authentication for administrator accounts (High) is also worth noting because it can be fixed immediately at no cost.

### Decisions Requested

1. Approve continued use of PeopleMetrics on condition that Standard Contractual Clauses are signed within 30 days, with no new EU employee data sent until then.
2. Approve contract amendments requiring breach notification within 48 hours from CloudNimbus and PeopleMetrics.
3. Approve completion of the PayrollPro and ShopStream assessments within 90 days.

### Next Steps

| Action | Owner | Target |
|---|---|---|
| Sign Standard Contractual Clauses with PeopleMetrics | Privacy Lead | 30 days |
| Update employee privacy notice and introduce human review of scores | EU HR Manager | 60 days |
| Enable MFA on Brightwell's MailBloom admin accounts | Marketing Manager | Immediately |
| Amend CloudNimbus and PeopleMetrics contracts (breach notice, retention, subcontractors) | GRC Team | 60 days |
| Complete PayrollPro and ShopStream assessments | GRC Team | 90 days |
| Reassess all Tier 1 and Tier 2 vendors | GRC Team | October 2027 |

---
