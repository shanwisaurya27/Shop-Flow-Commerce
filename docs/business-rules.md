# Business Rules Document

**Project:** Shop Flow Commerce  
**Document ID:** BRULE-SF-001  
**Related BRD:** BRD-SF-001  
**Version:** 1.0  
**Status:** Draft

---

## Purpose

This document defines the approved business rules that must be followed for all calculations, status transitions, and reporting related to revenue, orders, returns, and refunds.

All Power BI reports, PostgreSQL views, and operational processes must adhere to these rules.

---

## Business Rules

| Rule ID | Business Rule | Rationale | Related Requirements |
|---------|---------------|-----------|----------------------|
| **BRULE-001** | Cancelled orders must not be counted as revenue. | Prevents inflated revenue figures. | BR-010, BR-011 |
| **BRULE-002** | A return awaiting warehouse inspection must not be treated as a completed cash refund. | Refunds are only final after inspection and acceptance. | BR-008, BR-009 |
| **BRULE-003** | A refund cannot exceed the amount paid for the returned units. | Protects against over-refunding. | BR-008, BR-010 |
| **BRULE-004** | Guest sessions must be included in conversion funnel analysis. | Gives a complete picture of visitor behaviour. | BR-001, BR-002, BR-003 |
| **BRULE-005** | Customer cohort month must be calculated using the first valid order date, not the signup date. | Aligns cohorts with actual purchasing behaviour. | BR-014 |
| **BRULE-006** | Month zero in customer cohort analysis is 100% by definition and must not be interpreted as a retention achievement. | Avoids misinterpretation of cohort charts. | BR-014 |
| **BRULE-007** | Revenue and refund calculations must follow the same approved definitions across all reports. | Ensures consistency between Finance, Marketing and Merchandising. | BR-010, BR-011, BR-017 |
| **BRULE-008** | Refund processing must follow warehouse acceptance and the applicable business rules. | Enforces process control and status accuracy. | BR-006, BR-007, BR-009 |

---

## Metric Definitions (Approved)

### Revenue
- Sum of order totals for orders that are **not cancelled**.
- Does **not** include refunded amounts.

### Total Orders
- Count of orders with status that qualifies as a valid completed/paid order (excluding cancelled).

### Average Order Value (AOV)
- `Revenue / Total Orders` (using the definitions above).

### Refunded Cash
- Sum of refund amounts only for returns that have reached **Refunded** status.
- Must not exceed the original paid amount for the returned units (BRULE-003).

### Return Rate
- Can be calculated at unit or order level.
- Formula must be explicitly documented in reports and use only approved statuses.

### Refund Processing Time
- Measured from the date the return status becomes **Requested** (or when the item is marked as received) until the status becomes **Refunded**.
- Only completed refunds are included in average processing time calculations.

---

## Return Status Lifecycle

```
Requested → In Transit → Inspecting → Refunded
                                 ↘ Declined
```

- Status updates are owned by the relevant team (Customer Support / Warehouse / Finance).
- A return can only move to **Refunded** after warehouse acceptance.

---

## Enforcement

- All analytical views in PostgreSQL must implement these rules.
- Power BI measures must reference the approved views or apply the same logic.
- Any deviation requires formal change request and re-approval of this document.
