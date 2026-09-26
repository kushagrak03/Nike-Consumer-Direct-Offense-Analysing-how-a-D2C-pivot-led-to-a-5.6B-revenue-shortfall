Nike Consumer Direct Offense — Forensic BI Analysis
How a D2C Pivot Led to a $5.6B Revenue Shortfall | FY2015–FY2024
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=flat-square&logo=mysql&logoColor=white)
![Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=flat-square&logo=microsoft-excel&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=tableau&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square)
![Year](https://img.shields.io/badge/Data-FY2015--FY2024-navy?style=flat-square)
---
What This Project Is About
In 2017, Nike made one of the boldest strategic moves in retail history. They announced what they called the Consumer Direct Offense (CDO) — a plan to cut ties with over 50,000 wholesale retail partners like Foot Locker and department stores, and instead sell directly to customers through their own stores, website and apps.
The logic was clean: remove the middleman, keep more of the margin, own the customer relationship. And for a few years, it looked like it was working.
But by 2022, Nike was sitting on $9.7 billion of unsold inventory. Their operating margin had fallen from a peak of 15.58% to 12.29%. Their stock had dropped nearly 60% from its all-time high. Challenger brands like Hoka and On Running — which barely existed as competitors in 2017 — had quietly taken 8 points of market share while Nike was focused inward.
This project is my attempt to understand exactly what happened — using real financial data, SQL analysis, Excel modelling and a Tableau dashboard to break it down finding by finding.
---
Live Dashboard
> Click below to explore the interactive Tableau dashboard — filter by year, channel and metric to explore the findings yourself.
→ Open the Nike CDO Forensic BI Dashboard on Tableau Public
---
Key Findings at a Glance
Finding	What the Data Shows
📉 Margin Illusion	Operating margin fell 354 bps from peak despite D2C share rising to 44%
🏪 Wholesale Divorce	50,000+ accounts cut; wholesale revenue plateaued and declined in absolute terms
📦 Inventory Trap	Inventory peaked at $9.7B in Q4 FY2022 — forced heavy discounting
🏃 Competitor Surge	Nike market share: 38.2% → 30.2% while Hoka went 0.8% → 7.4%
💰 CLV Trap	Wholesale LTV:CAC of 24x+ vs D2C digital at 6.5x — D2C customers cost far more to acquire
📊 Market Verdict	NKE stock fell ~60% from Nov 2021 peak; inventory crisis caused −11.1% 30-day return
🔮 Revenue Gap	Balanced 60/40 strategy would have generated an estimated ~$5.6B more in FY2024
---
What I Built
1. MySQL Database — 7 Tables, 5 Query Blocks
Built a relational database with 7 tables covering Nike's financials, channel revenue, stock events, market share, CLV estimates, quarterly detail and scenario forecasts. Ran 5 analytical SQL query blocks using:
`JOIN` across financial and channel tables
`LAG()` window functions for year-on-year growth
`RANK()` for CLV and LTV:CAC ranking
`CASE WHEN` for strategy phase classification
`SUM() OVER()` for cumulative stock return analysis
`CTEs` for multi-step calculations
2. Excel Financial Model — 8 Tabs
Built a structured master model with RAW data tabs, CALC analytical tabs and a DASHBOARD summary tab. Key outputs:
Channel revenue shift and indexed growth comparison
CLV model across 6 customer segments with sensitivity analysis
Three-scenario revenue forecast (Balanced / Actual / Recovery)
RAG status dashboard for 8 key metrics
3. Tableau Public Dashboard — 7 Charts
An interactive dashboard with cross-filtering between all charts:
The Margin Illusion — Gross Margin vs Operating Margin (FY2015–FY2024)
The Wholesale Divorce — D2C vs Wholesale revenue shift
Market Share Erosion — Nike vs Hoka, On Running, New Balance, Adidas
CLV Channel Comparison — LTV:CAC by channel type
Stock Event Study — 30-day returns after each strategic decision
Inventory Crisis — Quarterly inventory vs revenue
Recovery Blueprint — Three scenario revenue forecasts through FY2027
---
Repository Structure
```
nike-cdo-forensic-bi-analysis/
│
├── Data/
│   ├── 01\_Nike\_Annual\_Financials.csv
│   ├── 02\_Nike\_Channel\_Revenue.csv
│   ├── 03\_Nike\_Stock\_Events.csv
│   ├── 04\_Market\_Share\_Competitor.csv
│   ├── 05\_CLV\_Customer\_Model.csv
│   ├── 06\_Nike\_Quarterly\_Detail.csv
│   └── 07\_Scenario\_Forecast.csv
│
├── SQL/
│   ├── SQL\_Q1\_Channel\_Shift.csv
│   ├── SQL\_Q2\_Margin\_Erosion.csv
│   ├── SQL\_Q3\_Market\_Share.csv
│   ├── SQL\_Q4\_CLV\_Analysis.csv
│   └── SQL\_Q5\_Stock\_Events.csv
│
├── Excel/
│   └── Nike\_OIO\_MasterModel.xlsx
│
├── Report/
│   └── Nike\_CDO\_CaseStudy\_Report.pdf
│
└── README.md
```
---
Data Sources
All data used in this project is publicly available. No proprietary or paid data was used.
#	Source	Used For
1	Nike 10-K SEC Filings (FY2015–FY2024)	Revenue, margins, channel splits
2	Macrotrends.net	Historical financial data
3	Yahoo Finance (NKE)	Stock price history
4	Industry market share estimates	Competitor share data
5	Nike Investor Relations	D2C vs wholesale disclosures
---
The Numbers That Tell the Story
```
Peak Operating Margin (FY2021)     →    15.58%
Operating Margin FY2024            →    12.29%   ↓ 354 bps

Nike Market Share FY2017           →    38.2%
Nike Market Share FY2024           →    30.2%    ↓ 8 pts

Hoka Market Share FY2017           →    0.8%
Hoka Market Share FY2024           →    7.4%     ↑ 6.6 pts

Peak Inventory (Q4 FY2022)         →    $9.7B
NKE Stock — Nov 2021 Peak          →    \~$177
NKE Stock — Jun 2024 Low           →    \~$70     ↓ \~60%

Estimated Revenue Gap vs
Balanced Channel Strategy          →    \~$5.6B   (FY2024)
```
---
About
Kushagra Kumar
Final Year | Electronics & Telecommunications Engineering
IET DAVV, Indore | Aspiring Data Analyst
I am a final year engineering student with a background in social media management and brand strategy. This is my first data analytics portfolio project — built entirely using MySQL, Excel and Tableau Public with publicly available data.
![GitHub](https://github.com/kushagrak03)
![Tableau](https://public.tableau.com/app/profile/kushagra.kumar5547/viz/NIKEProjectAnalysis/Dashboard1)
---
> \*All analysis is for educational and portfolio purposes. Data sourced entirely from publicly available financial records and industry reports.\*

