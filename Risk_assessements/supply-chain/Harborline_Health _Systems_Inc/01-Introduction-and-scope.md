# 1. Introduction and Scope
<details>
  <summary>Notes</summary>
  <p>why does this report exist, what does it cover, what doesn't it cover, and what should I keep in mind while reading it?.</p>
</details>


## 1.1 Purpose
Harborline relies on third-party suppliers and vendors  for storing and processing approx. 1.5 million patient information on their platform from cloud hosting to security providers. Because this data is protected under Ontario's Personal Health Information Protection Act **(PHIPA)**, a failure at any supplier could create legal and privacy consequences for Harborline and its customers. This report aims to assess cybersecurity and privacy risks that could potentially arise from these vendors so that leadership can properly manage them and make informed descisions. 

## 1.2 Objectives
This assessment aims to:
- Build an inventory of all current suppliers and their roles and data access.
- Categorize the suppliers by criticality based on importance to platform operations, data sensitivity and what kind of access they hold to it.
- Score the risks
- Identify the control gaps
- Recommend a prioritized action plan with owners and timelines.

## 1.3 Scope

### 1.3.1 In scope
- **Suppliers:** Harborline's supplier inventory contains 12 suppliers. Eleven that support the patient platform are in scope; provisioning servers, databases, storage, networking  the video call engine, SMS/email delivery, subscription and payment services, managed security, MFA and SSO, software development, backups and recovery, product analysis, hardware and all open source software dependencies.
- **Systems and data:** The patient platform(appointment booking, reminders, and virtual visits); patient data (names, contact details, health card numbers, appointment history, video visit metadata); staff and clinic user credentials; source code; and backups.
- **Risk categories:** cyber, privacy, continuity, compliance
- **Assessment period:** September 2026

### 1.3.2 Out of scope
- Technical tests( penetration or vunerability): this assessment relies on documentation and questionnaires.
- Financial or credit risk.
- Suppliers not supporting the patient platform - employee payroll platform(PayrollPoint HR)

## 1.4 Assumptions and Limitations
- Supplier questionnaire responses are assumed to be accurate and complete.
- The assessment is a point-in-time snapshot (September 2026); supplier risks may change after this date.

## 1.5 Intended Audience
1. CISO - Descide which risks to treat and in what order.
2. Risk Commitee - Oversee the risk position and approve the plan.
3. Director of Procurement - Update supplier contracts.
4. IT Operations - Carry out technical follow-up actions.
5. Privacy Officer(B) - Confirm alignment with PHIPA and PIPEDA.


