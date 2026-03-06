# E-Commerce Sales Funnel & Conversion Analysis

## Overview
This project analyzes a 5,000-user e-commerce sales funnel using BigQuery SQL, tracking 5 event stages from page view to purchase across a $88K revenue dataset. The goal was to identify where users were dropping off and which traffic sources were driving the most conversions.

## Dataset
- **Users:** 5,000
- **Revenue:** $88K
- **Event Stages:** Page View → Add to Cart → Checkout Start → Payment Info → Purchase
- **Traffic Sources:** Organic, Paid Ads, Email, Social Media

## Key Findings
- Overall conversion rate was **17%**
- Biggest drop-off was at **view to cart (31%)** — the primary leakage point
- **Email** had the highest purchase conversion rate at **34%**
- **Social media** had the lowest at **7%** — a 5x gap
- Average customer journey time was **24.63 minutes**
- Average Order Value (AOV) was **$106.51**

## Recommendations
- Shift social ad spend away from traffic campaigns toward email capture and retargeting
- Set a CAC ceiling of $42 based on the $106 AOV to protect margin
- Do not redesign the checkout flow — conversion rates post-cart are strong (82–92%)

## Queries
| File | Description |
|------|-------------|
| 01_funnel_conversion_rate.sql | Overall funnel conversion rates across all 5 stages |
| 02_funnel_by_source.sql | Conversion rates broken down by traffic source |
| 03_time_to_conversion.sql | Average time taken from view to purchase |
| 04_revenue_funnel.sql | Revenue metrics including AOV and revenue per visitor |

## Tools Used
- **BigQuery** — SQL querying and analysis
- **Google Cloud Platform** — data storage and compute
