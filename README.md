# ISO 27001 & ISO 42001 Gap Assessment — Northbridge Analytics (Portfolio Project)

## Overview
This is a fictional GRC consulting engagement, built to demonstrate a full ISO 27001:2022 
certification readiness assessment, extended with ISO/IEC 42001:2023 AI governance 
considerations given the client's in-house AI risk-scoring model.

**Role:** GRC Consultant (self-directed learning project)
**Frameworks:** ISO/IEC 27001:2022 (Annex A), ISO/IEC 42001:2023
**Client:** Northbridge Analytics Inc. (fictional B2B SaaS company, financial services sector)

## Scenario
Nothbridge Analytics is a 60-person B2B SaaS company that has a deadline for acheieving the ISO 27001 cert in 9 months. The company is Toronto-based and provides predictive data analytics to financial and insurance sectors. The company's platform ingests client transaction and account data to generate risk-scoring outputs. These results are used by the clients in underwriting and fraud review workflows.

### Size
~60 employees across engineering(25), sales and customer success(10), data and analytics(8), people and operations(5) and other executive roles. 
### Structure
The company operates on a remote-first model, with employees distributed across Canada and a small US presence.
### Technology and environment
- The platform is hosted entirely on AWS in a multi-tenant SaaS architecture.
- Engineering workflows use GitHub for version control and GitHub Actions for CI/CD, with infrastructure managed via Terraform.
- Most internal tools are federated through Okta SSO, though several legacy internal applications (administrative dashboards, internal reporting tools) remain outside this integration.
### Security Function
- Northbridge does not currently have a dedicated security team.
- Security-related responsibilities have been handled informally by a senior engineer alongside their primary engineering duties for approximately the past year.
### Business Driver for Certifications
- Three prospective enterprise clients — all regulated financial institutions — have indicated that ISO 27001 certification is a contractual prerequisite for vendor onboarding, as part of their third-party vendor risk management requirements. Leadership has set a 9-month target for certification readiness.
### Assessment history
- An external vendor security review conducted approximately 8 months ago identified the absence of a documented incident response plan and a formal access review process.
- These findings were acknowledged internally but have not yet been remediated.

## Contents
| Section | Description |
|---|---|
| [01 – Scope & Methodology](./01-scope-methodology.md) | ISMS boundary definition, assessment approach |
| [02 – Current State Findings](./02-current-state-findings.md) | Findings by Annex A domain |
| [03 – Gap Analysis (Annex A)](./03-gap-analysis-annex-a.md) | Current vs. Target Profile per control |
| [04 – Risk Register](./04-risk-register.md) | Prioritized gaps with likelihood/impact |
| [05 – Remediation Roadmap](./05-remediation-roadmap.md) | Phased 9-month plan |
| [06 – ISO 42001 AI Governance](./06-iso42001-ai-governance.md) | AI management system gap assessment |
| [Appendix – Statement of Applicability](./appendix-statement-of-applicability.md) | Full control applicability justification |

## Skills Demonstrated in this **Gap Assesement**
- ISO 27001 Annex A control mapping and gap assessment
- Risk-based prioritization and remediation planning
- AI governance analysis (ISO 42001) for a regulated-industry AI system
- Professional GRC reporting and documentation
