### A.5 - Organizational Controls 
- Northbridge does not maintain a formal information security policy
- Security related decisions are made by the senior engineer who has no defined roles and responsibilities.
- No governance stucture to information security(relevant to A.5.1, A.5.2).
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
