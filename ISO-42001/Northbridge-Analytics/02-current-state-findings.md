---
title: current findings
---
[Back](./)

# Current evidence-based findings

Annex A 2022 has 4 themes: Organizational (37 controls), People (8), Physical (14), Technological (34). For Northbridge, the highest-relevance domains are:

A.5 Organizational controls — policies, roles, supplier relationships, access control policy
A.6 People controls — screening, awareness training, responsibilities on termination
A.8 Technological controls — access control, secure development, logging/monitoring, cryptography

### A.5 - Organizational Controls 
- Northbridge does not maintain a formal information security policy
- Security related decisions are made by the senior engineer who has no defined roles and responsibilities.
- No governance stucture to information security (relevant to A.5.1, A.5.2).
- No access control policy exists in written form and access provisioning is handles ad-hoc by engineering and IT staff without a documented least-privilege standard (A.5.15, A.5.18)
- Supplier/vendor risk is not formally assessed given Northbridge's reliance on AWS and Okta as critical infrastructure providers and no evidence of security review process for the same (A.5.19 - A.5.22)
- No incident response procedure exists in written form assuming the prior vendor security review (8 months ago) identified this same gap, which has not yet been remediated (A.5.24, A.5.26).

### A.5 - People Controls 
- Northbridge conducts background checks on new hires, indicating a baseline screening control is in place (A.6.1).
- No formal security onboarding process. New employees are not walked through security responsibilities, acceptable use expectations, or access provisioning standards as a defined step (A.6.3, A.6.6)
- No security awareness training program is described anywhere in current practice this includes engineers and IT personel who have direct access to production client data. No structured exposure to phishing awareness, data handling expectations, or incident reporting procedures(A.6.3).
- Offboarding is informal and there is no checklist ensuring access is revoked when an employee departs, creating risk of orphaned credentials persisting after termination (A.6.5).

### A.5 - Technological Controls
- Okta SSO is deployed across most internal tools, indicating a **partial** centralized authentication capability exists (A.8.5).
- Several legacy tools like internal admin dashboards and reporting tools remain outside this integration and rely on standalone logins, creating inconsistent authentication coverage across in-scope systems (A.8.2, A.8.5)
- No information on logging or monitoring capability. The company cannot prove whether it has experienced a security incident this suggests detection capability is either absent or unverified (A.8.15, A.8.16).
- The engineering environment uses GitHub, GitHub Actions, and Terraform for development and infrastructure management however no information is available on code review enforcement (A.8.25), secrets management practices (A.8.28), or secure configuration baselines for cloud infrastructure(A.8.9).
- Employees use a mix of personal and company-issued laptops with no described device management or security policy this raises endpoint risk for a remote-first workforce (A.8.1).

## Control reference

🔴 Confirmed gap &nbsp; 🟡 Partly in place &nbsp; ⚪ Unknown, needs verification

**A.5 Organizational controls**

- 🔴 <span title="A written, approved security policy. Found: none exists, only scattered unapproved Notion pages."><b>A.5.1</b> Security policy</span>
- 🔴 <span title="Named people accountable for security, with backups. Found: one engineer does it informally, no backup.">**A.5.2** Roles and responsibilities</span>
- 🔴 <span title="Rules on who may access what. Found: access is granted ad hoc, with no least-privilege standard."><b>A.5.15</b> Access control</span>
- 🔴 <span title="Access is granted, reviewed and removed in a controlled way. Found: no access review process; a client flagged it and it was never actioned."><b>A.5.18</b> Access rights</span>
- 🔴 <span title="Managing risk from vendors you depend on. Found: no supplier review, despite reliance on AWS and Okta."><b>A.5.19–22</b> Supplier relationships</span>
- 🔴 <span title="Planning ahead for incidents. Found: no written incident response plan; flagged 8 months ago."><b>A.5.24</b> Incident planning</span>
- 🔴 <span title="Responding to incidents by following the plan. Found: no defined process; it depends on A.5.24."><b>A.5.26</b> Incident response</span>

**A.6 People controls**

- 🟡 <span title="Background checks before hiring. Found: checks run for new hires, but there is no written policy."><b>A.6.1</b> Screening</span>
- 🔴 <span title="Staff get security onboarding and regular training. Found: none described."><b>A.6.3</b> Awareness and training</span>
- 🔴 <span title="Access and duties end properly when someone leaves. Found: no offboarding checklist."><b>A.6.5</b> After termination</span>

**A.8 Technological controls**

- 🔴 <span title="Laptops and phones that reach company data are secured. Found: mix of personal and company laptops, no device policy."><b>A.8.1</b> Endpoint devices</span>
- 🟡 <span title="Admin access is limited and controlled. Found: Okta covers most tools; legacy dashboards sit outside it."><b>A.8.2</b> Privileged access</span>
- 🟡 <span title="Secure logins such as SSO and MFA. Found: Okta covers most tools, not all; MFA coverage unconfirmed."><b>A.8.5</b> Secure authentication</span>
- ⚪ <span title="Systems built from a secure, documented baseline. Unknown: Terraform is used, but baselines are unconfirmed."><b>A.8.9</b> Configuration management</span>
- ⚪ <span title="Events are logged for later investigation. Unknown: nobody has confirmed what is logged."><b>A.8.15</b> Logging</span>
- 🔴 <span title="Unusual activity is watched for. Found: the company cannot confirm whether it has had an incident, which suggests no monitoring."><b>A.8.16</b> Monitoring</span>
- ⚪ <span title="Security is built into software development. Unknown: CI/CD exists, but enforcement is unconfirmed."><b>A.8.25</b> Secure development</span>
- ⚪ <span title="Defined secure coding practices. Unknown: no information on standards or scanning."><b>A.8.28</b> Secure coding</span>

