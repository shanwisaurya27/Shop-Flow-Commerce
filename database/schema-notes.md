# PostgreSQL Schema Notes

**Project:** Shop Flow Commerce  
**Related BRD:** BRD-SF-001

This document captures the expected core entities and relationships for the analytical layer. Actual table names and columns should be aligned with the provided synthetic datasets.

---

## Core Entities (Expected)

| Entity          | Purpose                                      | Key Fields (examples)                          |
|-----------------|----------------------------------------------|------------------------------------------------|
| customers       | Customer master                              | customer_id, signup_date, ...                  |
| sessions        | Web sessions (including guests)              | session_id, customer_id (nullable), device, start_ts, ... |
| products        | Product catalogue                            | product_id, category, ...                      |
| orders          | Order header                                 | order_id, customer_id, order_date, status, total_amount, ... |
| order_items     | Line items                                   | order_item_id, order_id, product_id, qty, unit_price, ... |
| returns         | Return requests                              | return_id, order_id, status, requested_at, ... |
| refunds         | Completed / pending refunds                  | refund_id, return_id, amount, status, processed_at, ... |

---

## Recommended Analytical Views

Create views (or materialized views) that enforce the business rules:

1. **vw_valid_orders**  
   - Excludes cancelled orders (BRULE-001)

2. **vw_revenue**  
   - Sum of valid order totals

3. **vw_completed_refunds**  
   - Only refunds linked to returns in “Refunded” status (BRULE-002)

4. **vw_funnel_events**  
   - Session → View → Cart → Checkout → Purchase events (include guests – BRULE-004)

5. **vw_customer_cohorts**  
   - First valid order date as cohort month (BRULE-005)

6. **vw_rfm_scores**  
   - Recency, Frequency, Monetary per customer

7. **vw_return_status_timeline**  
   - Current and historical status of each return_id

8. **vw_category_contribution**  
   - Gross sales, refunded amount, net contribution by category

---

## Data Quality Checks (Recommended)

- Uniqueness of return_id, order_id, session_id, customer_id
- Refund amount ≤ sum of paid amounts for returned units
- No revenue from cancelled orders
- Status transitions follow the approved lifecycle
- Null handling for guest sessions

---

## Notes

- All calculations in Power BI should preferably consume these views rather than raw tables.
- Document any deviations from the expected schema when the actual datasets are explored.
