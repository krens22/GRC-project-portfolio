# Methodology

Key terms
•	Control: a specific safeguard a company puts in place, such as requiring multi-factor authentication.
•	Requirement: a rule written in a framework, such as PCI DSS Requirement 8. A 
•	control is how a company meets a requirement.
•	Mapping: a link between one control and the framework requirements it helps satisfy.
How mappings were made
1.	Each control was described in plain language first (for example, “only authorized people can access systems”).
2.	The official text of each framework was searched for requirements covering the same goal.
3.	Each link was rated by how completely the control satisfies the requirement (see below).


| Rating | Meaning | Example |
| :--- | :--- | :--- |
| **Full** | The control directly satisfies the requirement as written. | Enforcing MFA for all users satisfies ISO 27001 A.8.5 (secure authentication). |
| **Partial** | The control helps, but the requirement needs additional controls or evidence. | MFA supports GDPR Article 32, but Article 32 also expects other measures such as encryption and the ability to restore data. |
| **No direct mapping** | The framework has no requirement that clearly matches. | Used sparingly. |

How to read the table
Each row is one control. Read across the row to see which requirement in each framework that control supports. A requirement ID such as “CC6.1” is a reference number, and the full requirement text is in the official framework document.

**A note on GDPR :**
SOC 2, ISO 27001, and PCI DSS list specific criteria or controls. GDPR is a law that asks for “appropriate” security without a checklist, so GDPR mappings will most often be rated Partial.
Limitations of the method
Mappings reflect the author’s interpretation of the official text. A real audit depends on the organization’s scope, the auditor’s judgment, and the evidence provided.
