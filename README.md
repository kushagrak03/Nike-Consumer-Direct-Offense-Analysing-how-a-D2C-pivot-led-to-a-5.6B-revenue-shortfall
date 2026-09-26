# 📊 Nike Consumer Direct Offense — Forensic BI Analysis

> **How a D2C Pivot Led to a $5.6B Revenue Shortfall | FY2015–FY2024**

[![MySQL](https://img.shields.io/badge/MySQL-005C84?style=flat-square&logo=mysql&logoColor=white)](https://mysql.com)
[![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=flat-square&logo=microsoft-excel&logoColor=white)](https://microsoft.com/excel)
[![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/kushagra.kumar5547/viz/NIKEProjectAnalysis/Dashboard1)
[![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)](https://github.com/kushagrak03)
[![Data](https://img.shields.io/badge/Data-FY2015--FY2024-1A1A2E?style=flat-square)](https://github.com/kushagrak03)

> 📊 **Live Interactive Dashboard → [View on Tableau Public](https://public.tableau.com/app/profile/kushagra.kumar5547/viz/NIKEProjectAnalysis/Dashboard1)**

---

## 📌 Overview

In 2017, Nike announced one of the boldest strategic moves in retail history — the **Consumer Direct Offense (CDO)**. The plan was to cut over 50,000 wholesale retail partners like Foot Locker and department stores, and sell directly to customers through Nike's own stores, website and apps.

The logic was clean: remove the middleman, keep more of the margin, own the customer relationship. For a few years, it looked like it was working.

But by 2022, the cracks were visible. Nike was sitting on **$9.7 billion of unsold inventory**. Operating margin had fallen from a peak of 15.58% to 12.29%. The stock dropped nearly 60% from its all-time high. Challenger brands like Hoka and On Running — barely competitors in 2017 — had quietly taken 8 points of market share while Nike was focused inward.

This project is a forensic business intelligence analysis of exactly what happened — built using real public financial data, SQL analysis, Excel financial modelling and an interactive Tableau dashboard.

---

## 🖥️ Live Dashboard

> Click below to explore the interactive Tableau dashboard — filter by year, channel and metric across all 7 charts.

**[→ Nike CDO Forensic BI Dashboard on Tableau Public](https://public.tableau.com/app/profile/kushagra.kumar5547/viz/NIKEProjectAnalysis/Dashboard1)**

---

## 🏗️ Project Architecture

```
Layer 1 – Data Collection:    Nike 10-K SEC Filings | Macrotrends.net | Yahoo Finance NKE
          ↓
Layer 2 – Data Storage:       MySQL Database (7 Tables | 80+ Records | nike_ois_db)
          ↓
Layer 3 – SQL Analysis:       5 Query Blocks (CTEs | Window Functions | JOINs | RANK)
          ↓
Layer 4 – Financial Model:    Excel Master Model (8 Tabs | CLV | Scenario Forecast | RAG Dashboard)
          ↓
Layer 5 – Visualisation:      Tableau Public (7-Chart Interactive Dashboard | Cross-Filtering)
          ↓
Layer 6 – Deliverable:        Forensic PDF Case Study Report (21 Pages)
```

---

## 📁 Repository Structure

```
nike-cdo-forensic-bi-analysis/
│
├── Data/                          # Source datasets
│   ├── 01_Nike_Annual_Financials.csv       # FY2015–FY2024 revenue, margins, SGA
│   ├── 02_Nike_Channel_Revenue.csv         # D2C vs Wholesale split by year
│   ├── 03_Nike_Stock_Events.csv            # Strategic events + 30d/90d stock returns
│   ├── 04_Market_Share_Competitor.csv      # Nike vs Hoka, On Running, Adidas, NB
│   ├── 05_CLV_Customer_Model.csv           # CLV and LTV:CAC by channel segment
│   ├── 06_Nike_Quarterly_Detail.csv        # 24 quarters of granular P&L data
│   └── 07_Scenario_Forecast.csv            # 3-scenario revenue forecast FY2017–FY2027
│
├── SQL/                           # Query outputs from MySQL
│   ├── SQL_Q1_Channel_Shift.csv            # YoY D2C vs Wholesale revenue change
│   ├── SQL_Q2_Margin_Erosion.csv           # Gross vs Operating margin timeline
│   ├── SQL_Q3_Market_Share.csv             # Competitor market share analysis
│   ├── SQL_Q4_CLV_Analysis.csv             # CLV ranking by channel and segment
│   └── SQL_Q5_Stock_Events.csv             # Event study with cumulative returns
│
├── Excel/                         # Financial model
│   └── Nike_OIO_MasterModel.xlsx           # 8-tab master model (RAW + CALC + DASHBOARD)
│
├── Report/                        # Case study
│   └── Nike_CDO_CaseStudy_Report.pdf       # 21-page forensic analysis report
│
└── README.md                      # This file
```

---

## 🔍 Key Findings

| # | Finding | What the Data Shows |
|---|---------|---------------------|
| 1 | 📉 **The Margin Illusion** | Operating margin fell 354 bps from peak despite D2C share rising to 44% |
| 2 | 🏪 **The Wholesale Divorce** | 50,000+ accounts cut; wholesale revenue declined in absolute terms from FY2022 |
| 3 | 📦 **The Inventory Trap** | Inventory peaked at $9.7B in Q4 FY2022 — forced heavy discounting |
| 4 | 🏃 **Competitor Surge** | Nike share: 38.2% → 30.2% while Hoka grew 0.8% → 7.4% and On Running 0.3% → 6.8% |
| 5 | 💰 **The CLV Trap** | Wholesale LTV:CAC of 24x+ vs D2C digital at 6.5x — D2C costs far more to acquire |
| 6 | 📊 **Market Verdict** | NKE fell ~60% from Nov 2021 peak; inventory crisis caused −11.1% 30-day return |
| 7 | 🔮 **Revenue Gap** | Balanced 60/40 strategy would have generated an estimated ~$5.6B more in FY2024 |

---

## ⚙️ What I Built

### 1. MySQL Database — 7 Tables, 5 Query Blocks

Built a relational database (`nike_ois_db`) with 7 tables and ran 5 analytical SQL query blocks:

| Query | Purpose | Key Technique |
|-------|---------|---------------|
| Q1 — Channel Shift | YoY D2C vs Wholesale growth | `LAG()` window function |
| Q2 — Margin Erosion | Gross vs Operating margin timeline | `JOIN` + `CASE WHEN` phase labels |
| Q3 — Market Share | Competitor share erosion | `FIRST_VALUE()` + running delta |
| Q4 — CLV Analysis | Channel value ranking | `RANK()` + `PARTITION BY` |
| Q5 — Stock Events | Strategic decision returns | `SUM() OVER()` cumulative return |

### 2. Excel Financial Model — 8 Tabs

| Tab | Type | Contents |
|-----|------|---------|
| RAW_Financial | Data | 10-year P&L from Nike 10-K filings |
| RAW_Channel | Data | D2C vs Wholesale annual split |
| RAW_Product_Market | Data | Market share + CLV segment data |
| RAW_Stock_Events | Data | Stock prices + strategic event log |
| CALC_ChannelModel | Analysis | YoY growth, indexed revenue, scenario gap |
| CALC_CustomerCLV | Analysis | 6-segment CLV model + sensitivity table |
| CALC_MarketReaction | Analysis | Event study + cumulative return scoring |
| DASHBOARD_Summary | Output | 8 KPI cards + RAG status table + sparklines |

### 3. Tableau Public Dashboard — 7 Charts

| Chart | Title | Key Insight |
|-------|-------|-------------|
| 1 | The Margin Illusion | Gross margin held; operating margin collapsed post-2021 |
| 2 | The Wholesale Divorce | Wholesale revenue peaked and declined in absolute terms |
| 3 | Market Share Erosion | 8-point share loss to challenger brands |
| 4 | CLV Channel Comparison | Wholesale LTV:CAC 4x better than D2C digital |
| 5 | Stock Event Study | Market penalised every CDO overreach decision |
| 6 | The Inventory Trap | $9.7B inventory crisis clearly visible in quarterly data |
| 7 | The Recovery Blueprint | Three scenario revenue forecasts through FY2027 |

---

## 📊 Key Numbers

```
Peak Operating Margin (FY2021)          →    15.58%
Operating Margin FY2024                 →    12.29%    ↓ 354 bps

Nike Market Share FY2017                →    38.2%
Nike Market Share FY2024                →    30.2%     ↓ 8 pts

Hoka Market Share FY2017                →    0.8%
Hoka Market Share FY2024                →    7.4%      ↑ 6.6 pts

On Running Market Share FY2017          →    0.3%
On Running Market Share FY2024          →    6.8%      ↑ 6.5 pts

Peak Inventory (Q4 FY2022)             →    $9.7B
Wholesale Accounts Cut (FY2019–2022)   →    50,000+

NKE Stock Peak (Nov 2021)              →    ~$177
NKE Stock Low (Jun 2024)               →    ~$70      ↓ ~60%

Estimated Revenue Gap vs
Balanced Channel Strategy (FY2024)     →    ~$5.6B
```

---

## 🗄️ Data Sources

All data used in this project is publicly available. No proprietary or paid data was used.

| # | Source | Used For |
|---|--------|---------|
| 1 | Nike 10-K SEC Annual Filings (FY2015–FY2024) | Revenue, margins, channel splits, SGA |
| 2 | Macrotrends.net | Historical quarterly financial data |
| 3 | Yahoo Finance (Ticker: NKE) | Stock price history FY2017–FY2024 |
| 4 | Nike Investor Relations (investors.nike.com) | D2C vs Wholesale official disclosures |
| 5 | Industry market share estimates | Competitor share data (Euromonitor / SGB Online) |

---

## 🧠 Analytical Techniques Used

| Technique | Tool | Purpose |
|-----------|------|---------|
| Window Functions (LAG, RANK, SUM OVER) | MySQL | Year-on-year growth and cumulative analysis |
| Common Table Expressions (CTEs) | MySQL | Multi-step channel shift calculation |
| CLV Modelling | Excel | 6-segment customer lifetime value analysis |
| Scenario Forecasting | Excel (FORECAST.ETS) | 3-path revenue projection through FY2027 |
| Sensitivity Analysis | Excel (Data Table) | CLV response to AOV and frequency changes |
| Event Study Methodology | MySQL + Tableau | 30-day stock return after strategic decisions |
| RAG Status Framework | Excel | Traffic-light health assessment of 8 KPIs |
| Cross-Filter Dashboard | Tableau Public | Interactive 7-chart linked dashboard |

---

## 📄 Case Study Report

The project includes a **21-page forensic PDF case study report** covering:

- Introduction and project motive
- What the Consumer Direct Offense was and why it made sense
- Six findings explained in plain English with supporting data
- Dashboard walkthrough with all chart screenshots embedded
- Three-scenario recovery blueprint with recommendations
- Full glossary of 20 analytical terms with Nike-specific examples
- References and data source disclosure

> 📥 Download: [`Report/Nike_CDO_CaseStudy_Report.pdf`](Report/Nike_CDO_CaseStudy_Report.pdf)

---

## 🛠️ Troubleshooting

| Issue | Solution |
|-------|---------|
| CSV not opening correctly | Open with Excel → Data → From Text/CSV → set delimiter to comma |
| Excel formulas showing errors | Ensure all 7 RAW tabs are populated before opening CALC tabs |
| Tableau dashboard not loading | Check internet connection; try opening in Chrome or Edge |
| MySQL import failing | Use Table Data Import Wizard → select existing table → map columns manually |
| PDF not rendering images | Download and open with Adobe Acrobat Reader for full image display |

---

## 👤 About

**Kushagra Kumar**
Final Year | Electronics & Telecommunications Engineering
IET DAVV, Indore | Aspiring Data Analyst

This is my first data analytics portfolio project — built entirely using MySQL, Excel and Tableau Public with publicly available financial data. I have a background in social media management and brand strategy, which is what drew me to analysing a brand-led strategic failure at this scale.

[![GitHub](https://img.shields.io/badge/GitHub-kushagrak03-181717?style=flat-square&logo=github)](https://github.com/kushagrak03)
[![Tableau](https://img.shields.io/badge/Tableau-View_Dashboard-E97627?style=flat-square&logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/kushagra.kumar5547/viz/NIKEProjectAnalysis/Dashboard1)

---

## 📄 Disclaimer

> *This project is an academic data analysis portfolio piece prepared for educational and career development purposes. All data sourced entirely from publicly available financial records, SEC filings and industry reports. This is not financial advice and no proprietary Nike data was used.*
