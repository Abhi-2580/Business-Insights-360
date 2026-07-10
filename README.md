# 📊 Business Insights 360 — AtliQ Hardware

> *"AtliQ's revenue is growing fast, but the company is losing about $4,010M because its Operational Expenses are higher than its Gross Margin. This dashboard highlights the main problem areas across Finance, Sales, Marketing, and Supply Chain, helping decision-makers see where action is needed."*

---

## 🏬 Company Overview

AtliQ Hardware (a fictional company) is one of the fastest-growing companies in the consumer electronics market, specialised in hardware products such as PCs, Laptops, Accessories, Printers, Networking Equipment, Storage Devices, and more. Over the years, AtliQ has expanded globally and now operates across Asia Pacific (APAC), North America(NA), Latin America (LATAM), and the European Union (EU).

The company serves a diverse customer base through two primary sales platforms:
- **Brick-and-Mortar Stores** — Physical retail outlets such as Croma, Vijay Sales and Best Buy.
- **E-Commerce Platforms** — Online retailers such as Amazon and Flipkart.

Additionally, AtliQ operates through three sales channels:
- **Retailers** — Third-party sellers, both online and offline, that stock and sell AtliQ's products. For example, Croma and Amazon.
- **Direct Stores** — AtliQ's own physical stores, like AtliQe-store and AtliQ Exclusive, where consumers purchase directly.
- **Distributors** — In countries such as China and South Korea, where direct sales are restricted, AtliQ has partnered with large distributors like Neptune. These distributors then supply products to local retailers.

**Note:** AtliQ's customers are retailers and distributors, while the consumers are the end users.

---

## 🔎 Problem Statement

AtliQ Hardware had grown rapidly over the years and decided to expand into Latin America. However, the company faced significant losses in the region despite opening several stores. Meanwhile, competitor Dell experienced strong growth throughout the same period.

AtliQ's senior executives investigated the failure and identified two root causes:
1. Decisions were based on multiple disconnected Excel files that were ineffective at generating actionable insights.
2. Strategy relied on intuition and survey data rather than deep analytical insights.

To address these challenges, AtliQ launched a data analytics initiative and assigned a dedicated team to improve decision-making and help the company gain a strategic advantage.

---

## 🎯 Project Objective

The goal of this project is to create a simple and easy-to-use Power BI dashboard for AtliQ Hardware. It provides useful insights into Finance, Sales, Marketing, and Supply Chain, along with an Executive View that gives a quick overview of the business.

The dashboard helps stakeholders:
- Identify business opportunities
- Detect performance gaps
- Make data-driven decisions
- Improve transparency
- Enhance data accessibility
- Drive smarter business strategies for greater efficiency

---

## 🛢️ Data Overview

AtliQ's fiscal year runs **September to August**. The dataset covers actual sales from **1 September 2017 to 1 August 2025** with **3.7+ million records**.

The company provided two SQL databases and three Excel files for analysis.

**SQL Databases:**

| Database | Tables |
|----------|--------|
| gdb041 | fact_forecast_monthly, fact_sales_monthly, dim_customer, dim_market, dim_product |
| gdb056 | freight_cost, gross_price, manufacturing_cost, post_invoice_deductions, pre_invoice_deductions |

**Excel Files:**

| File | Coverage |
|------|----------|
| Operating Expenses | All fiscal years |
| Targets | Fiscal Year 2022–2025 only |
| Market Share | Personal Computer division only |

**NOTE:** Since this is a bootcamp project, the data files cannot be shared publicly.

---

## 🧹 Data Cleaning & Transformation

**Standardisation:**
- Removed leading and trailing spaces from text fields.
- Standardised naming conventions across tables for consistency.

**Data Structuring & Optimisation:**
- Created a `dim_date` table for accurate time-based analysis aligned to AtliQ's fiscal year.
- Merged `fact_sales_monthly` and `fact_forecast_monthly` into a single unified table `fact_actual_estimates` to simplify calculations and reduce model complexity.
- Added calculated fields in `fact_actual_estimates` by deriving values from related tables (e.g., pre-invoice deduction amounts derived from percentage values in the pre_invoice_deductions table).
- Disabled load for intermediate tables (fact_sales_monthly, gross_price, pre_invoice_deductions) used only for derivations — reducing Power BI report size and improving performance.

---

## 🛠️ Tools & Skills

| Tool | Purpose |
|------|---------|
| Power BI Desktop | Data modelling, DAX, Dashboard development & visualisation |
| Power Query | Data cleaning & ETL |
| MySQL | Querying and loading data into Power BI |
| DAX Studio | Performance optimisation |
| Excel | Data validation |
| Power BI Service | Report Publishing |

---

## 🗂️ Dashboard Views

| View | Key Metrics |
|------|-------------|
| 🏠 Home | Navigation hub with report overview |
| 💰 Finance | Top 3 KPIs, P&L Statement, Performance Over Time Chart, Top / Bottom Products & Customers |
| 📈 Sales | Customer & Product Performance Matrix and Chart, Unit Economics |
| 📣 Marketing | Segment & Market Profitability, GM% & NP% scatter analysis, NS & GM Bifurcation |
| 🚚 Supply Chain | Top 3 KPIs, Forecast Accuracy / Net Error Trend analysis, Risk by Customer & Product |
| 👔 Executive | Top 4 KPIs, Revenue Contribution by Division and Channel, PC Market Share trend, Top 5 Customers and Products |

---

## 📑 Report Inclusions
This repository includes a PDF version of the Power BI report and the underlying data model.
- 📄 [Dashboard](./BI360.pdf) 
- 🗂️ [Data Model](./DataModel.png)

