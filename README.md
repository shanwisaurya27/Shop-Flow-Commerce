# Shop Flow Commerce

**Business Analysis & Data Analytics Project**  
**Document ID:** BRD-SF-001 | **Version:** 1.0 | **Status:** Draft

Shop Flow Commerce is a mid-sized e-commerce platform selling products across **Fashion**, **Electronics**, **Home**, and **Beauty**.  

This repository contains the complete Business Requirements Document (BRD) and supporting artifacts for analyzing customer conversion, return/refund visibility, and consistent commercial reporting using **PostgreSQL** + **Power BI**.

---

## 🎯 Project Goals

| ID | Objective |
|----|-----------|
| BO-001 | Identify customer drop-off points in the browse-to-buy funnel |
| BO-002 | Improve return & refund status visibility |
| BO-003 | Establish common business definitions for revenue, orders & refunds |
| BO-004 | Reconcile business reports with source data |
| BO-005 | Analyze category performance adjusted for refunds |
| BO-006 | Analyze customer retention and buying behavior |
| BO-007 | Generate reliable management reports |

---

## 📁 Repository Structure

```
shop-flow-commerce/
├── README.md                          # This file
├── docs/
│   ├── BRD-SF-001.docx                # Original Business Requirements Document
│   ├── BRD-SF-001.md                  # Markdown version of the BRD
│   ├── business-rules.md              # Approved business rules (BRULE-001 → 008)
│   ├── user-stories.md                # Development-ready user stories
│   ├── as-is-to-be-processes.md       # Current vs proposed processes
│   └── acceptance-criteria.md         # Formal acceptance criteria
├── wireframes/
│   ├── return-tracking.md             # Customer return status tracking screens
│   └── powerbi-dashboard.md           # Proposed Power BI report pages
├── database/
│   └── schema-notes.md                # PostgreSQL data model notes
├── reports/
│   └── kpi-definitions.md             # KPI definitions & calculation logic
└── assets/                            # Images / diagrams (optional)
```

---

## 🔑 Key Business Problems

1. **Conversion Leakage** – Shoppers browse but abandon carts / never purchase.
2. **Opaque Returns & Refunds** – Customers cannot track return status; support handles repetitive queries.
3. **Inconsistent Metrics** – Finance, Marketing & Merchandising calculate revenue/refunds differently.

---

## 📊 Proposed Solution Overview

| Layer | Tool | Purpose |
|-------|------|---------|
| Data Storage & Analysis | PostgreSQL | Clean, consistent analytical views |
| Visualization | Power BI | Executive, Merchandising, Customer & Operations dashboards |
| Process | Standardized Return Statuses | Requested → In Transit → Inspecting → Refunded / Declined |
| Governance | Business Rules + Common Definitions | Single source of truth for metrics |

### Approved Return Statuses
| Status | Description |
|--------|-------------|
| Requested | Return request initiated |
| In Transit | Item on the way to warehouse |
| Inspecting | Warehouse inspecting the item |
| Refunded | Return accepted & refund completed |
| Declined | Return request declined |

---

## 📈 Power BI Report Pages (Planned)

1. **Executive Overview** – Revenue, Orders, AOV, Refunded Cash
2. **Merchandising** – Category sales, returns, contribution after refunds
3. **Customers** – Cohort retention + RFM segmentation
4. **Funnel & Refund Operations** – Conversion funnel, pending refunds, processing time

---

## 🚀 Getting Started (for contributors)

1. Clone the repository
2. Read `docs/BRD-SF-001.md` for full context
3. Review business rules and user stories before implementation
4. Use the wireframes as a reference for UI / dashboard design
5. Follow the acceptance criteria for validation

```bash
git clone https://github.com/<your-username>/shop-flow-commerce.git
cd shop-flow-commerce
```

---

## 📋 Deliverables Checklist

- [x] Business Requirements Document (BRD)
- [x] AS-IS / TO-BE process documentation
- [x] Business Rules
- [x] User Stories
- [x] Wireframes (Return Tracking + Dashboard layout)
- [x] KPI definitions
- [ ] PostgreSQL analytical views (to be implemented)
- [ ] Power BI dashboards (to be implemented)
- [ ] Test cases

---

## 👥 Stakeholders

| Stakeholder | Role |
|-------------|------|
| Business Owner / Management | Decision maker |
| Customers | End users |
| Customer Support | Operational |
| Finance / Merchandising / Marketing | Business users |
| Warehouse | Operational |
| Business Analyst | Requirements & analysis |
| Development / QA | Implementation & validation |

---

## 📝 Document Control

| Field | Value |
|-------|-------|
| Prepared By | Shanwi Saurya (Business Analyst) |
| Document Type | Business Requirements Document |
| Version | 1.0 |
| Status | Draft – For Review |
| Date | 30 October 2026 |

---

## 📄 License

This project is for educational / portfolio purposes. Synthetic data is used. No real business performance claims are made.

---

**Next Steps:** Review BRD → Approve metric definitions → Implement PostgreSQL views → Build Power BI reports.
