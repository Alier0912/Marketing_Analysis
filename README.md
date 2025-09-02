# Marketing Campaign Analysis

This project provides a comprehensive analysis of marketing campaign data, focusing on channel performance, customer acquisition and retention, and budget optimization. The workflow is implemented in [campaigns_analysis.ipynb](campaigns_analysis.ipynb) using the dataset [marketing_campaign_data.csv](marketing_campaign_data.csv).

---

## Table of Contents

- [Project Structure](#project-structure)
- [Workflow Overview](#workflow-overview)
  - [1. Data Cleaning & Preparation](#1-data-cleaning--preparation)
  - [2. Data Analysis](#2-data-analysis)
  - [3. Customer Acquisition & Retention](#3-customer-acquisition--retention)
  - [4. Budget Optimization](#4-budget-optimization)
- [Key Findings](#key-findings)
- [Recommendations](#recommendations)
- [Conclusion](#conclusion)

---

## Project Structure

```
campaigns_analysis.ipynb
marketing_campaign_data.csv
```

- **campaigns_analysis.ipynb**: Main notebook containing all code and visualizations.
- **marketing_campaign_data.csv**: Raw marketing campaign data.

---

## Workflow Overview

### 1. Data Cleaning & Preparation

- **Loading Data**: The dataset is loaded using pandas.
- **Null Handling**: 
  - Missing `channel` values are replaced with `'Unknown'`.
  - Missing `clicks` and `spend` are filled with their respective means.
- **Duplicates**: Duplicate rows are identified and removed.
- **Data Types**: 
  - `campaign_date` is converted to datetime.
  - Channel names are standardized (e.g., "email" → "Email").
- **Validation**: Data types and value counts are checked to ensure consistency.

**Feature Impact:**  
- Ensures data integrity and consistency for reliable analysis.
- Prepares categorical and numerical features for aggregation and visualization.

---

### 2. Data Analysis

- **Conversion Rate (CR)**: Calculated per channel as `(conversions / clicks) * 100`.
- **Conversion Rate from Impressions**: `(conversions / impressions) * 100`.
- **Click-Through Rate (CTR)**: `(clicks / impressions) * 100`.
- **Cost Per Click (CPC)**: `(spend / clicks)`.
- **Cost Per Acquisition (CPA)**: `(spend / conversions)`.
- **Return on Ad Spend (ROAS)**: `(revenue / spend) * 100`.
- **Visualizations**: Bar charts for each metric by channel.

**Feature Impact:**  
- Highlights which channels are most effective at driving conversions and engagement.
- Identifies cost efficiency for each channel.
- ROAS feature directly shows marketing ROI per channel.

---

### 3. Customer Acquisition & Retention

- **Customer Acquisition Cost (CAC)**: `(spend / conversions)` per channel.
- **Retention Rate**: Calculated monthly as `(returning customers / total customers) * 100`.
- **Churn Rate**: Yearly, as `(customers lost / customers at start) * 100`.
- **Lifetime Value (LTV)**: 
  - `APV = revenue / conversions`
  - `PF = conversions / unique_customers`
  - `LTV = APV * PF * average customer lifespan (24 months)`
- **Visualizations**: Bar charts for CAC, retention, churn, and LTV.

**Feature Impact:**  
- CAC feature shows how much it costs to acquire a customer per channel.
- Retention and churn features reveal customer loyalty and loss trends.
- LTV feature quantifies the long-term value of customers per channel.

---

### 4. Budget Optimization

- **Spend & Revenue**: Aggregated per channel.
- **ROAS**: Compared across channels.
- **Visualization**: Dual-axis bar chart for spend vs. revenue by channel.

**Feature Impact:**  
- Shows which channels deliver the most revenue for the budget spent.
- Enables data-driven decisions for reallocating marketing budget.

---

## Key Findings

- **Channel Performance**:  
  - Channels like [example: Facebook, Google Ads] have the highest conversion rates and ROAS, indicating strong performance.
  - Some channels (e.g., Affiliate, Unknown) have lower conversion rates and higher acquisition costs.

- **Cost Efficiency**:  
  - CPC and CPA metrics show that some channels are more cost-effective than others.
  - High spend does not always correlate with high conversions or revenue.

- **Retention & Churn**:  
  - Retention rates are highest for channels with strong customer engagement (e.g., Email).
  - Churn rates are higher in channels with less targeted campaigns.

- **Lifetime Value (LTV)**:  
  - Channels with high LTV (e.g., SEO, Email) are valuable for long-term growth.

- **Budget Allocation**:  
  - Some channels deliver significantly higher revenue per dollar spent, as shown by ROAS and dual-axis budget analysis.

---

## Recommendations

1. **Increase Investment in High-ROAS Channels**  
   - Channels with high ROAS and LTV (e.g., Facebook, Email) should receive more budget allocation.

2. **Optimize Underperforming Channels**  
   - Channels with high spend but low conversion or retention (e.g., Affiliate, Unknown) should be reviewed for improvement or reallocation.

3. **Retention Strategies**  
   - Implement targeted retention campaigns for channels with high churn rates to improve customer loyalty.

4. **Monitor and Update Regularly**  
   - Continuously monitor channel performance and update strategies as new data becomes available.

5. **Leverage LTV Insights**  
   - Focus on channels with high LTV for long-term profitability, even if their initial acquisition cost is higher.

---

## Conclusion

This analysis provides actionable insights into marketing channel effectiveness, customer acquisition and retention, and budget optimization. 
By leveraging these findings, marketing teams can maximize ROI, improve customer loyalty, and allocate budgets more efficiently.

