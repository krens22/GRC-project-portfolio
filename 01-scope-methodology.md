# Scope and Methodology

#### what people, processes, technology, and locations touch the information/data we're trying to protect? 
####


**## In- Scope**
- The production Saas platform (AWS-hosted) - this is where the client data lives.
- Engineering department - they build/maintain the systems processing client data.
- The risk scoring AI model directly intakes financial data and drives client-facing decisions.
- CI/CD pipeline(Github,GitHub Actions, Terraform) - means/medium by which any code and infrustructure changes reach production.
- The legacy standalone-login tools (old admin dashboards, internal reporting)
- Okta SSO - Controls access to all the above systems.

**## Out of Scope**
- Sales/CS tooling that doesn't touch production client data.
- People ops/finance systems (payroll, HR platforms) — internal employee data only, not client data.

## Methodology
This assessment was conducted using a control-based gap analysis approach against ISO/IEC 27001:2022 Annex A, supplemented by ISO/IEC 42001:2023 for the in-scope AI system. The assessment followed three steps:
1. Scoping — defining ISMS boundaries based on data flow analysis, identifying all systems, processes, and personnel that interact with in-scope client data
2. Current state assessment — evaluating existing controls against each applicable Annex A control area, rated using a four-point maturity scale (Not Started / Partial / Implemented / Managed), **consistent with prior control maturity work performed under the NIST CSF framework**
3. Gap analysis and prioritization — comparing current state to target state, with findings prioritized by risk to the certification timeline and to Northbridge's regulated-industry client obligation.