**NOTE:** The Information Panel includes provisions for FAQs and a downloadable live Excel version for future company use. However, sharing the live Excel version requires the company's permission.  
The Support Panel provides options to resolve issues, submit feedback, request new features, and review the contingency plan. Company support is needed to integrate these features into the Power BI report.
  
---

## 💡 Key Insights

### 💰 Financial Performance
- Net Sales reached **$19.37bn** — up **61.5% vs Last Year** — strong top-line growth.
- Net Profit is **-20.71%** because Operational Expense ($11,061M) is **1.57x the Gross Margin** ($7,051M).
- GM% declined to **36.41%** — down 2.17% vs Last Year — squeezed by both deduction growth and COGS rising faster than Net Sales.

### 📈 Sales Performance
-
- Pre Invoice and Post Invoice Deductions consume **53% of Gross Sales** — and are growing faster than revenue, compressing GM%.
- Every product segment shows **negative ∆GM%** vs Last Year — revenue is growing through over-discounting.
- **Amazon** — largest customer — grew revenue 58.5% but GM% declined **-5.2%**, signaling margin is being sacrificed for volume.
- **AQ Smash 1** — top product under Notebook segment — grew revenue 64.2% but GM% declined **-1.85%**, reflecting the structural GM problem across all products.

### 📣 Marketing Performance
- **India** is AtliQ's largest market at $4,623M NS, but the most loss-making at **-42.30% Net Profit** — the biggest geographic risk.
- **South Korea** is the only major market with positive Net Profit at **+1.23%** — proving profitability is achievable.
- No product category is currently profitable — this is a **structural OpEx problem**, not a product problem.
- **Business Laptop** ($3,386M NS) and **Gaming Laptop** ($3,132M NS) are the highest revenue categories, but both are deeply loss-making.
- **USB Flash Drives** ($9M NS) is the lowest revenue category and the most loss-making at **-33.00% Net Profit** — needs immediate strategic review.

### 🚚 Supply Chain Performance
- Forecast Accuracy improved to **91.41%** (+0.57% vs Last Year) — positive direction.
- However, **Absolute Error grew 48.32%** to 37M — errors are scaling faster than the business, not shrinking.
- **AtliQ Exclusive** — highest-margin channel at 43.73% GM% — has the worst forecast accuracy at 76.82% and is consistently **Out of Stock** (-497K Net Error). Losing sales in the highest-margin channel hurts the business even more.
- **Networking** is the only product segment with OOS risk — all other segments carry Excess Inventory risk, tying up working capital.

### 🌍 Competitive Position
- AtliQ's PC Market Share grew from **~6.7% (FY2024) to ~7.7% (FY2025)** — consistent improvement.
- **Dale** remains the dominant competitor — a significant market share gap remains.
- **South East Asia (SE)** was the fastest-growing region (~19.3% share in FY2025), making AtliQ one of the top 2 players in that region.
- **Retailers** contribute ~69.7% of revenue — heavy channel concentration risk.

---

## 📝 Recommendations

1. **Break down and reduce OpEx** — At $11,061M it is the single biggest lever to profitability. No targeted cost action is possible without an OpEx category breakdown.
2. **Review India's go-to-market strategy** — $4,623M revenue generating -$1,955M Net Profit is value destruction, not growth. Reprice, reduce promotional spend, or refocus on higher-margin categories.
3. **Shift to performance-based discounting** — Replace flat post-invoice discounts with a model tied to customer GM% contribution to stop margin erosion.
4. **Prioritise AtliQ Exclusive in supply planning** — It is our highest-margin channel but consistently out of stock. Lost sales are doubly damaging.
5. **Use South Korea as a profitability benchmark** — Study its cost and channel model and replicate across other markets.
6. **Scale forecasting capability with business growth** — Forecast Accuracy % improving while Absolute Error grows by 48% means the forecasting model is not keeping pace with business scale.
7. **Reduce deduction rate** — Pre Invoice Deductions at $9,384M represent 24% of Gross Sales. Even a 2% reduction would materially improve GM%.
8. **Strategically review USB Flash Drives** — At -33% Net Profit on only $9M revenue, this category needs repositioning, cost restructuring, or discontinuation.
9. **Align inventory and promotions with September–December peak** — Sales consistently surge in this window. Supply chain and marketing must plan inventory and campaigns ahead of this period every year.


## 📎 Links

🌐 [Linkedin Post](https://www.linkedin.com/posts/abhijeetpal1_bi-360-dashboard-ugcPost-7481212444799811584-_dJh/?utm_source=share&utm_medium=member_desktop&rcm=ACoAACvkoAMBFvZ7S2o6RaOW1TOAftiS92Nraqo)  
📊 [Live Dashboard](https://app.powerbi.com/groups/me/reports/a89489a5-56f9-4eee-b555-9e5528c88257/31181b0a108c17909188?experience=power-bi&clientSideAuth=0)

---

## 🎓 Acknowledgements

- **Dhaval Patel** — Founder, Codebasics
- **Hemanand Vadivel** — Co-Founder & CEO, Codebasics
- [Codebasics Data Analytics Bootcamp 5.O](https://codebasics.io/bootcamps/data-analytics-bootcamp-with-practical-job-assistance) — Project guidance and dataset

---

## 🙋 About Me

I am an aspiring Data Analyst with hands-on experience in Advanced Excel, Power BI, and SQL — passionate about turning raw data into business insights that drive real decisions.

This project reflects not just technical skills but business thinking — understanding what a CFO, Sales Director, Marketing Head, and Supply Chain Head actually need from data.

📧 [Email](mailto:abhijeetpal2580@gmail.com) <br>
💼 [LinkedIn](https://www.linkedin.com/in/abhijeetpal1/)<br>
🐙 [GitHub](https://github.com/Abhi-2580)

---

*Built as part of the Codebasics Data Analytics Bootcamp*

