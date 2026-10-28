## Section 2: Vendor Inventory

### 2.1 Purpose and Maintenance

The vendor inventory is the central register of every third party in scope for this program. All tiering, assessment, and remediation activity is driven from it. The full inventory is maintained in a spreadsheet (Appendix A) and owned by the GRC team.

The inventory is updated when a vendor is onboarded or offboarded, and whenever a business owner reports a change in the service, the data shared, or the hosting location. Each quarter, the GRC team reconciles the inventory against the accounts payable vendor list to identify vendors that were engaged without going through the program. For example, a marketing team that signs up for a new survey tool with a corporate card would appear in accounts payable but not in the inventory, and would be added and tiered at that point.

### 2.2 Inventory Fields

For each vendor, the inventory records the service provided, the types of data accessed, the data storage location, the Brightwell business owner, the assigned tier and the reason for it, the applicable assessment type, the DPIA determination made by the Privacy Lead, the assessment status, the overall risk rating, and the next review date. Recording the reason for each tier assignment allows the rating to be reviewed and defended later without relying on the memory of the person who assigned it.

### 2.3 Inventory Composition

Brightwell currently has ten vendors in scope. Their tiers were assigned using the criteria in Section 1.4.

| Vendor | Service | Data accessed | Tier |
|---|---|---|---|
| PayrollPro | Payroll processing | SINs, bank details, salaries | Tier 1: Critical |
| CloudNimbus | Cloud hosting | All customer and employee data | Tier 1: Critical |
| ShopStream | Payment processing | Payment tokens, customer details | Tier 1: Critical |
| PeopleMetrics | HR analytics | EU employee performance data | Tier 2: High |
| HelpDeskly | Customer support | Names, emails, order issues | Tier 2: High |
| MailBloom | Email marketing | Customer emails, preferences | Tier 2: High |
| DataLens BI | Analytics dashboards | Pseudonymized order data | Tier 3: Medium |
| MeetSphere | Video conferencing | Meeting content, attendee names | Tier 3: Medium |
| OfficeBrew | Office refreshments | None | Tier 4: Low |
| PixelStock | Stock photography | None | Tier 4: Low |

Three vendors are Tier 1, three are Tier 2, two are Tier 3, and two are Tier 4. The business owner, data location, tier rationale, and review dates for each vendor are recorded in Appendix A.

### 2.4 Observations

**Concentration of data.** The three Tier 1 vendors together process nearly all of Brightwell's sensitive data. CloudNimbus is the largest single dependency, since it hosts both the customer-facing website and the systems that hold customer and employee records. A failure or breach at CloudNimbus would affect sales and data protection at the same time, which is why it is subject to the most rigorous review.

**Data location.** Six of the eight vendors that handle data process it in the United States, in whole or in part. PeopleMetrics stores EU employee data in the US, which makes it the clearest case of a cross-border transfer under GDPR. HelpDeskly and MailBloom may also hold EU customer data. The business owners will confirm this, because it determines whether transfer safeguards are needed for those vendors.

**Tiering outcome.** MeetSphere is placed in Tier 3 rather than Tier 4. It has no access to Brightwell systems, but it can capture confidential discussions, and under Section 1.4 the highest-risk answer decides the tier. PeopleMetrics is placed in Tier 2 rather than Tier 1 because an outage would not stop sales or payroll. Its processing of EU employee performance data is addressed through the DPIA process in Section 5, and not through the tier.


---
