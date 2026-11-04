# Payment Vendor Review: PayStream Solutions (PCI DSS AOC)

## 1. Review Summary

| | |
|---|---|
| **Requestor** | E-commerce Team, Larkspur Outfitters |
| **Vendor** | PayStream Solutions (payment gateway) |
| **Business need** | Launch a subscribe-and-save program with monthly recurring card charges |
| **Services requested** | One-time card processing, card-on-file storage, recurring billing |
| **Document reviewed** | PCI DSS Attestation of Compliance (AOC) for Service Providers |
| **Reviewer** | Karen Fernandes |
| **Review date** | November 4, 2026 |
| **Decision** | *To be completed after the review* |

> **Note:** This is a fictional scenario created for portfolio purposes. The vendor, company, and AOC are not real.

## 2. Problem and Business Context

Larkspur Outfitters plans to launch a subscribe-and-save program that automatically charges customers' saved payment cards every month. To do this, the company would send cardholder data to PayStream Solutions, a third-party payment gateway. If PayStream's security controls don't cover the services Larkspur plans to use, a breach at the vendor could expose customer card data, trigger card brand fines, and damage customer trust. Before onboarding, this review checks whether PayStream's PCI DSS compliance actually covers recurring billing, not just payment processing in general.
