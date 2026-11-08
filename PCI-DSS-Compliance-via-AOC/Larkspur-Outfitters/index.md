---
title: PCI-DSS Compliance via AOC
---

This project is a third-party risk review of a fictional payment processor, PayStream Solutions, for a fictional online retailer, Larkspur Outfitters, which wants to launch a subscription program with monthly recurring card charges. Working from PayStream’s PCI DSS Attestation of Compliance (AOC), I validated the document’s currency, standard version, and independent assessor, then compared the services Larkspur needs against the services the assessment actually covered. The review found that while PayStream is “Compliant” overall, its recurring billing service was never assessed, which leaves the most important service for the subscription program without independent assurance. I rated this gap as high inherent risk and recommended a conditional approval: launch one-time checkout and card-on-file storage now, hold recurring billing until the vendor provides evidence of its controls, use tokenization as a compensating control, and add contract requirements for incident notification and future assessment. With these actions in place, the residual risk drops to low.

## Sections
- [Summary and business context](01-summary-and-business-context.html)
- [Scope](02-scope.html)
- [Methodology](03-methodology.html)
- [AOC Validation findings](04-aoc-validation-findings.html)
- [Scope findings](05-scope-findings.html)
- [Risk Assessment](06-risk-assessment.html)
- [Recommendations](08-recommendations.html)
- [Appendix A](appendix-a.html) 
