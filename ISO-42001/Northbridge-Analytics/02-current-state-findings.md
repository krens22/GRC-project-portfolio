---
title: current findings
---
[Back](./)

# Current evidence-based findings

Annex A 2022 has 4 themes: Organizational (37 controls), People (8), Physical (14), Technological (34). For Northbridge, the highest-relevance domains are:

A.5 Organizational controls — policies, roles, supplier relationships, access control policy\ 
A.6 People controls — screening, awareness training, responsibilities on termination\
A.8 Technological controls — access control, secure development, logging/monitoring, cryptography\

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


<style>
table {
  border-collapse: collapse;
  width: 100%;
  font-size: 0.92rem;
  display: block;
  overflow-x: auto;
}
th, td {
  padding: 8px 12px;
  text-align: left;
  vertical-align: top;
  border-bottom: 1px solid rgba(128, 128, 128, 0.3);
}
th {
  background: rgba(128, 128, 128, 0.12);
  font-weight: 600;
}
tr:nth-child(even) td {
  background: rgba(128, 128, 128, 0.05);
}
td:first-child {
  font-weight: 600;
  white-space: nowrap;
}
td:last-child {
  font-weight: 600;
  white-space: nowrap;
}
</style>

## Control reference

| Control | Name | What it means | What we found | Status |
|---|---|---|---|---|
| A.5.1 | Security policy | A written, approved policy that sets security direction | None exists; only scattered, unapproved Notion pages | Gap |
| A.5.2 | Roles and responsibilities | Named people accountable for security, with backups | One engineer does it informally; no backup | Gap |
| A.5.15 | Access control | Rules on who may access what | Access granted ad hoc; no least-privilege standard | Gap |
| A.5.18 | Access rights | Access is granted, reviewed and removed in a controlled way | No access review process | Gap |
| A.5.19–22 | Supplier relationships | Managing risk from vendors you depend on | No supplier review despite reliance on AWS and Okta | Gap |
| A.5.24 | Incident planning | Planning ahead for incidents | No written incident response plan | Gap |
| A.5.26 | Incident response | Responding to incidents by following the plan | No defined process | Gap |
| A.6.1 | Screening | Background checks before hiring | Checks run; no written policy | Partial |
| A.6.3 | Awareness and training | Security onboarding and regular training | None described | Gap |
| A.6.5 | After termination | Access and duties end properly when someone leaves | No offboarding checklist | Gap |
| A.8.1 | Endpoint devices | Laptops and phones that reach company data are secured | Mixed personal and company laptops; no device policy | Gap |
| A.8.2 | Privileged access | Admin access is limited and controlled | Okta covers most tools; legacy dashboards sit outside it | Partial |
| A.8.5 | Secure authentication | Secure logins such as SSO and MFA | Okta covers most tools, not all; MFA unconfirmed | Partial |
| A.8.9 | Configuration management | Systems built from a secure, documented baseline | Terraform used; baselines unconfirmed | Unknown |
| A.8.15 | Logging | Events recorded for later investigation | What is logged is unconfirmed | Unknown |
| A.8.16 | Monitoring | Watching for unusual activity | Company can't confirm whether it has had an incident, which suggests no monitoring | Gap |
| A.8.25 | Secure development | Security built into software development | CI/CD exists; enforcement unconfirmed | Unknown |
| A.8.28 | Secure coding | Defined secure coding practices | No information | Unknown |
