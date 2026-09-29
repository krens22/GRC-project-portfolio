<details>
<summary>Footnotes</summary>
<p>
- The SoA is the single most important document in an ISO 27001 audit. 
- It's the master list of all 93 Annex A controls where Northbridge states, for each one: is it applicable, why or why not, and what's the implementation status.
- Auditors use it as their checklist during certification — if a control is marked "applicable" in the SoA but there's no evidence it's actually implemented, that's an audit finding. If a control is marked "not applicable" with a weak justification, the auditor will challenge it directly.
- The key discipline of an SoA: every "Not Applicable" needs a real reason tied to the business, not a shortcut to avoid work. "Not applicable because we don't do X" is fine. "Not applicable because it's hard" is not — and auditors are trained to spot the difference.
  
- Why A.7 (Physical) is "Not Applicable" here, but justified through inheritance, not exclusion. This is a common and defensible pattern for cloud-only companies: Northbridge doesn't own physical infrastructure, so it can't implement physical controls directly — but it isn't off the hook. The justification explicitly says physical security is inherited from AWS's own certifications. A weak SoA would just say "N/A — we're cloud-based" and stop there; a strong one says where that responsibility now sits, because an auditor's next question is always "how do you know AWS actually has that covered?" — the answer being a supplier review (A.5.19-22), which is why that control is marked Yes.

- Why some rows say "Unable to Assess → In Progress" instead of picking one. The SoA is a living document across the whole 9-month project, not a single point-in-time snapshot. Where Section 3 found "Unable to Assess" because information was genuinely missing, the SoA tracks that the investigation itself is a Phase 2 action item — it shows the reader not just where things stand today, but that there's a plan to resolve the unknowns, not just a shrug.
</p>
</details>

## Appendix — Statement of Applicability

| Control | Control Name | Applicable? | Justification | Implementation Status |
|---|---|---|---|---|
| A.5.1 | Policies for information security | Yes | Required — no policy currently exists; foundational to ISMS | Not Started → In Progress (Phase 1) |
| A.5.2 | Information security roles and responsibilities | Yes | Required — currently informal, single point of failure | Not Started → In Progress (Phase 1) |
| A.5.7 | Threat intelligence | No | Northbridge's threat exposure is adequately covered via AWS's native threat intelligence services (e.g., GuardDuty) given its cloud-only infrastructure; a dedicated internal threat intel function is disproportionate to company size and risk profile | N/A |
| A.5.15 | Access control | Yes | Required — no documented access control policy exists | Not Started → In Progress (Phase 1) |
| A.5.18 | Access rights | Yes | Required — no access review process exists | Not Started → In Progress (Phase 1) |
| A.5.19–A.5.22 | Supplier relationships | Yes | Required — Northbridge is materially dependent on AWS and Okta; no supplier review process exists | Not Started → In Progress (Phase 2) |
| A.5.23 | Information security for use of cloud services | Yes | Directly applicable — Northbridge's entire production environment is AWS-hosted | Partial (relies on AWS shared responsibility model, not formally documented internally) |
| A.5.24 | Incident management planning and preparation | Yes | Required — prior vendor review already flagged this gap; unremediated | Not Started → In Progress (Phase 2) |
| A.5.31 | Legal, statutory, regulatory and contractual requirements | Yes | Required — Northbridge processes financial data for regulated clients (PIPEDA and sector-specific obligations apply) | Not Started |
| A.6.1 | Screening | Yes | Partially implemented — background checks exist, formal policy does not | Partial |
| A.6.3 | Information security awareness, education and training | Yes | Required — no training program exists | Not Started → In Progress (Phase 2) |
| A.6.5 | Responsibilities after termination or change of employment | Yes | Required — confirmed real-world failure (un-revoked access) | Not Started → In Progress (Phase 1) |
| A.6.6 | Confidentiality or non-disclosure agreements | Yes | Assumed standard employment agreements exist; formal NDA coverage for contractors needs confirmation | Unable to Assess |
| A.7.1–A.7.14 | Physical controls (full set) | No | Northbridge is remote-first with no owned office or data center; physical infrastructure is entirely managed by AWS under its own ISO 27001/SOC 2 certifications | N/A (inherited via cloud provider) |
| A.8.1 | User endpoint devices | Yes | Required — no device management policy for a remote workforce using mixed personal/company devices | Not Started → In Progress (Phase 2) |
| A.8.2 | Privileged access rights | Yes | Required — legacy tools sit outside centralized access control | Partial → In Progress (Phase 1) |
| A.8.5 | Secure authentication | Yes | Required — Okta SSO covers most but not all systems | Partial → In Progress (Phase 1) |
| A.8.9 | Configuration management | Yes | Required — Terraform in use, but baseline enforcement unconfirmed | Unable to Assess → In Progress (Phase 2) |
| A.8.15 | Logging | Yes | Required — no confirmed logging/monitoring capability | Unable to Assess → In Progress (Phase 2) |
| A.8.16 | Monitoring activities | Yes | Required — company cannot confirm absence of past incidents | Not Started → In Progress (Phase 2) |
| A.8.24 | Use of cryptography | Yes | Directly applicable — client financial data requires encryption in transit and at rest; current implementation status needs technical confirmation | Unable to Assess |
| A.8.25 | Secure development life cycle | Yes | Required — CI/CD pipeline exists but enforcement practices unconfirmed | Unable to Assess → In Progress (Phase 2) |
| A.8.28 | Secure coding | Yes | Required — same rationale as A.8.25 | Unable to Assess → In Progress (Phase 2) |
| A.8.34 | Protection of information systems during audit testing | Yes | Applicable in preparation for the Stage 2 certification audit | Not Started (Phase 3) |

*Note: this is a representative subset, not the full 93-control list — a real SoA would cover every control.*
