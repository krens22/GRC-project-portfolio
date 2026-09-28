<details>
<summary><b>Footnotes</b></summary>
<p>
  
1. **Governance first**. Policies, roles, and the risk assessment come before technical fixes. Auditors check the ISMS itself (Clauses 4-10) as well as the controls, and most later controls need a policy to point to.
2. **Quick wins early**. Cheap, fast fixes that remove the worst risks (revoking old access, turning on MFA) go in the first phase. They cut real risk immediately, and they show leadership visible progress.
3. **Evidence takes time**. ISO auditors want proof that controls have been operating, such as access reviews actually performed, training completed, or an incident drill run. That means controls must be in place months before the audit, so anything with a "must show it working" requirement has to start early.
  
</p>
</details>


## Section 5 — Remediation Roadmap

### Phase 1 (Months 0–3): Foundations and Quick Wins

| # | Action | Addresses | Owner | Evidence for Auditor |
|---|---|---|---|---|
| 1.1 | Executive sponsor formally commits to ISMS; appoint an ISMS owner (security lead) with a named backup | R-07, A.5.2, Clause 5 | CEO | Signed management commitment; org chart with roles |
| 1.2 | Finalize ISMS scope statement (incl. confirmation of open scoping items: sales dashboards, legacy tools) | Clause 4 | ISMS Owner | Approved scope document |
| 1.3 | Run formal risk assessment using the Section 4 method; approve risk treatment plan | Clause 6.1 | ISMS Owner | Risk register, treatment plan |
| 1.4 | Write and approve core policies: Information Security Policy, Access Control Policy, Acceptable Use | A.5.1, A.5.15 | ISMS Owner + CEO | Versioned, approved policies |
| 1.5 | Audit and revoke stale access across AWS, GitHub, Okta, and all legacy tools; eliminate shared logins | R-01, A.5.18, A.6.5 | Head of Engineering | Access review report with removal log |
| 1.6 | Enforce MFA on all in-scope systems; bring legacy tools behind Okta or restrict/retire them | R-05, A.8.2, A.8.5 | Head of Engineering | Okta config export, legacy tool decision log |
| 1.7 | Create HR onboarding/offboarding checklist that includes system access revocation | R-01, A.6.5 | People Ops | Completed checklist for next departure |

### Phase 2 (Months 3–6): Build Operating Controls

| # | Action | Addresses | Owner | Evidence for Auditor |
|---|---|---|---|---|
| 2.1 | Write incident response plan (roles, severity levels, escalation, client notification steps); run one tabletop exercise | R-02, A.5.24, A.5.26 | ISMS Owner | Approved plan, exercise notes |
| 2.2 | Turn on and centralize logging (e.g., AWS CloudTrail, GuardDuty) with alerts for high-risk events | R-02, A.8.15, A.8.16 | Head of Engineering | Log config, sample alert and response |
| 2.3 | Launch security awareness training and onboarding module; track completion | A.6.3 | People Ops | Completion records |
| 2.4 | Endpoint policy: require company-managed devices or MDM baseline (disk encryption, screen lock) for anyone accessing production | A.8.1 | Head of Engineering | MDM enrollment report |
| 2.5 | Set up supplier review process; assess AWS and Okta (start with their existing ISO/SOC reports) | R-06, A.5.19–A.5.22 | ISMS Owner | Supplier register with completed reviews |
| 2.6 | Enforce secure development basics: branch protection, mandatory code review, secrets scanning | A.8.25, A.8.28 | Head of Engineering | GitHub settings, sample reviewed PRs |
| 2.7 | Review Terraform for secure configuration baselines; document them | A.8.9 | Head of Engineering | Baseline document, review notes |

### Phase 3 (Months 6–9): Prove It Works and Certify

| # | Action | Addresses | Owner | Evidence for Auditor |
|---|---|---|---|---|
| 3.1 | Complete Statement of Applicability (justify each Annex A control as included or excluded) | Clause 6.1.3 | ISMS Owner | Approved SoA |
| 3.2 | Conduct internal audit of the ISMS (by someone independent of the work, e.g., external consultant) | Clause 9.2 | External or independent reviewer | Internal audit report |
| 3.3 | Hold management review meeting; log decisions and actions | Clause 9.3 | CEO | Meeting minutes |
| 3.4 | Fix internal audit findings; log corrective actions | Clause 10 | ISMS Owner | Corrective action log |
| 3.5 | Certification audit: Stage 1 (documentation review), then Stage 2 (evidence of operation) | R-04 | ISMS Owner | Certification body reports |
| 3.6 | AI governance workstream per Section 6 (model documentation, bias testing, drift monitoring) | R-03 | Head of Data Science | See Section 6 |
