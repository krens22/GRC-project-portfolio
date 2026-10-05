# Third-Party Risk Review: VigilGrid Security Inc.
**SOC 2 Type II Report Review and Gap Analysis**

> *Portfolio project. All companies, people, and report contents are fictional.*


**Vendor**: VigilGrid Security Inc., a managed detection and response provider 
**Service requested**: Managed detection and response (MDR), a 24/7 security monitoring, alert investigation, and incident response support 
**Requesting business unit**: Meridian Security Team
**Customer organization**: Meridian Logistics, approx. 1,200 employees in Canada, US and Ireland
**Data and access involved**: Privileged agent on all Meridian endpoints and servers; endpoint activity data (logins, processes run, files accessed, network connections) transmitted to the vendor's US-hosted cloud and retained for 13 months
**Vendor risk tier**: Tier 1 (Critical); privileged access to every endpoint means a vendor compromise could give an attacker visibility into, or control over, Meridian's entire environment
**Review date**: October 5, 2026 
**Reviewer**: Karen Fernandes (TPRM Analyst)
**Report reviewed**: VigilGrid SOC 2 Type II report
**Report period**: 
**Criteria covered**: Security, Availability, Confidentiality (Processing, Integrity and Privacy not covered) 
**Status**: Draft

## 1. Engagement overview
**Business need:** Meridian's security team wants to outsource round-the-clock threat monitoring and response, because it lacks the staff to cover nights and weekends in-house.

**Why this vendor is rated Tier 1:**VigilGrid's agent runs with elevated privileges on every Meridian device and streams activity data off-site, so a failure at VigilGrid would directly expose Meridian's systems and employee activity data, including data about EU-based staff.
