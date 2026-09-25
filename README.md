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
The **NŌR Real Estate Intelligence Dashboard** is an enterprise-grade financial analytics and sales tracking system designed in Power BI. Built to manage 9 flagship multi-tier developments (including Skyline, Degla Landmark, One Kattameya, Lake Front, and Crystal Plaza), the platform solves the core business challenge of monitoring real estate receivables, contract progression, and multi-bank installment schedules.

### 📊 Core Key Performance Indicators (KPIs)
- 📑 **Total Sales Transactions:** **3,088 validated unit contracts**
- 💵 **Total Tracked Installments:** **21,616 payment milestones**
- ⏱️ **Average Milestones per Contract:** **7.00 installment milestones / unit**
- 🏦 **Multi-Bank Banking Coverage:** **9 Commercial Banks** (National Bank of Egypt, CIB, Banque Misr, QNB Egypt, AAIB, Alex Bank, Banque du Caire, Credit Agricole, EGBANK)
- 🏗️ **Flagship Developments Modeled:** 9 mega-projects across residential, commercial, and mixed-use portfolios

---

## 🎯 Business Problem & Objectives
1. 📈 **Cash Flow Predictability:** Provide milestone-by-milestone visibility into projected collections, overdue installments, and future liquidity.
2. 🏦 **Commercial Banking Channel Optimization:** Monitor clearance cycles, transaction volumes, and collection distributions across 9 partner banks.
3. 🏢 **Project Sales Velocity & Unit Mix:** Track absorption rates, sold inventory, and pricing performance across developments.
4. 💳 **Payment Plan Risk Assessment:** Compare structured bank financing vs. direct cash installment structures to mitigate customer default exposure.

---

## 💡 In-Depth Data Analysis & Business Insights
- 📑 **Milestone Density & Collection Complexity:** Managing **21,616 milestones across 3,088 contracts** demands installment-level granular tracking; macro contract-level metrics obscure short-term cash flow gaps.
- 🏦 **Banking Partner Concentration:** Over 68% of financed installment volumes flow through the top 3 commercial banks (NBE, CIB, and Banque Misr), underscoring the value of streamlined banking reconciliation.
- 🏢 **Development Velocity Variations:** Skyline and Degla Landmark lead transaction velocity (over 45% of total units), while premium waterfront projects generate superior per-square-meter revenue margins.
- 💰 **Cash vs. Bank Settlement Profiles:** Cash installment plans show higher average ticket sizes but require active aging analysis to maintain collection pacing compared to direct bank debits.

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
  <img src="./Dashboard%20Previews/Summary%20By%20Date%20Page.png" alt="NŌR Dashboard — Summary by Date" width="95%">
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
- 📐 **DAX (Data Analysis Expressions):** Milestone Collection Rate %, Outstanding Receivables, Cash Flow Projection, Average Ticket Value
- 🧹 **Power Query (M):** Multi-table staging, installment reconciliation, data normalization
- 🏗️ **Data Architecture:** Galaxy Schema with dual shared dimensions across sales and installments

---

## 📜 License & Author
- **Author:** Kerelos Nakhla ([GitHub](https://github.com/Kerelos-Nakhla))
- **License:** MIT License
