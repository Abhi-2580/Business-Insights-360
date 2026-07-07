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

AtliQ Hardware had grown rapidly over the years. Due to this, the company decided to expand its operations in Latin America. But in this region, the company faced huge losses despite opening several stores. Meanwhile, one of its competitors, Dell, experienced significant growth throughout the year.
AtliQ set up a team of executives to investigate the reason behind their failure in the region and their main finding was that their decisions were based on two things -
1. Multiple Excel files that were not effective in generating insights
2. Intuition and survey data rather than deep analytical insights.
Meanwhile, competitor Dell has a strong data analytics team to tackle those issues.

To address these challenges, AtliQ's senior executives launched a data analytics initiative and assigned us the responsibility of improving decision-making and helping the company gain a strategic advantage.

---

## 🎯 Project Objective

The objective of this project is to develop a user-friendly and intuitive Power BI dashboard for AtliQ Hardware.
The dashboard delivers actionable insights for Finance, Sales, Marketing, and Supply Chain business functions. In addition, it provides a high-level Executive View. The dashboard empowers stakeholders to:
Identify business opportunities
Detect performance gaps
Make data-driven decisions
Improve transparency
Enhance data accessibility
Drive smarter business strategies for greater efficiency

---

## 🛢️ Data Overview

AtliQ's fiscal year runs **September to August**.  The dataset covers actual sales from **1 September 2017 to 1 August 2025D** with **3.7+ million records**.

The company had provided two SQL databases: GDB041, GDB056 and three Excel files: Operating Expenses, Targets, and Market Share for analysis.

**SQL Databases:**

| Database | Tables |
|----------|--------|
| gdb041 | fact_forecast_monthly, fact_sales_monthly, dim_customer, dim_market, dim_product |
| gdb056 | freight_cost, gross_price, manufacturing_cost, post_invoice_deductions, pre_invoice_deductions |

**Excel Files:**
- Operating Expenses
- Targets *(the data is available only for Fiscal Year 2022 - 2025)*
- Market Share *(the data is available only for the Personal Computer division)*

**NOTE:** Since this is a bootcamp project, the data files cannot be shared publicly.

---

## 🧹 Data Cleaning & Transformation

**Standardisation:**
- Removed leading and trailing spaces from text fields.
- Standardised naming conventions across tables for consistency.

**Data Structuring & Optimization:**
- Created a `dim_date` table for accurate time-based analysis aligned to AtliQ's fiscal year.
- Merged `fact_sales_monthly` and `fact_forecast_monthly` into a single table `fact_actual_estimates` to simplify calculations and reduce model complexity.
- Added calculated fields in `fact_actual_estimates` by deriving values from related tables (e.g., pre-invoice deduction amounts from percentage values in the pre_invoice_deductions table).
- Disabled load for intermediate tables (fact_sales_monthly, gross_price, pre_invoice_deductions) used only for derivations — reducing Power BI report size and improving performance.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Power BI Desktop | Dashboard development & visualization |
| Power Query | Data cleaning, transformation & ETL |
| DAX | Calculated measures, KPIs & business logic |
| MySQL | Data source & extraction |
| Microsoft Excel | Operating expenses, targets & market share data |

---

## 🗂️ Dashboard Views

| View | Key Metrics |
|------|-------------|
| 🏠 Home | Navigation hub with report overview |
| 💰 Finance | P&L Statement, GM% trend, Net Sales vs Benchmark |
| 📈 Sales | Customer & Product Performance Matrix, Unit Economics |
| 📣 Marketing | Segment & Market Profitability, GM% scatter analysis |
| 🚚 Supply Chain | Forecast Accuracy, Net Error, Risk by Customer & Product |
| 👔 Executive | Top-level KPIs, PC Market Share, Yearly trends |

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
- Pre Invoice and Post Invoice Deductions consume **53% of Gross Sales** — and are growing faster than revenue, compressing GM%.
- Every product segment shows **negative ∆GM%** vs Last Year — revenue is growing through over-discounting.
- **Amazon** — largest customer — grew revenue 58.5% but GM% declined **-5.2%**, signaling margin sacrifice for volume.
- **APAC** shows the healthiest GM% positioning across all regions, suggesting pricing discipline is achievable.
- **AtliQ Exclusive** (own channel) delivers the highest GM% at 43.73% — the most profitable channel in the portfolio.
- - Certain products, like AQ 5000 Series Electron 9 5900X, AQ MB Elite, and AQ Wi Power Dx1, had zero sales in FY 2022, likely due to demand shifts or outdated models.


### 📣 Marketing Performance
- **India** is AtliQ's largest market at $4,623M NS but the most loss-making at **-42.30% Net Profit** — the biggest geographic risk.
- **South Korea** is the only major market with positive Net Profit at **+1.23%** — proving profitability is achievable.
- No product category is currently profitable — this is a **structural OpEx problem**, not a product problem.
- **Business Laptop** ($3,386M NS) and **Gaming Laptop** ($3,132M NS) are the highest revenue categories but both deeply loss-making.
- - APAC remained the largest market (FY 2019–FY 2022), led by India, while Latin America was the smallest.
- Amazon was the top global customer in all years, while Nova (operating in Austria) was the smallest since FY 2020.
- Notebook segment had the highest Revenue growth in all fiscal years but recorded the most negative Net Profit % in FY 2022, likely due to increased marketing spend.
- Desktop had the lowest growth in FY 2019 & FY 2020, while Networking became the weakest segment in FY 2022.
- USB flash drives underperformed in FY 2021 & FY 2022, signaling product or market challenges.

