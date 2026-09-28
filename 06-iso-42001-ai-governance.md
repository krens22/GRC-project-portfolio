## Gap Analysis: ISO 42001 AI Governance
<details>
  <summary>Footnotes</summary>
  <p>
- ISO 42001 asks a different question about the same AI system: is the AI's behavior understood, monitored, and accountable?
- A system can be perfectly secure (locked down, encrypted, access-controlled) and still be an ungoverned AI risk — nobody tested it for bias, nobody can explain why it flagged a specific transaction, nobody's watching whether its accuracy is degrading over time. That's the gap 42001 exists to close.
  </p>
</details>

| Control Area | Requirement | Finding Reference | Rating | Justification |
|---|---|---|---|---|
| AI Risk Assessment | Formal assessment of AI system risks and impacts | No risk/impact assessment ever conducted | Not Started | No process exists to evaluate risks the model poses, despite 18 months in production making high-stakes financial decisions. This is the foundational control — without it, none of the downstream controls (bias testing, monitoring) have anywhere to anchor their priorities. |
| System Documentation | Documented intended use, limitations, and data provenance | No model documentation exists | Not Started | No record of what the model is meant to do, what it shouldn't be used for, or where its training data came from. This creates both an audit problem (nothing to show a certifier) and an operational one (institutional knowledge lives only in the data science team's memory). |
| Data Quality & Bias | Testing for bias/fairness in training data and outputs | No bias or fairness testing performed | Not Started | Given the model influences underwriting/fraud decisions about real people, undetected bias could mean systematically disadvantaging certain groups — a real legal and reputational exposure, not just a technical one. |
| Model Monitoring | Ongoing monitoring for performance/drift over time | No drift monitoring or retraining schedule | Not Started | A model trained on data from ~18+ months ago may no longer reflect current transaction patterns. Without monitoring, degraded accuracy would go unnoticed until it caused a visible bad outcome. |
| Human Oversight | Defined human review/override capability for AI-driven decisions | Unclear whether human review exists before model output affects a decision | Unable to Assess | This needs direct confirmation from Northbridge — it's the single most important open question in this whole section, since "fully automated, no human review" vs. "model output is one input a human considers" are very different risk profiles. |
| Explainability / Redress | Mechanism for affected individuals to contest or seek explanation | No such mechanism described | Not Started | For clients in the financial/insurance sector, this connects directly to existing regulatory expectations around explainable adverse decisions (e.g., adverse action notices in lending-adjacent contexts) — this isn't just an AI best practice, it may be a legal requirement depending on how the output is used downstream. |
