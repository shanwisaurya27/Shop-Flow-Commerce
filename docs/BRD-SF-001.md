# BUSINESS REQUIREMENTS DOCUMENT (BRD)

**Project: Shop Flow Commerce**

| Field | Details |
|-------|---------|
| **Project Name** | Shop Flow Commerce |
| **Document Type** | Business Requirement Document |
| **Document ID** | BRD-SF-001 |
| **Version** | 1.0 |
| **Prepared By** | Shanwi Saurya |
| **Role** | Business Analyst |
| **Project Type** | E-Commerce Business Analysis |
| **Status** | Draft |
| **Date** | 30 October 2026 |

---

## 1. Executive Summary

Shop Flow Commerce is a mid-sized e-commerce company that sells products in four categories: **Fashion**, **Electronics**, **Home** and **Beauty**.

This organization is confronted with three challenges:

1. Shoppers check out the products but leave the site without purchasing anything.
2. Clients cannot monitor the status of their returns and refunds.
3. Diverse departments have different methods of computing the revenue, refunds, and other business metrics.

---

## 2. Background Information on the Business

Shop Flow runs a platform through which customers can browse, purchase, and ask for refunds for their purchases.

The business has information on its customers, sessions, orders, order items, returns, and refunds.

But the business lacks enough visibility about the customers' buying behavior, refund processes, and commercial performance.

---

## 3. Problem Statement for the Business

Shop Flow faces issues in three key aspects of its business operations.

### 3.1 Customer Conversion Issues
- The customers are visiting the website but do not necessarily add items to their cart.
- The customers abandon their transactions before completing their purchase.
- The business is unable to pinpoint where the customers are leaving.

### 3.2 Issues With Visibility of Return and Refunds
- The customers are contacting customer service for details on their returns.
- The customers cannot easily monitor whether the items have arrived at the warehouse.
- The details of the refund processing are not clear.
- The status related enquiries are being handled by the support staff unnecessarily.

### 3.3 Inconsistency in Business Reporting
- The finance, marketing, and merchandising departments calculate their metrics differently.
- The income and refunds calculation process is inconsistent.
- The management is unable to get a unified view of the business operations.

---

## 4. Business Objectives

| Business Objective ID | Business Objective |
|-----------------------|--------------------|
| BO-001 | Determine customer drop-off points in the browse-to-buy conversion funnel. |
| BO-002 | Improve return and refund status visibility. |
| BO-003 | Establish common business definitions for revenue, orders and refunds. |
| BO-004 | Reconcile business reports with source data. |
| BO-005 | Analyze category performance adjusted for refunds. |
| BO-006 | Analyze customer retention and buying behavior. |
| BO-007 | Generate reliable business reports to facilitate managerial decision-making. |

---

## 5. Project Scope

### 5.1 In Scope
1. Customer browse-to-buy funnel analysis.
2. Customer conversion and drop-off analysis.
3. Return and refund status visibility.
4. Monitoring the refund processing cycle-time.
5. Revenue and order reconciliation.
6. Common commercial metrics definitions.
7. Category performance adjusted for refunds.
8. Customer cohort analysis.
9. Basic RFM customer segmentation.
10. Business reporting using Power BI.

### 5.2 Out of Scope
1. Creation of the mobile app.
2. Re-creation of the customer loyalty program.
3. Creation of the tax calculation engine.
4. Advertising spend ROI measurement.

---

## 6. Stakeholder Analysis

| Stakeholder | Role | Responsibility |
|-------------|------|----------------|
| Business Owner / Management | Decision Maker | Reviews business performance and determine business priorities. |
| Customers | End Users | Browse products, purchase items and track returns. |
| Customer Support Team | Operational User | Handles customer enquiries and return-related queries. |
| Finance Team | Business User | Reviews revenue, refunds and financial performance. |
| Warehouse Team | Operational User | Receives and inspects returned products. |
| Merchandising Team | Business User | Monitors product and category performance. |
| Marketing Team | Business User | Reviews customer acquisition and conversion performance. |
| Business Analyst | Analyst | Investigates problems, documents requirements and defines business rules. |
| Development Team | Technical Team | Implements approved system requirements. |
| QA / Testing Team | Testing Team | Validates requirements and expected system behaviour. |

---

## 7. Business Requirements

