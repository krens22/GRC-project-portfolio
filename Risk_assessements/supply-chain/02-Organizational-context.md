# 2. Organizational Context

## 2.1 Company Profile
Harborline Health Systems Inc. is a Toronto-based provider of a cloud platform for online appointment booking, patient reminders, and virtual care visits. Founded in 2017, it employs approx. 250 people and serves about 400 clinics across Ontario.

## 2.2 Services and Technology Overview
The platform is hosted in a public cloud in a Canadian data region, and uses a microservices architecture that incorporates a large number of open-source software libraries. Staff and clinic users sign in through single sign-on with multi-factor authentication. The platform also allows patients to book appointments online, receive reminder notifications by text message or email and schedule virtual visits via video. Patient data is backed up daily and a disaster recovery plan is tested annually. Harborline's engineering team is supplemented by an offshore software development contractor. Any code submitted by this contractor is reviewed by Harborline engineers before release to the production platform.


## 2.3 Data Handled
- Patient names, contact details, and Ontario health card numbers (High sensitivity)
- Appointment history and visit type (High sensitivity)
- Video visit metadata (times, durations, participants); Harborline does not record call content (Medium sensitivity)
- Clinic staff login details
- Payment data, handled through the payment processor; card details are not stored in full by Harborline (High sensitivity)
  
## 2.4 Regulatory and Contractual Obligations
1. PHIPA: Harborline acts as an electronic service provider for clinics, which are responsible for their patients' health information. Harborline must protect this data and support its customers' compliance.
- PIPEDA: applies to Harborline's commercial activities.
- Customer contracts: many clinics require timely breach notification and evidence of security controls.
- Security frameworks: Harborline has completed a SOC 2 Type I report and is working toward ISO 27001 certification.
  
## 2.5 Why Supplier Risk Matters to Harborline
Harborline does not operate its platform alone. Hosting, video, messaging, payments, identity, managed security, development support, and backups are all provided by external suppliers, several of which handle patient data or hold privileged access. A failure at any one of them could interrupt operation at hundreds of clinics or compromise health records.

## 2.6 Governance and Current Third-Party Risk Practices
| Role  |  Responsibility  |  
| -------- | -------- | 
| CISO | Owns security and this assessment  |  
| Head of GRC | Reviews the report |    
| Director of IT Operations | Manages technical supplier relationships |
| Director of Procurement | Manages supplier contracts/relationships |    
| Privacy Officer  |  Oversees PHIPA and PIPEDA complaince  |    

### 2.6.2 Current practices

At the time of this assessment, supplier risk is managed as follows:

- Procurement maintains a supplier list in a spreadsheet.
- Security questionnaires are sent to new suppliers during onboarding.
- Suppliers are not currently grouped by criticality.
- Contract terms, including incident notification requirements, vary by supplier.
- Supplier access to Harborline systems is reviewed informally rather than on a fixed schedule.
- Open-source software components are not tracked in a structured inventory.

