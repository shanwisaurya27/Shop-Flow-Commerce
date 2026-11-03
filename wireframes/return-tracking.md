# Wireframes – Customer Return Tracking

**Project:** Shop Flow Commerce  
**Tool suggestion:** Figma / FigJam / Balsamiq  
**Related Requirements:** BR-004 to BR-009

These are low-fidelity textual wireframes that describe the key screens for the return tracking experience. Use them as a starting point for detailed Figma designs.

---

## Screen 1: My Returns (List View)

```
┌────────────────────────────────────────────────────────────┐
│  Shop Flow Commerce                    [Search]  [Profile] │
├────────────────────────────────────────────────────────────┤
│  ← Back to Orders                                          │
│                                                            │
│  My Returns                                                │
│  ─────────────────────────────────────────────────────────│
│                                                            │
│  Return ID: RET-2026-00482          Status: In Transit     │
│  Order: #ORD-88921                  Requested: 28 Oct 2026 │
│  Item: Wireless Headphones (x1)                            │
│  [View Details →]                                          │
│                                                            │
│  ─────────────────────────────────────────────────────────│
│                                                            │
│  Return ID: RET-2026-00391          Status: Refunded       │
│  Order: #ORD-87410                  Requested: 12 Oct 2026 │
│  Item: Summer Dress (x1)                                   │
│  [View Details →]                                          │
│                                                            │
│  ─────────────────────────────────────────────────────────│
│                                                            │
│  Return ID: RET-2026-00215          Status: Declined       │
│  Order: #ORD-85102                  Requested: 03 Oct 2026 │
│  Item: Smart Watch Band (x1)                               │
│  [View Details →]                                          │
│                                                            │
└────────────────────────────────────────────────────────────┘
```

**Notes:**
- Show most recent returns first.
- Status badge colour coding recommended:
  - Requested → Blue
  - In Transit → Orange
  - Inspecting → Purple
  - Refunded → Green
  - Declined → Red

---

## Screen 2: Return Details + Status Timeline

```
┌────────────────────────────────────────────────────────────┐
│  Shop Flow Commerce                    [Search]  [Profile] │
├────────────────────────────────────────────────────────────┤
│  ← My Returns                                              │
│                                                            │
│  Return ID: RET-2026-00482                                 │
│  Status: ● In Transit                                      │
│                                                            │
│  Order: #ORD-88921                                         │
│  Item: Wireless Headphones – Black                         │
│  Qty: 1   |   Paid: ₹2,499                                 │
│                                                            │
│  ─────────────────────────────────────────────────────────│
│  STATUS TIMELINE                                           │
│                                                            │
│  ● Requested          28 Oct 2026, 14:32                   │
│  │  Return request created                                 │
│  │                                                         │
│  ● In Transit         29 Oct 2026, 09:15                   │
│  │  Item handed over to courier                            │
│  │  Tracking: SF-TRK-99102                                 │
│  │                                                         │
│  ○ Inspecting         Expected soon                        │
│  │                                                         │
│  ○ Refunded / Declined                                     │
│                                                            │
│  ─────────────────────────────────────────────────────────│
│  Need help?  [Contact Support]                             │
└────────────────────────────────────────────────────────────┘
```

**Notes:**
- Timeline is vertical and chronological.
- Completed steps are filled; future steps are empty circles.
- Show expected next action where possible.

---

## Screen 3: Refund Confirmation (Final State)

```
┌────────────────────────────────────────────────────────────┐
│  Shop Flow Commerce                    [Search]  [Profile] │
├────────────────────────────────────────────────────────────┤
│  ← My Returns                                              │
│                                                            │
│  Return ID: RET-2026-00391                                 │
│  Status: ● Refunded                                        │
│                                                            │
│  Order: #ORD-87410                                         │
│  Item: Summer Dress – Size M                               │
│  Qty: 1   |   Paid: ₹1,899                                 │
│                                                            │
│  ─────────────────────────────────────────────────────────│
│  REFUND DETAILS                                            │
│                                                            │
│  Refund Amount:     ₹1,899                                 │
│  Method:            Original payment method                │
│  Processed on:      18 Oct 2026                            │
│  Expected in bank:  3–5 business days                      │
│                                                            │
│  ─────────────────────────────────────────────────────────│
│  STATUS TIMELINE (all complete)                            │
│  ● Requested → ● In Transit → ● Inspecting → ● Refunded    │
└────────────────────────────────────────────────────────────┘
```

---

## Key Design Principles

1. **Clarity first** – Customer should understand status in < 3 seconds.
2. **Unique Return ID** always visible.
3. **Progressive disclosure** – List → Details → Full timeline.
4. **Consistent status language** across Customer, Support, Warehouse and Finance.
5. **Mobile-first** – These screens must work well on small devices.

---

## Suggested Figma Structure

- Frame set: Desktop + Mobile variants
- Components: Status Badge, Timeline Step, Return Card
- Prototype: Click from List → Details → (optional) Support chat
