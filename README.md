# Business-Insights-360
Power BI dashboard analyzing AtliQ Hardware's business performance across Finance, Sales, Marketing, Supply Chain, and Executive views.
# Business Insights 360 — AtliQ Hardware

## 📊 Project Overview

Business Insights 360 is a comprehensive Power BI dashboard 
built for AtliQ Hardware — a global computer hardware and 
peripherals manufacturer operating across APAC, EU, NA, 
and LATAM regions.

The dashboard provides a 360-degree view of business 
performance across Finance, Sales, Marketing, Supply Chain, 
and Executive dimensions — enabling data-driven decisions 
at every level of the organization.

This project was built as part of the Codebasics Data 
Analytics Bootcamp.

---

## 🔗 Live Dashboard

👉 [View Live Power BI Dashboard](#) ← Replace with your link

---

## 🎯 Business Problem

AtliQ Hardware was relying on Excel-based reporting which 
was unable to handle the scale and complexity of their 
growing global operations. Leadership needed a single 
source of truth — a unified dashboard that could surface 
actionable insights across all business functions quickly 
and accurately.

---

## 💡 Key Insights Delivered

### Finance
- Net Sales reached $19.37bn — up 61.5% vs Last Year
- Net Profit is -20.71% driven by Operational Expense 
  of $11,061M exceeding Gross Margin of $7,051M
- Pre Invoice and Post Invoice Deductions consuming 
  53% of Gross Sales — growing faster than revenue

### Sales
- Every product segment shows declining GM% vs Last Year
- Amazon — largest customer — grew 58.5% in revenue 
  but GM% declined -5.2%, signaling over-discounting
- APAC region shows healthiest GM% positioning 
  across all regions

### Marketing
- India is AtliQ's largest market at $4,623M NS but 
  most loss-making at -42.30% Net Profit
- South Korea is the only major market with positive 
  Net Profit at +1.23% — a profitability benchmark
- No product category is currently profitable — 
  structural cost problem, not a product problem

### Supply Chain
- Forecast Accuracy improved to 91.41% (+0.57% vs LY)
- Absolute Error grew 48.32% to 37M — errors scaling 
  with business growth
- AtliQ Exclusive — highest margin channel — is 
  consistently Out of Stock due to under-forecasting

---

## 🗂️ Dashboard Views

| View | Purpose |
|------|---------|
| Home | Navigation hub for all views |
| Finance | P&L Statement, GM% trend, Net Sales performance |
| Sales | Customer & Product Performance Matrix, Unit Economics |
| Marketing | Segment & Market Profitability, GM% scatter analysis |
| Supply Chain | Forecast Accuracy, Net Error, Risk by Customer & Product |
| Executive | Top level KPIs, Market Share, Yearly trends |

---

## 🛠️ Tools & Technologies

| Tool | Usage |
|------|-------|
| Power BI Desktop | Dashboard development |
| Power Query | Data transformation & ETL |
| DAX | Calculated measures & KPIs |
| MySQL | Data source & extraction |
| Excel | Data validation & exploration |

---

## 📐 Data Model

- Fact tables: Sales, Forecast, Market Share
- Dimension tables: Customer, Product, Market, Date
- Star schema design for optimized query performance
- Data loaded through MySQL → Power Query → Power BI

---

## 📸 Dashboard Screenshots

### Home Page
![Home](screenshots/home.png)

### Finance View
![Finance](screenshots/finance.png)

### Sales View
![Sales](screenshots/sales.png)

### Marketing View
![Marketing](screenshots/marketing.png)

### Supply Chain View
![Supply Chain](screenshots/supply_chain.png)

### Executive View
![Executive](screenshots/executive.png)

---

## 📁 Repository Structure
atliq-business-insights-360/
│
├── README.md
├── BusinessInsights360.pbix
│
└── screenshots/
├── home.png
├── finance.png
├── sales.png
├── marketing.png
├── supply_chain.png
└── executive.png
---

## 🎓 Acknowledgements

- **Dhaval Patel** — Mentor & Instructor, Codebasics
- **Hemanand Vadivel** — Instructor, Codebasics
- **Codebasics Data Analytics Bootcamp** — Project guidance 
  and dataset

---

## 🙋 About Me

I am an aspiring Data Analyst with skills in Power BI, 
Excel, and SQL — passionate about turning raw data into 
Business insights that drive decisions.

📧 [Your Email]
💼 [Your LinkedIn Profile URL]
🐙 [Your GitHub Profile URL]
