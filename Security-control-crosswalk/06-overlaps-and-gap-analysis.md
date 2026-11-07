## Overlaps and Gaps Analysis

### Rating summary

| Framework | Direct | Supporting |
|---|---|---|
| SOC 2 | 10 | 0 |
| ISO 27001:2022 | 10 | 0 |
| PCI DSS v4.0.1 | 9 | 1 |
| GDPR | 4 | 6 |

### Where the frameworks overlap

All 10 controls map to at least three of the four frameworks, which confirms the main idea of a crosswalk: one control can serve several audits. Three controls are rated Direct in all four frameworks: **encryption, incident response, and vendor management**. Implementing these once covers the most ground, so a team with limited time should start there.

SOC 2 and ISO 27001 line up closely with the control-based approach used here, with all 10 controls rated Direct in both. This is because both frameworks are built around controls an organization chooses and operates.

### Where the frameworks differ

**Level of detail.** PCI DSS is prescriptive, meaning it gives specific rules. Requirement 8.4, for example, spells out exactly where multi-factor authentication is required. GDPR sits at the other extreme. It asks for "appropriate" security measures and leaves the organization to decide what that means. For the same MFA control, PCI says exactly what to do, while GDPR only supports it through Article 32.

**GDPR is outcome-based.** Only 4 of 10 controls are Direct under GDPR (encryption, incident response, vendor management, and backup), and in each of these cases the regulation names the measure or its outcome explicitly. For the other six, GDPR defers to "appropriate" measures, so an organization needs SOC 2, ISO 27001, or PCI DSS to supply the technical detail.

**PCI DSS has a backup gap.** Backup and recovery is the only control rated Supporting under PCI DSS. PCI focuses on protecting card data, so it has no general backup requirement, while GDPR Article 32(1)(c) names the ability to restore data explicitly. An organization that follows PCI alone could still fall short of GDPR on this point.

**The frameworks are different kinds of things.** SOC 2 is an audit report, ISO 27001 is a certification, PCI DSS is a contractual industry standard, and GDPR is a law. Meeting a requirement therefore carries different consequences: a failed SOC 2 control becomes an audit exception, while a GDPR failure can lead to regulatory fines.

### What this crosswalk does not show

- **Management system requirements.** ISO 27001 requires more than controls. It also requires a risk assessment, a documented scope, management review, and a Statement of Applicability (a document listing which Annex A controls apply and why). Implementing these 10 controls would not by itself earn certification.
- **Privacy obligations.** GDPR covers much more than security: a lawful basis for processing, individuals' rights to access and delete their data, and impact assessments for risky processing. A security control crosswalk addresses only the security side.
- **Depth of implementation.** A "Direct" rating means the control addresses the requirement. It does not mean the control is implemented well enough to pass an audit.
