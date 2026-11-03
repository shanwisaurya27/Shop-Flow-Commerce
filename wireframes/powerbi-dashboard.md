# Wireframes – Power BI Dashboard Layout

**Project:** Shop Flow Commerce  
**Related Requirements:** BR-016, BR-017 + all KPI requirements

These are conceptual layouts for the four planned Power BI report pages. Use them as a guide when building the actual .pbix file.

---

## Page 1: Executive Overview

```
┌────────────────────────────────────────────────────────────────────┐
│  SHOP FLOW COMMERCE – Executive Overview          [Date Slicer]   │
├────────────────┬────────────────┬────────────────┬────────────────┤
│  Revenue       │  Total Orders  │  AOV           │  Refunded Cash │
│  ₹ XX,XX,XXX   │  X,XXX         │  ₹ X,XXX       │  ₹ X,XX,XXX    │
│  ▲ 4.2% vs LY  │  ▲ 2.1%        │  ▼ 1.3%        │  ▲ 8.5%        │
├────────────────┴────────────────┴────────────────┴────────────────┤
│                                                                    │
│  Revenue Trend (Monthly)              Orders vs Refunds (Monthly)  │
│  [Line Chart]                         [Clustered Column Chart]     │
│                                                                    │
├────────────────────────────────────────────────────────────────────┤
│  Top Categories by Net Revenue (after refunds)                     │
│  [Horizontal Bar Chart]                                            │
│                                                                    │
├────────────────────────────────────────────────────────────────────┤
│  Key Alerts / Insights                                             │
│  • Cart abandonment currently at XX%                               │
│  • Average refund processing time: X.X days                        │
│  • Highest return rate category: XXX                               │
└────────────────────────────────────────────────────────────────────┘
```

**Key Measures (must use approved definitions):**
- Revenue (excl. cancelled)
- Total Orders
- AOV
- Refunded Cash (only finalised refunds)

---

## Page 2: Merchandising

```
┌────────────────────────────────────────────────────────────────────┐
│  SHOP FLOW COMMERCE – Merchandising               [Date | Category]│
├──────────────────────────────┬─────────────────────────────────────┤
│  Gross Sales by Category     │  Net Contribution after Refunds     │
│  [Column Chart]              │  [Column + Line or Waterfall]       │
├──────────────────────────────┴─────────────────────────────────────┤
│  Category Performance Table                                        │
│  Category | Gross Sales | Refunded | Net Sales | Return Rate | AOV │
│  Fashion  | ...         | ...      | ...       | ...         | ... │
│  Electronics | ...      | ...      | ...       | ...         | ... │
│  ...                                                               │
├────────────────────────────────────────────────────────────────────┤
│  Return Reasons / Patterns (if data available)                     │
│  [Pie or Treemap]                                                  │
└────────────────────────────────────────────────────────────────────┘
```

---

## Page 3: Customers

```
┌────────────────────────────────────────────────────────────────────┐
│  SHOP FLOW COMMERCE – Customers                   [Cohort Period]  │
├────────────────────────────────────────────────────────────────────┤
│  Customer Cohort Retention                                         │
│  [Matrix / Heatmap – Month 0 = 100%]                               │
│                                                                    │
├──────────────────────────────┬─────────────────────────────────────┤
│  RFM Segment Distribution    │  Segment Value (Monetary)           │
│  [Donut / Pie]               │  [Bar Chart]                        │
├──────────────────────────────┴─────────────────────────────────────┤
│  RFM Details Table (filterable)                                    │
│  Customer ID | Recency | Frequency | Monetary | Segment            │
└────────────────────────────────────────────────────────────────────┘
```

**Notes:**
- Cohort month based on first valid order date (BRULE-005)
- Month 0 clearly labelled as 100% baseline (BRULE-006)

---

## Page 4: Funnel & Refund Operations

```
┌────────────────────────────────────────────────────────────────────┐
│  SHOP FLOW COMMERCE – Funnel & Operations         [Device | Date]  │
├────────────────────────────────────────────────────────────────────┤
│  Browse-to-Buy Conversion Funnel                                   │
│  Sessions → Product Views → Add to Cart → Checkout → Purchase      │
│  [Funnel Chart with drop-off %]                                    │
│                                                                    │
│  Mobile vs Desktop conversion comparison side-by-side              │
├──────────────────────────────┬─────────────────────────────────────┤
│  Pending Refunds             │  Refund Processing Time             │
│  Count + Value               │  Average + Distribution             │
│  [KPI + Table]               │  [Histogram / Box plot]             │
├──────────────────────────────┴─────────────────────────────────────┤
│  Returns by Status (Requested / In Transit / Inspecting / etc.)    │
│  [Stacked Bar or Status cards]                                     │
└────────────────────────────────────────────────────────────────────┘
```

---

## Design Guidelines for Power BI

1. Use a consistent colour palette and status colours across all pages.
2. All monetary measures must follow the approved business rules.
3. Tooltips should show the definition of the measure (for transparency).
4. Include a “Last refreshed” timestamp and data source note.
5. Provide clear filters / slicers for Date, Category, Device, and Status.
