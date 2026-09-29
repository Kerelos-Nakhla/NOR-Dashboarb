# 🏢 NŌR Real Estate Analytics & Financial Intelligence Dashboard

<p align="center">
  <b>Executive Portfolio & Cash Flow Intelligence System for Multi-Project Real Estate Developments</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Power BI" />
  <img src="https://img.shields.io/badge/DAX-Cash_Flow_Intelligence-blue?style=for-the-badge" alt="DAX" />
  <img src="https://img.shields.io/badge/Real_Estate-Portfolio_Analytics-success?style=for-the-badge" alt="Real Estate" />
  <img src="https://img.shields.io/badge/Banking-Receivables_Tracking-orange?style=for-the-badge" alt="Receivables" />
</p>

---

## 📌 Executive Overview
The **NŌR Real Estate Intelligence Dashboard** is an enterprise-grade financial analytics and sales tracking system built in Power BI. Modeling **8 flagship multi-tier developments** across Greater Cairo, Giza, and the North Coast, the system monitors **18.64B EGP** in contracted sales, tracks **21,616 installment milestones**, and provides actionable visibility into receivables, overdue collections, and banking clearance across **9 commercial banking partners**.

---

## 📊 Portfolio Financial Summary & Core KPIs

| Metric | Portfolio Value | Description / Business Impact |
| :--- | :--- | :--- |
| **Gross Contracted Sales** | **18,639.15M EGP (~18.64B)** | Total contract value across 3,088 sold residential and commercial units |
| **Total Invoiced Amount** | **14,229.22M EGP (~14.23B)** | Total milestone value that has matured (`Paid` + `Due - Not Paid`) |
| **Total Amount Collected** | **13,094.37M EGP (~13.09B)** | Cash and banking receipts cleared into development accounts |
| **Outstanding Receivables (Overdue)** | **1,134.85M EGP (~1.13B)** | Overdue installment arrears requiring collections intervention |
| **Future Pipeline (Not Due)** | **4,409.93M EGP (~4.41B)** | Contracted cash flow pipeline maturing in upcoming fiscal quarters |
| **Invoiced Collection Rate** | **92.02%** | Proportion of matured milestone values collected to date |
| **Gross Portfolio Absorption** | **4.17%** | 3,088 units contracted out of 74,040 adopted master-plan units |
| **Installment Milestones** | **21,616 Milestones** | 12,241 Paid (56.6%), 1,381 Overdue (6.4%), 7,994 Future (37.0%) |
| **Average Milestone Density** | **7.00 Payments / Unit** | Average installment schedule length across financing plans |

---

## 📈 Project-Level Performance & Receivables Breakdown

The portfolio spans 8 major developments with distinct sales velocities, ticket sizes, and cash flow profiles:

| Project | Location | Adopted Units | Sold Units | Sold % | Gross Sales (EGP) | Collected (Paid) | Overdue (Arrears) | Future Pipeline | Invoiced Collection Rate |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Skyline Katamya** | Katameya, Cairo | 13,500 | 528 | 3.9% | 5,667.6M | 5,186.2M | 198.0M | 283.4M | **96.3%** |
| **One Kattameya** | Katameya, Cairo | 3,572 | 640 | 17.9% | 3,405.3M | 2,370.5M | 122.8M | 912.0M | **95.1%** |
| **Degla Landmark** | Nasr City, Cairo | 5,082 | 600 | 11.8% | 2,946.8M | 2,791.6M | 155.2M | 0.0M | **94.7%** |
| **Rihana** | Maadi, Cairo | 891 | 455 | 51.1% | 2,266.0M | 922.9M | 95.4M | 1,247.7M | **90.6%** |
| **Crystal Plaza Maadi** | Maadi, Cairo | 635 | 317 | 49.9% | 1,519.4M | 975.5M | 41.7M | 502.2M | **95.9%** |
| **Lake Front 6** | 6th of October, Giza | 1,203 | 249 | 20.7% | 1,380.3M | 207.1M | 68.9M | 1,104.3M | **75.0%** |
| **Degla Palms 6 October** | 6th of October, Giza | 23,928 | 279 | 1.2% | 1,309.5M | 516.0M | 81.7M | 711.8M | **86.3%** |
| **Zahra North Coast** | Sidi Abdel Rahman, Alex | 25,132 | 20 | 0.1% | 145.4M | 118.0M | 27.4M | 0.0M | **81.2%** |

---

## 💡 In-Depth Financial Analysis & Key Insights

1. **High Invoiced Collection Efficiency (92.0%):**
   Matured installments show strong realization across mature Cairo projects (Skyline at 96.3%, Crystal Plaza at 95.9%, and One Kattameya at 95.1%), indicating high customer compliance on prime developments.
2. **Receivables Risk Concentration:**
   Outstanding arrears stand at **1.13B EGP** across 1,381 overdue milestones. The largest absolute arrears are in Skyline (198.0M EGP) and Degla Landmark (155.2M EGP), whereas Lake Front 6 exhibits the lowest collection rate (75.0%) due to newer schedule commencements.
