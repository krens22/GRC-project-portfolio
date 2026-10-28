## Section 5: Data Protection Impact Assessment: PeopleMetrics

### 5.1 Purpose and Reason for the Assessment

A Data Protection Impact Assessment (DPIA) is a structured review of whether a way of using personal data creates a high risk to the people the data is about, and what is done to reduce that risk. GDPR requires one before processing begins when the processing is likely to result in a high risk to individuals.

This DPIA was triggered by the vendor assessment in Section 3. PeopleMetrics meets several of the triggers in Section 1.5 at once. It systematically evaluates employees through automated scoring, it processes data about employees, who are in a weaker position than customers because they cannot easily object to what their employer does, and it transfers EU data to the United States. Any one of these would justify a closer look. The combination makes a DPIA required.

### 5.2 Description of the Processing

Brightwell uses PeopleMetrics to analyze performance data for its EU-based employees and to generate performance scores. The scores are used by HR and line managers to inform promotion and pay discussions. The purpose is to make those decisions more consistent across the organization.

| Element | Description |
|---|---|
| Data subjects | About 40 employees at the Dublin office |
| Data categories | Name, employee ID, job title, manager, performance review ratings, goal completion data, and manager comments |
| Special category data | None intended, but free-text manager comments could contain health or other sensitive information |
| Recipients | HR team, line managers, PeopleMetrics, and PeopleMetrics's subcontractors |
| Storage location | PeopleMetrics data centers in the United States |
| Retention | No defined period; data is kept until the contract ends |
| Legal basis | Legitimate interests of Brightwell (consent is not suitable in an employment relationship, because employees cannot freely refuse) |

### 5.3 Necessity and Proportionality

**Lawful basis.** Legitimate interests require a balancing test showing that Brightwell's interest in consistent performance management is not outweighed by employees' rights. That test has not yet been documented and must be completed before processing continues.

**Data minimization.** Only data needed to produce a performance score should be sent. Brightwell does not need to send full manager comments to achieve this, and should send structured ratings and goal data only.

**Transparency.** Review of Brightwell's current employee privacy notice found that it does not mention PeopleMetrics, automated scoring, or the transfer to the US. Employees have therefore not been told how their data is used. This is an internal Brightwell gap and is not a vendor finding. It is recorded as F-11 in Section 4.

**Employee rights.** Employees can ask for access to their data, ask for corrections, and object to processing. They also have the right not to be subject to a decision based solely on automated processing where it significantly affects them, which includes decisions on promotion and pay. Brightwell has no process for handling such requests as they relate to PeopleMetrics.

**Alternatives.** Brightwell could use the existing review process without automated scoring. The scoring adds consistency, but it is not essential, and this is why human review and employee notice are required conditions, not optional improvements.

### 5.4 Risks to Individuals

Risks are rated using the method in Section 4.1, focusing on the effect on employees and not on Brightwell.

| ID | Risk to individuals | Related finding | L | I | Rating |
|---|---|---|---|---|---|
| R1 | EU employee data transferred to the US without a legal safeguard, with possible access by US authorities | F-04 | 3 | 3 | **Critical** |
| R2 | Inaccurate or biased scores lead to unfair promotion or pay outcomes with no human check | F-05 | 2 | 3 | **High** |
| R3 | Employees are unaware of the processing and cannot exercise their rights | F-11 | 3 | 2 | **High** |
| R4 | Delayed breach notice leaves employees unable to protect themselves, for example from fraud or phishing | F-07 | 2 | 3 | **High** |
| R5 | Data kept longer than needed increases exposure and breaches the storage limitation principle | F-06 | 2 | 2 | Medium |
| R6 | Sensitive information in free-text comments is stored and exposed | F-12 | 1 | 3 | Medium |

### 5.5 Measures to Reduce the Risks

| Risk | Measures | Residual rating |
|---|---|---|
| R1 | Execute Standard Contractual Clauses (or confirm PeopleMetrics's certification under the EU-US Data Privacy Framework). Complete a transfer impact assessment. Require encryption of data at rest and restrict vendor staff access. | Medium |
| R2 | Require a manager to review every score before it informs a decision. Give employees the right to contest a score. Ask PeopleMetrics for documentation of how scores are calculated and tested for bias. | Medium |
| R3 | Update the employee privacy notice to name PeopleMetrics, describe the scoring, and state the US transfer. Inform employees and their representatives before further processing. Create a process for handling rights requests. | Low |
| R4 | Amend the contract to require breach notice within 48 hours of the vendor becoming aware. Align Brightwell's incident procedure so that employees are told promptly. | Medium |
| R5 | Set a retention period in the data processing agreement: current and previous two review cycles only, with deletion within 90 days of an employee leaving. | Low |
| R6 | Stop sending free-text comments to PeopleMetrics. Give managers guidance on what not to record. | Low |

### 5.6 Conclusion and Residual Risk

With the measures in 5.5 in place, no residual risk is above Medium, and consultation with the Irish Data Protection Commission under Article 36 is not required. This conclusion depends on the measures actually being implemented. If the Standard Contractual Clauses are not signed within the 30-day deadline in Section 4, R1 remains Critical, and Brightwell must either stop sending EU employee data to PeopleMetrics or consult the supervisory authority before continuing.

**Decision:** Processing may continue on condition that the measures are completed within the Section 4 timelines: R1 within 30 days, R2, R3, and R4 within 60 days, and R5 and R6 within 90 days.

### 5.7 Review and Sign-Off

The Privacy Lead has sought the views of the EU HR Manager and of employee representatives, and has recorded them with this DPIA. The DPIA is reviewed after twelve months, or earlier if PeopleMetrics changes what data it processes, where it stores it, or how scores are produced.

| Role | Name | Date |
|---|---|---|
| Prepared by: Third-Party Risk Analyst | | October 2026 |
| Reviewed by: Privacy Lead | | |
| Approved by: EU HR Manager (business owner) | | |

---
