## 7. CUEC analysis

### 7.1 Summary of CUECs

| # | CUEC (summary) | Meridian owner | Feasibility | Evidence to retain | Main concern |
|---|---|---|---|---|---|
| 1 | Install the agent on all in-scope endpoints; apply updates within 30 days | IT Operations | Moderate | Asset inventory reconciled monthly against the agent console; patch compliance report | Devices that cannot run the agent (warehouse handhelds, kiosks, contractor laptops) create blind spots |
| 2 | Forward logs from all required sources | Security Team | Moderate | Log source inventory; ingestion health checks | The report never defines "required sources" |
| 3 | Keep the authorized contacts list current; notify VigilGrid within 24 hours of changes | Security Team and HR | Moderate to Hard | Contact list with review dates; offboarding checklist step | Staff turnover across three time zones; a stale list means VigilGrid may call or take direction from the wrong person |
| 4 | Restrict VigilGrid API keys and portal access to authorized personnel | Security / Identity team | Easy | SSO and MFA on the portal; keys held in a secrets vault; access list | Low, but the mobile app was not assessed (see Section 5) |
| 5 | Evaluate whether monitoring and response actions comply with local labor and privacy laws | Legal / Privacy, with HR | **Hard** | Completed privacy assessment; employee notices; documented data transfer mechanism | Highest concern: legal responsibility moves to Meridian, and the audit does not cover Privacy |

### 7.2 Analysis

**CUEC 1: Agent coverage and updates.** Meridian is a logistics company, so it likely has devices beyond office laptops, such as handheld scanners and shared kiosks, that may not support the agent. Any device without the agent is invisible to VigilGrid, and attackers favor the blind spots. Meridian needs an accurate asset inventory to prove coverage, and a patch process that meets the 30-day window.

**CUEC 2: Log forwarding.** The report says "required sources" but never lists them. Meridian could comply in good faith and still fall short. This needs written clarification from VigilGrid.

**CUEC 3: Authorized contacts.** This links to the exceptions in Section 6. If a Meridian security lead leaves and nobody tells VigilGrid within 24 hours, VigilGrid may still treat that person's instructions as authorized, and VigilGrid itself failed to remove departed users' access on time (CC6.3). Both sides of the process are weak. A practical fix is to add "notify VigilGrid" as a mandatory step in Meridian's own offboarding checklist.

**CUEC 4: Keys and portal access.** This is straightforward for a security-mature organization: enforce SSO with MFA on the portal and store API keys in a secrets vault rather than in scripts or shared documents. The only added question is the mobile app, which sits outside the audit.

**CUEC 5: Legal compliance of monitoring.** This is the one to take seriously. In effect, VigilGrid says, "monitoring your employees is legal where you operate, and that's your job to confirm." Meridian operates in three jurisdictions, and the agent sends detailed employee activity data (logins, programs run, files accessed) to a US cloud.

- **Ireland (GDPR):** Employee monitoring generally needs a documented lawful basis, clear notice to staff, and usually a **DPIA** (a structured assessment of privacy risk). Sending EU employee data to the US also needs a transfer mechanism, such as **standard contractual clauses (SCCs)**, which are pre-approved contract terms for data leaving the EU, or the vendor's certification under the **EU-US Data Privacy Framework**. Meridian should ask which one VigilGrid relies on.
- **Canada:** Rules vary by province. For example, Ontario requires employers of 25 or more employees to have a written electronic monitoring policy, and Quebec has its own strict privacy law.
- **United States:** Some states, such as New York, require written notice to employees before electronic monitoring.

I'm not a lawyer, and these are examples to prompt the right questions, so Meridian's legal team would confirm the details. The point for your memo is that the audit's missing Privacy criterion, noted in Section 4, comes back here as a real obligation.

### 7.3 CUEC conclusion
Of the five CUECs, three (agent coverage, log forwarding, and contact maintenance) are achievable with existing IT and security processes but need clear ownership and evidence, and one (portal and key access) is straightforward. The fifth, legal compliance of monitoring, is the most demanding: it places responsibility on Meridian for EU, Canadian, and US employee monitoring requirements, while the SOC 2 report offers no assurance on privacy.

Meridian's ability to meet CUEC 3 also depends on VigilGrid fixing its own access removal weaknesses, so the two sides' controls need to work together.

**Actions required:**
1. Reconcile Meridian's asset inventory against the planned agent deployment and document devices that cannot run the agent, with an alternative monitoring plan for each.
2. Ask VigilGrid to define "required log sources" in writing.
3. Add a "notify VigilGrid within 24 hours" step to Meridian's offboarding checklist and name a backup owner.
4. Enforce SSO and MFA on the VigilGrid portal and store API keys in a secrets vault.
5. Complete a privacy assessment (including a DPIA for EU staff), issue employee notices, and confirm the data transfer mechanism before go-live.