3. **Banking Channel Clearance vs. Direct Cash:**
   Financed receivables flow through 9 major partner institutions (National Bank of Egypt, CIB, Banque Misr, QNB, AAIB, Alex Bank, Banque du Caire, Credit Agricole, EGBANK). Over 68% of banking installments concentrate in NBE, CIB, and Banque Misr.
4. **Future Cash Flow Realization (4.41B EGP Pipeline):**
   With 7,994 unbilled future milestones totaling 4.41B EGP, Rihana (1.25B EGP) and Lake Front 6 (1.10B EGP) represent the primary medium-term cash generators.

---

## 📐 Key DAX Measures & Formula Reference

The semantic model contains over **130 DAX measures** organized across calculation tables (`global_summary`, `collection_by_date_summary`, `8 Projects`, and `HTML Visuals`).

### 1. Global Portfolio Invoicing & Receivables
Tracks matured receivables, cleared cash, and outstanding balances across the portfolio:

```dax
// Total cleared payments
Amount Collected = 
CALCULATE(
    SUM(fact_installments[installment_amount]), 
    fact_installments[installment_status] = "Paid"
)

// Total matured milestone invoices (Paid + Due)
Invoiced Amount = 
CALCULATE(
    SUM(fact_installments[installment_amount]), 
    fact_installments[installment_status] IN {"Paid", "Due - Not Paid"}
)

// Arrears balance due
Outstanding Balance = 
[Invoiced Amount] - [Amount Collected]

// Contracted unit absorption rate
Sold % = 
DIVIDE([# Sold], [# Units])

// Total units adopted in master plan
# Units = 
SUM(dim_project[adopted_total_units])

// Total contracted units sold
# Sold = 
COUNTROWS(fact_sales)
```

### 2. Multi-Channel Segmentation (Bank Facilities vs. Direct Cash)
Differentiates commercial banking debt service from direct developer cash installments:

```dax
// Outstanding receivables tied to commercial banking facilities
Bank Outstanding = 
SUMX(
    FILTER(fact_sales, RELATED(dim_bank[bank/cash]) = "Bank"), 
    [Outstanding Balance]
)

// Direct buyer cash installment arrears
Cash Outstanding = 
SUMX(
    FILTER(fact_sales, RELATED(dim_bank[bank/cash]) = "Cash"), 
    [Outstanding Balance]
)
```

### 3. Project-Specific Milestone Intelligence (104 Measures Across 8 Projects)
Evaluates milestone collection efficiency per development (sample for Crystal Plaza Maadi and Skyline):

```dax
// Issued milestone count excluding unbilled future installments
Issued Invoices Crystal Plaza Maadi = 
CALCULATE(
    COUNTROWS(fact_installments),
    dim_project[project_name] = "Crystal Plaza Maadi",
    fact_installments[installment_status] <> "Not Due",
    FILTER(fact_installments, fact_installments[installment_status] = "Paid" || fact_installments[installment_amount] > 0)
)

// Collected milestone invoices count
Collected Invoices Crystal Plaza Maadi = 
CALCULATE(
    COUNTROWS(fact_installments), 
    fact_installments[installment_status] = "Paid", 
    dim_project[project_name] = "Crystal Plaza Maadi"
)

// Milestone collection rate %
Collection Invoices Rate Crystal Plaza Maadi = 
DIVIDE([Collected Invoices Crystal Plaza Maadi], [Issued Invoices Crystal Plaza Maadi])

// Outstanding arrears amount for project
Outstanding Amount Crystal Plaza Maadi = 
CALCULATE(
    SUM(fact_installments[installment_amount]), 
    fact_installments[installment_status] = "Due - Not Paid", 
    dim_project[project_name] = "Crystal Plaza Maadi"
)

// Total invoice amount (Collected + Outstanding)
Total Invoice Amount Crystal Plaza Maadi = 
[Collected Amount Crystal Plaza Maadi] + [Outstanding Amount Crystal Plaza Maadi]
```

### 4. Dynamic Time Intelligence & Period-Over-Period Tracking
Computes period movements without rigid calendar limits:

```dax
// Collections realized in the active date context
Collected New = 
CALCULATE([Amount Collected])

// Cumulative collections prior to the active date filter
Collected Old = 
CALCULATE(
    [Amount Collected], 
    dim_date[Date] < MIN(dim_date[Date])
)

// Active outstanding arrears in current window
Outstanding New = 
CALCULATE([Outstanding Balance])

// Historical outstanding arrears before current window
Outstanding Old = 
CALCULATE(
    [Outstanding Balance], 
    dim_date[Date] < MIN(dim_date[Date])
)

// Active sales count in window
Rows New = 
CALCULATE(COUNTROWS(fact_sales))

// Historical sales count prior to window
Rows Old = 
CALCULATE(
    COUNTROWS(fact_sales), 
    dim_date[Date] < MIN(dim_date[Date])
)
```

