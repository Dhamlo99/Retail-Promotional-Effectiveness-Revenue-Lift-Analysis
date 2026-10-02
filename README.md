# Retail Promotional Effectiveness & Revenue Lift Analysis

## Executive Summary
This project evaluates promotional campaign efficiency and revenue impact across 50 retail store locations and 10 cities during two peak holiday periods: **Diwali** and **Sankranti**. 

By analyzing SKU-level baseline versus promotional sales, this audit identifies which promotional structures (`BOGOF`, `500 Cashback`, `50% OFF`, `33% OFF`, `25% OFF`) generate true top-line revenue expansion versus those that dilute profit margins through uncompensated discount volume.

---

## Data Model & Schema Overview

The analysis operates on the relational schema `retail_events_db` consisting of one central fact table and three dimension tables[cite: 1, 2, 3, 4]:

```text
       dim_campaigns (campaign_id)
                  │
                  ▼
dim_stores ──< fact_events >── dim_products
(store_id)      (event_id)     (product_code)