| Requirement ID | Business Requirement | Priority |
|----------------|----------------------|----------|
| BR-001 | Identify customer drop-off points across the browse-to-buy conversion funnel. | High |
| BR-002 | Analyze customer conversion rates at different funnel stages. | High |
| BR-003 | Compare customer conversion behaviour across mobile and desktop devices. | Medium |
| BR-004 | Provide customers with visibility into their return status. | High |
| BR-005 | Generate a unique return ID for every return request. | High |
| BR-006 | Establish common return statuses for customers, warehouse and support teams. | High |
| BR-007 | Allow customers to track return progress from request creation to final decision. | High |
| BR-008 | Improve visibility into pending and completed refunds. | High |
| BR-009 | Monitor refund processing cycle time and identify delayed returns. | High |
| BR-010 | Establish consistent definitions for revenue, orders, average order value and refunded cash. | High |
| BR-011 | Reconcile reported revenue and order figures against source data. | High |
| BR-012 | Analyze category sales and contribution after refunds. | High |
| BR-013 | Identify product and category return patterns and reasons. | Medium |
| BR-014 | Analyze customer retention through cohort analysis. | Medium |
| BR-015 | Segment customers using Recency, Frequency and Monetary (RFM) analysis. | Medium |
| BR-016 | Provide management with a consolidated business performance report. | High |
| BR-017 | Ensure the same approved business definitions are used across reports. | High |

**Priority Definitions:**
- **High**: Essential for solving a major business problem.
- **Medium**: Important for improving business understanding and decision-making.
- **Low**: Useful but not immediately necessary.

---

## 8. Business Rules

| Rule ID | Business Rule |
|---------|---------------|
| BRULE-001 | Cancelled orders must not be counted as revenue. |
| BRULE-002 | A return awaiting warehouse inspection must not be treated as a completed cash refund. |
| BRULE-003 | A refund cannot exceed the amount paid for the returned units. |
| BRULE-004 | Guest sessions must be included in conversion funnel analysis. |
| BRULE-005 | Customer cohort month must be calculated using the first valid order date, not the signup date. |
| BRULE-006 | Month zero in customer cohort analysis is 100% by definition and must not be interpreted as a retention achievement. |
| BRULE-007 | Revenue and refund calculations must follow the same approved definitions across all reports. |
| BRULE-008 | Refund processing must follow warehouse acceptance and the applicable business rules. |

---

## 9. AS-IS Business Process

### 9.1 Customer Purchase Process
1. Customer visits website.
2. Customer looks through available products.
3. Customer can add some products into the cart.
4. Customer can exit without purchase.
5. Some customers make purchases.

**Existing Problem:** The company can't specify the reasons and stages where customer drops off.

### 9.2 Returns and Refunds Process
1. Customer communicates with customer service about return.
2. Information related to returns is processed by separate teams.
3. The warehouse and finance have no common return id.
4. Customer can not track the return status.
5. Customer service deals with repeated inquiries regarding the status.

**Existing Problem:** Returns and refunds information is not visible enough.

### 9.3 Business Reporting Process
1. Business reports are made by various departments.
2. Various teams use different calculation approaches.
3. The figures of revenues and refunds may not coincide.
4. There is a difficulty for management to have a consistent picture of business performance.

**Existing Problem:** There is no approved common definition for important commercial metrics.

---

## 10. TO-BE Business Process

### 10.1 Customer Purchase Analysis
1. Collect customer web sessions.
2. Track product browsing and cart events.
3. Analyze customers' journey through the purchase funnel.
4. Determine key points of drop-off.
5. Compare conversion behavior based on devices.
6. Report findings to management to improve business performance.

### 10.2 Return and Refund Process
1. Customer starts an eligible order.
2. Customer requests a return.
3. Special return ID number is generated.
4. Status of return is updated throughout the process.
5. Warehouse accepts and verifies the returned product.
6. The refund process is performed after the warehouse accepts the product, according to business rules.
7. Customer views updated status of return and refund.

**Approved Return Statuses:**

| Status | Description |
|--------|-------------|
| Requested | Return request is initiated. |
| In Transit | Returned item is on its way to the warehouse. |
| Inspecting | Warehouse is inspecting the returned item. |
| Refunded | Returned and refunded process was completed. |
| Declined | Return request was declined. |

### 10.3 Business Reporting Process
1. Gather business data from source files.
2. Store and analyze the data in PostgreSQL.
3. Use approved business definitions.
4. Conform calculated values with source data.
5. Prepare Power BI reports.

---

## 11. Key Performance Indicators (KPIs)

| KPI | Purpose |
|-----|---------|
| Browse-to-Buy Conversion Rate | Measures the percentage of sessions resulting in purchases. |
| Add-to-Cart Rate | Measures how many sessions result in cart activity. |
| Cart Abandonment Rate | Measures the proportion of carts that do not result in purchases. |
| Revenue | Measures eligible order revenue under the approved definition. |
| Total Orders | Measures the number of valid orders. |
| Average Order Value (AOV) | Measures average revenue per valid order. |
| Refunded Cash | Measures the amount of completed refunds. |
| Return Rate | Measures the proportion of purchased units or orders returned, according to the approved calculation. |
| Refund Processing Time | Measures the time taken to complete refunds. |
| Customer Retention Rate | Measures how many customers return to purchase again. |
| Category Contribution After Refunds | Measures category performance after accounting for refunds. |

---

## 12. Expected Business Outcomes