---

## 🎯 Business Problem & Objectives
1. 📈 **Cash Flow Predictability:** Milestone-by-milestone visibility into projected collections, overdue installments, and future liquidity.
2. 🏦 **Commercial Banking Channel Optimization:** Monitor clearance cycles, transaction volumes, and collection distributions across 9 partner banks.
3. 🏢 **Project Sales Velocity & Unit Mix:** Track absorption rates, sold inventory, and pricing performance across developments.
4. 💳 **Payment Plan Risk Assessment:** Compare structured bank financing vs. direct cash installment structures to mitigate customer default exposure.

---

## 🖼️ Dashboard Visual Tour & Storytelling

### 1. Landing Page
<p align="center">
  <img src="./Dashboard%20Previews/Landing%20Page.png" alt="NŌR Dashboard — Landing" width="95%">
</p>

### 2. Global Summary (View 1)
<p align="center">
  <img src="./Dashboard%20Previews/1-%20Global%20Summary%20Page.png" alt="NŌR Dashboard — 1 - Global Summary" width="95%">
</p>

### 3. Global Summary (View 2)
<p align="center">
  <img src="./Dashboard%20Previews/2-%20Global%20Summary%20Page.png" alt="NŌR Dashboard — 2 - Global Summary" width="95%">
</p>

### 4. Summary by Date & Collection Aging
<p align="center">
  <img src="./Dashboard%20Previews/Summary%20by%20Date%20Page.png" alt="NŌR Dashboard — Summary By Date Page" width="95%">
</p>

### 5. Project Portfolio Summary
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Summary.png" alt="NŌR Dashboard — Project Summary" width="95%">
</p>

### 6. Project Installments & Cash Schedules
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Installments.png" alt="NŌR Dashboard — Project Installments" width="95%">
</p>

### 7. Project Installments — Option 1
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Installments%20First%20Option%20.png" alt="NŌR Dashboard — Option 1" width="95%">
</p>

### 8. Project Installments — Option 2
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Installment%20Second%20Option.png" alt="NŌR Dashboard — Option 2" width="95%">
</p>

### 9. Project Summary by Bank
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Summary%20By%20Bank.png" alt="NŌR Dashboard — Project Summary by Bank" width="95%">
</p>

### 10. Project Installments by Bank
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Installments%20By%20Bank.png" alt="NŌR Dashboard — Project Installment by Bank" width="95%">
</p>

### 11. Project Summary by Cash
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Summary%20By%20Cash.png" alt="NŌR Dashboard — Project Summary by Cash" width="95%">
</p>

### 12. Project Installments by Cash
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Installments%20By%20Cash.png" alt="NŌR Dashboard — Project Installment by Cash" width="95%">
</p>

### 13. Project Summary by Bank Wise
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Summary%20By%20Bank%20Wise.png" alt="NŌR Dashboard — Bank Wise Summary" width="95%">
</p>

---

## 🏗️ Data Architecture & Star Schema
The enterprise data model utilizes a multi-fact Galaxy Schema connecting contracts, milestone receivables, and commercial banks:

- **Fact Tables:**
  - `fact_sales` — Unit sales contracts, transaction dates, customer keys, project keys, contract values
  - `fact_installments` — Milestone payment schedules, due dates, payment status, settlement values, bank IDs
- **Dimension Tables:**
  - `dim_project` — Development names, phases, locations, master project IDs
  - `dim_unit` — Unit types (Apartments, Duplexes, Penthouses, Commercial), floor plans, gross areas
  - `dim_customer` — Investor and resident profiles, national IDs, contact classifications
  - `dim_bank` — Banking partners (NBE, CIB, Banque Misr, QNB, AAIB, Alex Bank, Banque du Caire, Credit Agricole, EGBANK)
  - `dim_payment_plan` — Down payment ratios, milestone frequencies, grace periods
  - `dim_date` — Financial calendar hierarchy, due month, quarter, maturity fiscal year

### 📐 Model Representation
<p align="center">
  <img src="./Dashboard%20Previews/Model.png" alt="NŌR Dashboard — Galaxy Schema Data Model" width="95%">
</p>

---

## 🛠️ Tools & Technologies
- 📊 **Power BI Desktop:** Multi-level financial reports, interactive project matrix, banking drill-downs
- 📐 **DAX (Data Analysis Expressions):** 130+ dynamic measures for receivables, collection rates, aging, and variance intelligence
- 🗄️ **Power BI Project (PBIP) & TMDL:** Source-control ready tabular model definition language
- ⚡ **Power Query (M):** Multi-table staging, installment reconciliation, data normalization
- 🏗️ **Data Architecture:** Galaxy Schema with dual shared dimensions across sales and installments

---

## 📜 License & Author
- **Author:** Kerelos Nakhla ([GitHub](https://github.com/Kerelos-Nakhla))
- **License:** MIT License
