# Customer Funnel Analysis Dashboard | Power BI

## Project Overview

This project focuses on analyzing customer behavior across a marketing and sales funnel using Power BI. The objective is to identify user drop-off points, measure conversion rates, analyze revenue performance, and uncover insights across channels, devices, regions, and product categories.

The dashboard enables stakeholders to monitor funnel performance, optimize customer acquisition strategies, and improve overall conversion rates through data-driven decision-making.

---

## Business Problem

Organizations invest heavily in acquiring users through various marketing channels. However, not all users complete the purchase journey.

This project aims to answer:

- Where are users dropping off in the funnel?
- What is the overall conversion rate?
- Which marketing channels drive the highest revenue?
- Which devices perform best?
- Which regions contribute the most revenue?
- How does user activity change over time?

---

## Dataset Information

The dataset contains user interaction and transaction data with the following fields:

| Column Name | Description |
|------------|-------------|
| User_ID | Unique identifier for each user |
| Session_ID | Unique session identifier |
| Event | User activity within the funnel |
| Timestamp | Date and time of interaction |
| Device | Device used by the customer |
| Region | User location/region |
| Channel | Marketing acquisition channel |
| Product_Category | Product category |
| Revenue | Revenue generated |
| Bounce_Flag | Indicates bounced sessions |

---

## Project Objectives

- Analyze customer journey across funnel stages.
- Measure user conversion rates.
- Identify funnel drop-offs.
- Evaluate channel performance.
- Analyze revenue trends.
- Monitor bounce rates.
- Compare device and regional performance.

---

## Key Performance Indicators (KPIs)

- Total Users
- Total Sessions
- Total Revenue
- Total Purchases
- Conversion Rate
- Bounce Rate

---

## Dashboard Pages

### 1. Executive Summary

Provides a high-level overview of:

- Total Users
- Total Sessions
- Revenue
- Purchases
- Conversion Rate
- Bounce Rate

---

### 2. Funnel Analysis

Visualizes customer movement through stages:

- Visit
- Product View
- Add To Cart
- Checkout
- Purchase

Helps identify major drop-off points.

---

### 3. Channel Performance Analysis

Analyzes:

- Revenue by Channel
- Conversion by Channel
- User Acquisition by Channel

---

### 4. Device & Regional Analysis

Compares:

- Device Performance
- Regional Performance
- Revenue Contribution
- Conversion Rates

---

### 5. Revenue Insights

Tracks:

- Revenue Trends
- Product Category Revenue
- Revenue by Channel

---

## Power BI Visualizations Used

### Funnel Chart
Customer Journey Funnel Analysis

### Gauge Chart
Overall Conversion Rate vs Target

### Area Chart
Revenue Trend by Marketing Channel

### Clustered Bar Chart
Revenue Contribution by Acquisition Channel

### Matrix Visual
Region × Channel Performance Matrix

### KPI Cards
Executive Summary Metrics

---

## DAX Measures

### Total Users

```DAX
Total Users =
DISTINCTCOUNT(Funnel[User_ID])
```

### Total Sessions

```DAX
Total Sessions =
DISTINCTCOUNT(Funnel[Session_ID])
```

### Total Revenue

```DAX
Total Revenue =
SUM(Funnel[Revenue])
```

### Purchases

```DAX
Purchases =
CALCULATE(
    DISTINCTCOUNT(Funnel[User_ID]),
    Funnel[Event]="Purchase"
)
```

### Conversion Rate

```DAX
Conversion Rate =
DIVIDE([Purchases],[Total Users],0)
```

### Bounce Rate

```DAX
Bounce Rate =
DIVIDE(
    SUM(Funnel[Bounce_Flag]),
    [Total Sessions],
    0
)
```

---

## Key Insights Generated

- Identified customer drop-off stages in the funnel.
- Measured end-to-end conversion rate.
- Analyzed revenue contribution across channels.
- Evaluated device-specific performance.
- Measured regional revenue distribution.
- Monitored customer engagement trends.
- Assessed bounce behavior and session quality.

---

## Tools & Technologies

- Power BI
- Power Query
- DAX
- Data Modeling
- Data Visualization
- Funnel Analysis
- Business Intelligence

---

## Project Outcomes

This dashboard provides actionable insights into customer behavior, helping businesses:

- Improve conversion rates
- Reduce funnel drop-offs
- Increase revenue
- Optimize marketing spend
- Enhance user experience

---

## Author

Vishal Awasthi

Aspiring Data Analyst | Power BI | SQL | Python | Data Visualization
