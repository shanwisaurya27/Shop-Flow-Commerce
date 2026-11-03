# KPI Definitions

**Project:** Shop Flow Commerce  
**Related BRD:** BRD-SF-001  
**Must follow:** Business Rules (BRULE-001 → BRULE-008)

All KPIs used in reports and dashboards must use these definitions.

---

| KPI | Definition | Formula / Logic | Notes |
|-----|------------|-----------------|-------|
| **Browse-to-Buy Conversion Rate** | % of sessions that result in a purchase | (Sessions with ≥1 purchase) / (Total sessions) × 100 | Includes guest sessions |
| **Add-to-Cart Rate** | % of sessions that add at least one item to cart | (Sessions with cart activity) / (Total sessions) × 100 | |
| **Cart Abandonment Rate** | % of carts that do not convert to an order | (Carts without purchase) / (Total carts) × 100 | |
| **Revenue** | Eligible order revenue | Sum of order totals where order is **not cancelled** | BRULE-001 |
| **Total Orders** | Number of valid orders | Count of non-cancelled orders | |
| **Average Order Value (AOV)** | Average revenue per valid order | Revenue / Total Orders | |
| **Refunded Cash** | Amount of completed refunds | Sum of refund amounts where return status = **Refunded** | BRULE-002, BRULE-003 |
| **Return Rate** | Proportion of purchased units/orders that were returned | Returned units (or orders) / Sold units (or orders) | Document whether unit- or order-based |
| **Refund Processing Time** | Time to complete a refund | Date(Refunded) – Date(Requested or Received) | Only completed refunds |
| **Customer Retention Rate** | % of customers who purchase again in a later period | Cohort-based retention | Month 0 = 100% (BRULE-006) |
| **Category Contribution After Refunds** | Net performance of category | Category Gross Sales – Category Refunded Amount | |

---

## Implementation Guidance

- Prefer calculating these measures in PostgreSQL views, then consume in Power BI.
- If calculated in Power BI, the DAX must mirror the business rules exactly.
- Always display the definition (or a link to it) in report tooltips or documentation page.
