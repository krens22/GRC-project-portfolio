## Appendix D: Data Flow Diagram

<img width="1326" height="715" alt="image" src="https://github.com/user-attachments/assets/700cb4b9-d8d0-4357-9728-d90c1663f0c7" />


The diagram shows how EU employee data moves through the PeopleMetrics process:

1. **Dublin employees** (about 40) generate performance review ratings and goal data.
2. **Brightwell HR system** (hosted by CloudNimbus in Ireland) stores the data and sends the structured ratings and goal data to PeopleMetrics.
3. **PeopleMetrics data center** (United States) processes the data and generates performance scores. A boundary line marks the point where data leaves the EU, labeled "Cross-border transfer: Standard Contractual Clauses required (F-04)."
4. **Scores** are returned to HR and line managers, who review them before use (F-05).

Mark each point where a finding applies: the transfer (F-04), the score step with no review (F-05), the retention period at PeopleMetrics (F-06), and the free-text comments that should no longer be sent (F-12).
