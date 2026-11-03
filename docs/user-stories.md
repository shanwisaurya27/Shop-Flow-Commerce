# User Stories

**Project:** Shop Flow Commerce  
**Related BRD:** BRD-SF-001  
**Version:** 1.0

These user stories translate the Business Requirements into development-ready items.

---

## Funnel Analysis

### US-FUN-001 – Conversion Funnel Visibility
**As a** Marketing / Business Analyst  
**I want** to see session-level conversion rates at each stage of the browse-to-buy funnel  
**So that** I can identify the biggest drop-off points and prioritise improvements.

**Acceptance Criteria:**
- Funnel stages include at least: Session → Product View → Add to Cart → Checkout → Purchase
- Guest sessions are included (BRULE-004)
- Drop-off rates are calculated and visualised
- Comparison by device (Mobile vs Desktop) is available (BR-003)

**Related Requirements:** BR-001, BR-002, BR-003

---

## Return & Refund Visibility

### US-REF-001 – Customer Return Tracking
**As a** Customer  
**I want** a unique Return ID and real-time status of my return  
**So that** I do not need to contact support for basic status updates.

**Acceptance Criteria:**
- Every return request generates a unique Return ID (BR-005)
- Statuses follow the approved list: Requested, In Transit, Inspecting, Refunded, Declined
- Customer can view the full journey from request to final decision
- Pending vs completed refunds are clearly distinguished

**Related Requirements:** BR-004, BR-005, BR-006, BR-007, BR-008, BR-009

### US-REF-002 – Refund Cycle Time Monitoring
**As a** Operations / Finance Manager  
**I want** to see average and outlier refund processing times  
**So that** I can identify delays and improve SLA compliance.

**Acceptance Criteria:**
- Processing time is measured according to BRULE-008
- Delayed returns can be filtered / highlighted
- Only returns that reached “Refunded” status are included in completed metrics

---

## Metrics & Reconciliation

### US-MET-001 – Consistent Commercial Metrics
**As a** Finance / Management user  
**I want** revenue, orders, AOV and refunded cash to follow a single approved definition  
**So that** all reports are consistent and reconcilable to source data.

**Acceptance Criteria:**
- Cancelled orders are excluded from revenue (BRULE-001)
- Refunds only appear after warehouse acceptance and final status (BRULE-002)
- Refund amount ≤ original paid amount for returned units (BRULE-003)
- Reported figures can be reconciled against source tables

**Related Requirements:** BR-010, BR-011, BR-017

---

## Merchandising

### US-MER-001 – Category Performance After Refunds
**As a** Merchandising Manager  
**I want** to see category sales and contribution after accounting for refunds  
**So that** I understand true net performance of each category.

**Acceptance Criteria:**
- Gross sales and net contribution (after refunds) are shown
- Return patterns and reasons are available (where data exists)
- Figures use approved metric definitions

**Related Requirements:** BR-012, BR-013

---

## Customer Analytics

### US-CUS-001 – Cohort & RFM Analysis
**As a** Marketing / CRM Analyst  
**I want** customer cohort retention and basic RFM segmentation  
**So that** I can understand retention behaviour and segment customers for targeting.

**Acceptance Criteria:**
- Cohort month is based on first valid order date (BRULE-005)
- Month 0 is always 100% and clearly labelled (BRULE-006)
- RFM scores (Recency, Frequency, Monetary) are calculated and segmentable

**Related Requirements:** BR-014, BR-015

---

## Reporting

### US-REP-001 – Management Dashboard
**As a** Business Owner / Management  
**I want** a consolidated Power BI dashboard using approved definitions  
**So that** I can make decisions based on consistent, trustworthy numbers.

**Acceptance Criteria:**
- Dashboard pages cover: Executive Overview, Merchandising, Customers, Funnel & Refund Operations
- All measures use the same approved business logic
- Key KPIs are visible at a glance

**Related Requirements:** BR-016, BR-017
