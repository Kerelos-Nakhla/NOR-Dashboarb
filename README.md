# NŌR Real Estate Analytics & Financial Intelligence Dashboard

<p align="center">
  <b>Executive Portfolio & Cash Flow Intelligence System for Multi-Project Real Estate Developments</b>
</p>

---

## Executive Overview
The **NŌR Real Estate Intelligence Dashboard** is an enterprise-grade financial analytics and sales tracking system designed in Power BI. Built to manage 9 flagship multi-tier developments (including Skyline, Degla Landmark, One Kattameya, Lake Front, and Crystal Plaza), the platform solves the core business challenge of monitoring real estate receivables, contract progression, and multi-bank installment schedules.

### Core Metrics & Scope (Calculated from Actual Production Data)
- **Total Sales Transactions:** 3,088 validated unit contracts
- **Total Tracked Installments:** 21,616 payment milestones
- **Multi-Bank Portfolio Coverage:** National Bank of Egypt (NBE), CIB, Banque Misr, QNB Egypt, AAIB, Alex Bank, Banque du Caire, Credit Agricole, and EGBANK
- **Key Dimensions:** Real estate unit types, customer profiles, payment structures, project milestones, and banking channels

---

## Business Problem & Analytical Objectives
1. **Cash Flow Predictability:** Real estate developments operate on long-cycle milestone-based receivables. Executive leadership requires granular visibility into collections vs. outstanding balances.
2. **Bank Channel Performance:** Managing customer financing across 9 commercial banks creates operational friction without a unified view of clearance times, default rates, and deposit distributions.
3. **Project Velocity & Unit Mix:** Tracking unit absorption rates, percentage of completion (POC), and installment aging across projects.

## Key Analytical Takeaways
- **Installment intensity:** 21,616 tracked milestones across 3,088 contracts equals an average of **7 installment milestones per contract**, highlighting the importance of installment-level monitoring rather than contract-level reporting alone.
- **Portfolio complexity:** The model combines sales and installment facts with shared customer, project, unit, payment-plan, date, and bank dimensions, allowing receivables to be analyzed from both commercial and collection perspectives.
- **Decision focus:** The dashboard moves from portfolio-level performance to project, payment-plan, bank, and cash views, supporting investigation of where receivables are concentrated and how collection activity is distributed.


---

## Dashboard Visual Tour & Storytelling

### 1. Landing Page
<p align="center">
  <img src="./Dashboard%20Previews/Landing%20Page.png" alt="NŌR Dashboard — Landing" width="95%">
</p>

### 2. 1 - Global Summary
<p align="center">
  <img src="./Dashboard%20Previews/1-%20Global%20Summary%20Page.png" alt="NŌR Dashboard — 1 - Global Summary" width="95%">
</p>

### 3. 2 - Global Summary
<p align="center">
  <img src="./Dashboard%20Previews/2-%20Global%20Summary%20Page.png" alt="NŌR Dashboard — 2 - Global Summary" width="95%">
</p>

### 4. Summary by Date
<p align="center">
  <img src="./Dashboard%20Previews/Summary%20By%20Date%20Page.png" alt="NŌR Dashboard — Summary by Date" width="95%">
</p>

### 5. Project Summary
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Summary.png" alt="NŌR Dashboard — Project Summary" width="95%">
</p>

### 6. Project Installments
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Installments.png" alt="NŌR Dashboard — Project Installments" width="95%">
</p>

### 7. Project Installment - First Option
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Installments%20First%20Option%20.png" alt="NŌR Dashboard — Project Installment - First Option" width="95%">
</p>

### 8. Project Installment - Second Option
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Installment%20Second%20Option.png" alt="NŌR Dashboard — Project Installment - Second Option" width="95%">
</p>

### 9. Project Summary by Bank
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Summary%20By%20Bank.png" alt="NŌR Dashboard — Project Summary by Bank" width="95%">
</p>

### 10. Project Installment by Bank
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Installments%20By%20Bank.png" alt="NŌR Dashboard — Project Installment by Bank" width="95%">
</p>

### 11. Project Summary by Cash
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Summary%20By%20Cash.png" alt="NŌR Dashboard — Project Summary by Cash" width="95%">
</p>

### 12. Project Installment by Cash
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Installments%20By%20Cash.png" alt="NŌR Dashboard — Project Installment by Cash" width="95%">
</p>

### 13. Project Summary by Bank Wise
<p align="center">
  <img src="./Dashboard%20Previews/Project%20Summary%20By%20Bank%20Wise.png" alt="NŌR Dashboard — Project Summary by Bank Wise" width="95%">
</p>

---

## Data Architecture & Model
The semantic model is engineered as a **Galaxy Schema (Constellation Schema)**, connecting two distinct fact tables (`fact_sales` and `fact_installments`) across shared conformed dimensions.

### Model Representation
<p align="center">
  <img src="./Dashboard%20Previews/Model.png" alt="NŌR Dashboard — Galaxy Schema Data Model" width="95%">
</p>

- **Fact Tables:**
  - `fact_sales`: 3,088 unit contracts, unit pricing, total due, total paid, and percentage of completion.
  - `fact_installments`: 21,616 milestone records, installment amounts, status, and due schedules.
- **Conformed Dimensions:**
  - `dim_bank`: Commercial banking entities.
  - `dim_customer`: Buyer demographics and classification.
  - `dim_project`: Development master records, geographic zones, and completion targets.
  - `dim_unit`: Unit inventory, square meter pricing, and floor allocations.
  - `dim_payment_plan`: Flexible milestone installment schedules.
  - `dim_date`: Calendar intelligence enabling YoY and MoM time intelligence DAX calculations.

---

## Tools & Technologies
- **Business Intelligence:** Microsoft Power BI Desktop & Service
- **Modeling & Logic:** Advanced DAX (Time Intelligence, Dynamic Receivables, Bank Share Ratios)
- **Data Transformation:** Power Query (M Language) for ETL and normalization
- **Database Architecture:** Star & Galaxy Schema Design

---

## License & Usage
This repository is released under the [MIT License](LICENSE). Developed by **Kerelos Nakhla** — Data Analyst & BI Developer.
