# Miami Shops — Performance vs. Weather & Demographics (Capstone)

A Power BI capstone project that explores how **weather conditions** and **customer demographic mix** drive daily shop performance across multiple Miami retail locations.

## Overview

Most sales dashboards stop at "here are the numbers". This one goes further by asking: **what external factors actually move the numbers?**

It joins daily shop transaction data with weather observations and customer demographic snapshots into a single fact table, then visualises sales per customer alongside temperature, rainfall, weekend flags, and the family/gender/marital mix of the customers walking in. The goal: surface the external drivers stakeholders should pay attention to when planning staffing, inventory, or promotions.

## Tools

- **Microsoft Power BI Desktop**
- **DAX**
- **Data modelling** — pre-joined fact table (`table_joined`) combining sales, weather, and demographics

## Dataset

A custom joined dataset (`table_joined`) containing daily-level records with:

**Sales metrics**
- `sales_usd` — daily sales in USD
- `customers` — daily customer count
- `sales_per_customer` — average basket size

**External / contextual fields**
- `date` — calendar date
- `shop_name` — store identifier
- `avg_temp_f` — daily average temperature (Fahrenheit)
- `is_rain` — rain flag
- `is_weekend` — weekend flag

**Customer demographic mix**
- `pct_family`, `pct_single` — household type breakdown
- `pct_male`, `pct_female` — gender breakdown

## What the report contains

### Page 1

- **KPI cards** for sales, customers, and average sales per customer
- **Clustered column / line** charts breaking down sales by month and shop
- **Donut chart** showing the demographic mix of customers contributing to revenue
- **Slicers** for shop, weekend, rain

### Page 2

- **Pivot table** with daily-level detail
- Cross-tab views slicing performance by **weather conditions** and **demographic segments**
- Text boxes and shapes used for layout polish and annotations

## Key technical work

- **Data integration** — built a single denormalised fact table joining three logical sources (sales, weather, demographics) into one row-per-day-per-shop grain. This is a common challenge in real-world reporting and the modelling choice (denormalise vs. star) is something interviewers like to discuss.
- **Behavioural framing** — went beyond reporting "what happened" to surfacing **why it might have happened** (weather, weekend, customer mix). This is the difference between a junior dashboard and an analyst's dashboard.
- **Two-page design** — Page 1 for high-level KPIs, Page 2 for granular interrogation.

## Screenshots

![image alt](https://github.com/bigruntown/Miami-Shops/blob/main/Screenshot.jpg?raw=true)
![image alt](https://github.com/bigruntown/Miami-Shops/blob/main/detail%20page%20screenshot.jpg?raw=true)


## How to view this project

1. Download `Miami-shops-CAPSTONE-PROJECT.pbix` from this repo.
2. Open it in **Power BI Desktop** (free download from Microsoft).
3. Use the slicers on Page 1 to filter by shop, rain, or weekend.

---

*Built as the capstone project for the Utiva Data Science program (2026).*
