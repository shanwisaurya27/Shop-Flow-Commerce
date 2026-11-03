# AS-IS / TO-BE Business Processes

**Project:** Shop Flow Commerce  
**Related BRD:** BRD-SF-001

---

## 1. Customer Purchase Process

### AS-IS
```
Customer visits website
        ↓
Looks through products
        ↓
May add items to cart
        ↓
May exit without purchase   ←── Drop-off (location unknown)
        ↓
Some customers complete purchase
```

**Problem:** No visibility into where customers abandon the funnel.

### TO-BE
```
Collect web sessions
        ↓
Track product views & cart events
        ↓
Analyse full purchase funnel
        ↓
Identify key drop-off points
        ↓
Compare Mobile vs Desktop behaviour
        ↓
Report insights to management
```

**Improvement:** Data-driven identification of conversion leaks.

---

## 2. Returns and Refunds Process

### AS-IS
```
Customer contacts support about return
        ↓
Information handled by separate teams
        ↓
No common Return ID between Warehouse & Finance
        ↓
Customer cannot track status
        ↓
Support handles repeated status queries
```

**Problem:** Low visibility, high support load, fragmented data.

### TO-BE
```
Customer requests return on eligible order
        ↓
Unique Return ID is generated
        ↓
Status updated throughout lifecycle:
  Requested → In Transit → Inspecting → Refunded / Declined
        ↓
Warehouse accepts & inspects item
        ↓
Refund processed only after acceptance (per business rules)
        ↓
Customer views live status of return & refund
```

**Approved Statuses:**

| Status      | Description                                      |
|-------------|--------------------------------------------------|
| Requested   | Return request initiated                         |
| In Transit  | Item on the way to the warehouse                 |
| Inspecting  | Warehouse inspecting the returned item           |
| Refunded    | Return accepted and refund completed             |
| Declined    | Return request declined                          |

**Improvement:** Self-service tracking + reduced support volume + clear ownership.

---

## 3. Business Reporting Process

### AS-IS
```
Different departments create their own reports
        ↓
Each team uses different calculation methods
        ↓
Revenue & refund numbers often do not match
        ↓
Management lacks a single reliable view
```

**Problem:** Inconsistent metrics and low trust in reports.

### TO-BE
```
Source data loaded into PostgreSQL
        ↓
Analytical views apply approved business rules
        ↓
All reports (Power BI) use the same definitions
        ↓
Figures can be reconciled back to source data
        ↓
Management receives consistent dashboards
```

**Improvement:** Single source of truth + reconcilable numbers + trusted decision-making.

---

## Process Ownership (TO-BE)

| Stage / Activity              | Primary Owner          |
|-------------------------------|------------------------|
| Return request creation       | Customer / Support     |
| Status: Requested → In Transit| Customer Support       |
| Status: In Transit → Inspecting | Warehouse           |
| Inspection decision           | Warehouse              |
| Refund execution              | Finance                |
| Metric definitions & reports  | Business Analyst + Finance |
| Funnel analysis               | Marketing / BA         |