1. Better understanding of the customers' purchase behavior.
2. Detection of significant conversion funnel drop-offs.
3. Better insights into return and refund operations.
4. Dependence reduction of customer support on basic status checks.
5. Consistency in revenue and refunds calculation.
6. Better understanding of the categories' performance.
7. Better customer retention analysis.
8. Reliability of management reports.
9. Data-driven decision making.

---

## 13. Assumptions

1. The provided datasets will contain the necessary information for the analysis.
2. The dataset contains synthetic business information for educational purposes.
3. The customers, orders, sessions, returns, and refunds can be uniquely identified.
4. The business will approve the common metrics before the reporting.
5. The Warehouse and Finance teams will use the agreed upon process for returns and refunds.
6. The available data is sufficient for the planned analysis, subject to verification.

---

## 14. Constraints and Dependencies

### Constraints
1. The project uses synthetic datasets.
2. The analysis is restricted to the information in the provided data.
3. No business performance can be claimed on the basis of synthetic records.
4. The quality of the reports is contingent on the quality of the source data.

### Dependencies
1. Availability of customer and session datasets.
2. Availability of order, order-item, return and refund datasets.
3. Agreement on commercial metric definitions.
4. Access to PostgreSQL and Power BI.
5. Availability of approved business rules.

---

## 15. Risks

| Risk ID | Risk Description | Impact | Mitigation |
|---------|------------------|--------|------------|
| R-001 | Incomplete or incorrect source data. | High | Validate data before analysis. |
| R-002 | Different departments use different metric definitions. | High | Establish common approved definitions. |
| R-003 | Incorrect refund calculations. | High | Validate refund amounts against paid amounts. |
| R-004 | Duplicate records affect business calculations. | High | Apply appropriate data validation and reconciliation. |
| R-005 | Return status is not updated on time. | Medium | Define clear status ownership and update responsibilities. |
| R-006 | Incorrect interpretation of customer funnel data. | Medium | Validate session counts and funnel calculations. |

---

## 16. Proposed Solution and Deliverables

| Deliverable | Description | Tool |
|-------------|-------------|------|
| Business Requirements Document | Documents business needs and objectives. | MS Word |
| AS-IS / TO-BE Process Flow | Represents existing and proposed processes. | Draw.io |
| Business Rules Document | Defines approved business calculations and conditions. | MS Word |
| User Stories | Converts business requirements into development-ready stories. | Jira |
| Wireframes | Illustrates proposed return-tracking screens. | Figma |
| Database Analysis | Stores and processes business data. | PostgreSQL |
| Analytical Views | Provides consistent business calculations. | PostgreSQL |
| Business Dashboard | Displays commercial and operational performance. | Power BI |
| Test Cases | Validates business rules and requirements. | Jira / Excel |

### Proposed Power BI Report Pages
1. **Executive Overview** – Revenue, orders, AOV and refunded cash.
2. **Merchandising** – Category sales, returns and contribution after refunds.
3. **Customers** – Cohort retention and RFM analysis.
4. **Funnel and Refund Operations** – Conversion funnel, pending refunds and processing time.

---

## 17. Requirement Traceability

| Business Requirement | Related User Story | Validation |
|----------------------|--------------------|------------|
| BR-001 to BR-003 | US-FUN-001 | Funnel calculation test |
| BR-004 to BR-009 | US-REF-001 | Return and refund status test |
| BR-010 to BR-011 | US-MET-001 | Revenue reconciliation test |
| BR-012 to BR-013 | US-MER-001 | Category contribution test |
| BR-014 to BR-015 | US-CUS-001 | Cohort and RFM validation |
| BR-016 to BR-017 | US-REP-001 | Dashboard and metric consistency test |

---

## 18. Acceptance Criteria

The objectives for BRD will be seen to have been achieved when:

1. Customer funnels are able to be reviewed through the use of session data.
2. Customer drop-off points are able to be highlighted.
3. Each request for return has an ID number.
4. The five return statuses that are approved are able to be captured.
5. Pending and completed refunds are able to be differentiated.
6. The amounts refunded are verified against the payments made for the returned products.
7. Refunds are not included in revenue calculations.
8. The revenue and orders align with the source information.
9. The performance of categories after refund is able to be evaluated.
10. Customer cohorts and RFM analyses are able to be repeated.
11. The Power BI reports make use of approved business logic.

---

## 19. Conclusion

The ShopFlow Commerce project is about enhancing the analysis of customer conversion, return and refund, and consistency in business reports.

The suggested approach incorporates business analysis, data analysis and business intelligence in order for management to be able to get an idea of the issues that arise in their operation.

In the course of this project we will see how Business Analyst sees problems in the business and solves them.

---

## 20. Document Approval

| Prepared By | Reviewed By | Approved By |
|-------------|-------------|-------------|
| **Shanwi Saurya** | Project Reviewer | Business Owner |
| Business Analyst | _______________ | _______________ |
| Date: __________ | Date: __________ | Date: __________ |

**Document Status: Draft – For Review**
