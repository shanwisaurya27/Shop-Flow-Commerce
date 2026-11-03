# Acceptance Criteria

**Project:** Shop Flow Commerce  
**Related BRD:** BRD-SF-001  
**Version:** 1.0

The project (and individual deliverables) will be considered accepted when the following criteria are met.

---

## Overall Project Acceptance

1. Customer funnels can be reviewed using session data.
2. Customer drop-off points can be clearly highlighted.
3. Every return request has a unique Return ID.
4. The five approved return statuses (Requested, In Transit, Inspecting, Refunded, Declined) are captured and used.
5. Pending and completed refunds can be differentiated.
6. Refunded amounts are verified against the original payments for the returned products.
7. Refunds are excluded from revenue calculations.
8. Reported revenue and order figures reconcile with source data.
9. Category performance after refunds can be evaluated.
10. Customer cohort analysis and RFM segmentation can be repeated reliably.
11. Power BI reports use only the approved business logic and definitions.

---

## Detailed Acceptance by Area

### Funnel Analysis (BR-001 to BR-003)
- [ ] Session → View → Cart → Checkout → Purchase funnel is available
- [ ] Drop-off percentages are calculated at each stage
- [ ] Mobile vs Desktop comparison is present
- [ ] Guest sessions are included

### Return & Refund Visibility (BR-004 to BR-009)
- [ ] Unique Return ID generated for every request
- [ ] All five statuses are supported and transition correctly
- [ ] Customer-facing status history is available
- [ ] Pending vs completed refunds are distinguishable
- [ ] Refund processing time can be measured and outliers identified

### Metrics & Reconciliation (BR-010, BR-011, BR-017)
- [ ] Cancelled orders excluded from revenue
- [ ] Refunds only counted after final “Refunded” status
- [ ] Refund amount never exceeds original paid amount
- [ ] Source-to-report reconciliation is possible and documented

### Merchandising (BR-012, BR-013)
- [ ] Category contribution after refunds is calculable
- [ ] Return patterns (and reasons where available) are analysable

### Customer Analytics (BR-014, BR-015)
- [ ] Cohorts use first valid order date
- [ ] Month 0 = 100% and is clearly labelled
- [ ] Basic RFM scores and segments are available

### Reporting (BR-016)
- [ ] Four planned Power BI pages exist and use consistent measures
- [ ] Management can obtain a single consolidated view of performance

---

## Sign-off

| Role              | Name               | Date       | Signature |
|-------------------|--------------------|------------|-----------|
| Business Analyst  | Shanwi Saurya      |            |           |
| Project Reviewer  |                    |            |           |
| Business Owner    |                    |            |           |