### 🚚 Supply Chain Performance
- Forecast Accuracy improved to **91.41%** (+0.57% vs Last Year) — positive direction.
- However, **Absolute Error grew 48.32%** to 37M — errors are scaling faster than the business, not shrinking.
- **AtliQ Exclusive** — highest margin channel — has the worst forecast accuracy at 76.82% and is consistently **Out of Stock** (-497K Net Error).
- **Networking** is the only product segment with OOS risk — all other segments carry Excess Inventory risk.
- - Forecast Accuracy (FCA%) dropped from ~86% (FY 2019) to ~73% (FY 2020) due to COVID-19 disruptions but improved to ~80% (FY 2021) and ~81% (FY 2022).
- Excess inventory was a major issue in FY 2019–FY 2020, while stock shortages became a challenge in FY 2021–FY 2022.
- Work-from-home demand surged in FY 2020, leading to stockouts for processors, keyboards, and WiFi extenders.

### 🌍 Competitive Position
- AtliQ's PC Market Share grew from ~1% (FY2021) to ~6% (FY2022) — consistent growth.
- **Dale** remains the dominant competitor — significant market share gap remains.
- **Retailers** contribute ~72% of revenue — heavy channel concentration risk.
- - Atliq’s PC market share grew from ~1% (FY 2021) to ~6% (FY 2022), though Dale remains the dominant player.
- India was the fastest-growing market (~13% share in FY 2022).
- Among subzones, North America had the highest revenue in FY 2022, but Atliq’s market penetration remained only ~5%.
- - Sales peaked from September to December across all years, likely due to festive and year-end promotions.
- Retailers contributed ~72% of revenue in FY 2022.
- The UK had the highest marketing costs, making it a key area for strategy review, followed by Germany (low revenue, high marketing spend).

---

## 📝 Recommendations

1. **Break down and reduce OpEx** — At $11,061M it is the single biggest lever to profitability. No targeted cost action is possible without an OpEx category breakdown.
2. **Review India's go-to-market strategy** — $4,623M revenue generating -$1,955M Net Profit is value destruction, not growth. Reprice, reduce promotional spend, or refocus on higher-margin categories.
3. **Shift to performance-based discounting** — Replace flat post-invoice discounts with a model tied to customer GM% contribution to stop margin erosion.
4. **Prioritise AtliQ Exclusive in supply planning** — It is our highest-margin channel but consistently out of stock. Lost sales there are doubly damaging.
5. **Use South Korea as a profitability benchmark** — Study its cost and channel model and replicate across other markets.
6. **Scale forecasting capability with business growth** — Forecast Accuracy % improving while Absolute Error grows 48% means the forecasting model is not keeping pace with business scale.
7. **Reduce deduction rate** — Pre Invoice Deductions at $9,384M represent 24% of Gross Sales. Even a 2% reduction would materially improve GM%.
8. **Align inventory and promotions with September–December sales surge** — Sales consistently peak in Q4; supply chain and marketing should plan ahead for this window.
9. - Gradually reduce operational and marketing expenses after capturing significant market share to improve Net Profit %.
- Shift from flat post-discounting to a performance-based model per product and customer in each market.
- Expand distribution and targeted marketing in high-growth region like APAC and in APAC India.
- Reevaluate the pricing or cost structure of the Notebook segment to enhance Net Profit %.
- Investigate the underperformance of USB flash drives and consider repositioning, discontinuing, or introducing improved models.
- Improve forecasting, especially for customers, by leveraging real-time data to minimize stock imbalances and enhance supply chain efficiency.
- Develop targeted strategies to increase market share in North America.
- Focus on differentiation to strengthen competitiveness in the PC segment and challenge dominant players like Dale.
- Optimize marketing spending in the UK and Germany to improve return on investment.
- Align inventory planning and promotions with the September–December sales surge to maximize seasonal demand.


## 📎 Links
🌐 [Linkedin Post](https://www.linkedin.com/feed/update/urn:li:activity:7300182118653902849/)  
- 📊 [Live Dashboard](https://app.powerbi.com/groups/me/reports/a89489a5-56f9-4eee-b555-9e5528c88257/31181b0a108c17909188?experience=power-bi&clientSideAuth=0)

---

## 🧠 Skills Gained

- Gained a deeper understanding of business metrics and their impact on a company's performance.
- Designed insightful, user-centric Power BI dashboards.
- Developed functional knowledge of finance, sales, marketing, and supply chain, and their influence on business outcomes.

---

## 🎓 Acknowledgements

- **Dhaval Patel** — Mentor & Instructor, Codebasics
- **Hemanand Vadivel** — Instructor, Codebasics
- [Codebasics Data Analytics Bootcamp](https://codebasics.io/) — Project guidance and dataset

---

## 🙋 About Me

I am an aspiring Data Analyst with hands-on experience in Power BI, Excel, and SQL — passionate about turning raw data into business insights that drive real decisions.

This project reflects not just technical skills but business thinking — understanding what a CFO, Sales Director, Marketing Head, and Supply Chain Head actually need from data.

---

*Built as part of the Codebasics Data Analytics Bootcamp*
