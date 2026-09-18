# NŌR Developments — Real Estate Sales & Installment Intelligence

<p align="center">
  <strong>Portfolio-Level Real Estate Analytics • Sales Performance • Installment Collection • Bank & Cash Intelligence</strong>
</p>

<p align="center">
  A Power BI analytics solution designed to turn multi-project real estate sales and installment data into a structured view of unit adoption, financial collections, outstanding balances, payment plans, and bank-level exposure.
</p>

---

## Executive Overview

**NŌR Developments** is a real estate analytics project built in **Power BI** around a multi-project sales and installment model.

The solution connects sales, customer, unit, project, payment-plan, bank, and date dimensions with transactional sales and installment facts. The dashboard is designed around a practical management question:

> **How much has been sold, how much has been invoiced and collected, what remains outstanding, and how does the financial position change by project, date, payment channel, and bank?**

Rather than presenting isolated KPIs, the report creates a connected analytical journey from **portfolio-level performance → project performance → installment plans → bank/cash segmentation → bank-wise exposure**.

---

## Business Scope

The dashboard covers **8 real estate projects** across multiple Egyptian markets:

| Project | Location | Adopted Units |
|---|---|---:|
| One Kattameya | Katameya, Cairo | 3,572 |
| Zahra North Coast | Sidi Abdel Rahman / North Coast | 25,132 |
| Degla Landmark | Nasr City, Cairo | 5,082 |
| Skyline Katamya | Katameya, Cairo | 13,500 |
| Degla Palms 6 October | 6th of October, Giza | 23,928 |
| Lake Front 6 | 6th of October, Giza | 1,203 |
| Crystal Plaza Maadi | Zahraa El Maadi, Cairo | 635 |
| Rihana | Zahraa El Maadi, Cairo | 891 |
| **Portfolio Total** | — | **73,943** |

The project portfolio spans **73,943 adopted units**, giving the report a portfolio-level perspective rather than focusing on a single development.

---

## What the Dashboard Answers

### Portfolio Performance
- How many units exist across the development portfolio?
- How many units have been sold/adopted?
- What is the overall sales conversion?
- What is the total invoiced value?
- How much has actually been collected?
- What remains outstanding?

### Project Performance
- Which projects carry the largest unit base?
- How does sales conversion differ between developments?
- How does invoiced value compare with collected value?
- Where is outstanding exposure concentrated?

### Installment Intelligence
- How many invoices have been issued?
- How many have been collected?
- What is the collection rate?
- What amount remains due but unpaid?
- How do payment plans affect the collection profile?

### Bank & Cash Analysis
- How does performance differ between **Bank** and **Cash** channels?
- Which banks are represented in financed sales?
- How much has each bank contributed to collections?
- What is the outstanding balance associated with bank-financed sales?

### Time Analysis
- How does sales and collection activity evolve over time?
- Which periods contribute most to invoiced and collected amounts?
- How does the outstanding balance change across the reporting timeline?

---

## Analytical Highlights

### 1. Large Portfolio Footprint

The model represents **73,943 adopted units across 8 projects**. The portfolio is highly diversified by development scale, with **Zahra North Coast** and **Degla Palms 6 October** representing two of the largest unit bases, while projects such as **Crystal Plaza Maadi** and **Rihana** operate at substantially smaller scales.

This makes portfolio-level aggregation useful, but also makes project-level normalization essential when interpreting sales performance.

### 2. Sales Conversion Is More Informative Than Unit Volume Alone

The dashboard separates:

**Adopted Units → Sold Units → Sold %**

This prevents a large project from appearing stronger simply because it has more units. Sales conversion provides a more comparable view of commercial performance across developments with very different inventories.

### 3. Collection Is Separated From Invoicing

The financial model distinguishes:

**Invoiced Amount → Collected Amount → Outstanding Balance**

This creates a clearer view of realized cash collection versus contractual/invoiced exposure and allows management to identify the gap between what has been invoiced and what has actually been collected.

### 4. Bank and Cash Are Treated as Separate Financial Channels

The report explicitly segments financial performance by:

- **Bank**
- **Cash**

This allows the same project to be investigated from two different collection structures and supports bank-level analysis without losing the overall project context.

### 5. Bank-Wise Analysis Adds Financing Visibility

The bank-wise view breaks financed activity down by individual institutions and exposes:

- Sales/customer records
- Unit value
- Invoiced amount
- Collected amount
- Outstanding balance

This turns bank information from a simple attribute into an analytical dimension for financial monitoring.

---

# Dashboard Experience

The report is organized as a management journey rather than a collection of disconnected pages.

## 1. Global Overview

The global pages provide the portfolio-level view of units, sales, invoicing, collections, and outstanding exposure.

## 2. Time-Based Performance

The summary-by-date page introduces the temporal dimension and helps identify changes in sales and collection activity over the reporting period.

## 3. Project Intelligence

Project-level pages drill from the portfolio into the economics of an individual development, including sales conversion, project completion, invoicing, collection, and outstanding balances.

## 4. Installment Intelligence

The installment pages analyze the payment-plan structure and distinguish between alternative installment configurations.

## 5. Bank & Cash Intelligence

The bank and cash pages isolate the two primary collection channels and expose their different financial profiles.

## 6. Bank-Wise Intelligence

The bank-wise page moves one level deeper and analyzes financed activity across individual banks.

---

# Dashboard Screenshots

## Landing

![Landing Page](./Dashboard%20Previews/Landing%20Page.png)

---

## 1. Global Summary

![Global Summary 1](./Dashboard%20Previews/1-%20Global%20Summary%20Page.png)

---

## 2. Global Summary

![Global Summary 2](./Dashboard%20Previews/2-%20Global%20Summary%20Page.png)

---

## Summary by Date

![Summary By Date](./Dashboard%20Previews/Summary%20By%20Date%20Page.png)

---

## Project Summary

![Project Summary](./Dashboard%20Previews/Project%20Summary.png)

---

## Project Installments

![Project Installments](./Dashboard%20Previews/Project%20Installments.png)

---

## Project Installments — First Option

![Project Installments First Option](./Dashboard%20Previews/Project%20Installments%20First%20Option%20.png)

---

## Project Installments — Second Option

![Project Installments Second Option](./Dashboard%20Previews/Project%20Installment%20Second%20Option.png)

---

## Project Summary by Bank

![Project Summary By Bank](./Dashboard%20Previews/Project%20Summary%20By%20Bank.png)

---

## Project Installments by Bank

![Project Installments By Bank](./Dashboard%20Previews/Project%20Installments%20By%20Bank.png)

---

## Project Summary by Cash

![Project Summary By Cash](./Dashboard%20Previews/Project%20Summary%20By%20Cash.png)

---

## Project Installments by Cash

![Project Installments By Cash](./Dashboard%20Previews/Project%20Installments%20By%20Cash.png)

---

## Project Summary — Bank Wise

![Project Summary By Bank Wise](./Dashboard%20Previews/Project%20Summary%20By%20Bank%20Wise.png)

---

## Data Model — Galaxy Schema

![Galaxy Schema](./Dashboard%20Previews/Model.png)

The model follows a **Galaxy Schema** because the solution contains multiple fact tables sharing common dimensions.

### Fact Tables

- **fact_sales** — unit/customer sales transactions and commercial values
- **fact_installments** — installment-level financial transactions and payment status

### Dimension Tables

- **dim_project** — project attributes
- **dim_unit** — unit-level attributes
- **dim_customer** — customer information
- **dim_bank** — bank and Bank/Cash classification
- **dim_payment_plan** — installment-plan structure
- **dim_date** — reporting calendar and time intelligence

### Model Concept

```text
                         dim_project
                              │
                              │
dim_customer ──────── fact_sales ──────── dim_unit
                              │
                              │
                           shared
                          dimensions
                              │
                    fact_installments
                       │          │
                dim_payment_plan  dim_date
                       │
                    dim_bank
```

The shared-dimension approach allows sales and installment facts to be analyzed consistently across project, customer, unit, date, payment-plan, and bank dimensions.

---

# Data Architecture

The analytical model separates **descriptive dimensions** from **transactional facts**.

| Layer | Tables | Purpose |
|---|---|---|
| Dimensions | Bank, Customer, Date, Payment Plan, Project, Unit | Business context and slicing |
| Facts | Sales, Installments | Transactional measures |
| BI Layer | Power BI / DAX | KPIs, calculations, segmentation and reporting |

This architecture supports reusable measures instead of embedding business logic directly into individual visuals.

---

# Core KPIs

The report is centered around a consistent KPI framework:

- **Total Units**
- **Units Sold**
- **Sold %**
- **Invoiced Amount**
- **Amount Collected**
- **Outstanding Balance**
- **Bank Outstanding**
- **Cash Outstanding**
- **Issued Invoices**
- **Collected Invoices**
- **Outstanding Invoices**
- **Collection Rate**
- **Project Completion**
- **Unit Price**

These measures are reused throughout the global, project, installment, bank, cash, and bank-wise views.

---

# Analytical Workflow

```text
Raw Real Estate Data
        ↓
Data Preparation
        ↓
Dimensional Modeling
        ↓
Sales + Installment Facts
        ↓
DAX Measures
        ↓
Portfolio KPIs
        ↓
Project Analysis
        ↓
Bank / Cash Segmentation
        ↓
Bank-Wise Financial Analysis
        ↓
Management Insights
```

---

# Key Analytical Challenges

### Multi-Fact Analysis

Sales and installment transactions represent different business processes. Keeping them as separate fact tables avoids mixing incompatible transaction grains.

### Financial Reconciliation

Invoiced, collected, and outstanding amounts must be treated as separate concepts. The dashboard therefore exposes each metric explicitly instead of presenting a single financial total.

### Project Comparability

Projects vary substantially in inventory size. Using **Sold %** alongside absolute sold units provides a more meaningful comparison.

### Payment-Plan Complexity

Multiple installment options require the model to preserve payment-plan structure while still allowing portfolio-level aggregation.

### Bank / Cash Segmentation

Bank-financed and cash transactions require separate analytical treatment while remaining connected to the same project and customer context.

---

# Technology Stack

| Technology | Role |
|---|---|
| **Power BI** | Data modeling, interactive reporting and visualization |
| **Power Query** | Data preparation and transformation |
| **DAX** | Business logic, KPIs and analytical measures |
| **Excel** | Source datasets |
| **Galaxy Schema** | Multi-fact dimensional modeling |

---

# Repository Structure

```text
NOR-Dashboarb/
│
├── Assets/
│   ├── Project images
│   ├── Bank logos
│   └── Dashboard visual assets
│
├── Data/
│   ├── dim_bank.xlsx
│   ├── dim_customer.xlsx
│   ├── dim_date.xlsx
│   ├── dim_payment_plan.xlsx
│   ├── dim_project.xlsx
│   ├── dim_unit.xlsx
│   ├── fact_installments.xlsx
│   └── fact_sales.xlsx
│
├── Screenshots/
│   ├── Landing Page.png
│   ├── 1- Global Summary Page.png
│   ├── 2- Global Summary Page.png
│   ├── Summary By Date Page.png
│   ├── Project Summary.png
│   ├── Project Installments.png
│   ├── Project Installments First Option .png
│   ├── Project Installment Second Option.png
│   ├── Project Summary By Bank.png
│   ├── Project Installments By Bank.png
│   ├── Project Summary By Cash.png
│   ├── Project Installments By Cash.png
│   ├── Project Summary By Bank Wise.png
│   └── Model.png
│
├── NOR Development.pbix
├── LICENSE
└── README.md
```

---

# Project Value

NŌR Developments is structured as a **real estate financial intelligence solution**, not simply a visual reporting exercise.

The project demonstrates the ability to:

- Model multiple transactional processes in a **Galaxy Schema**
- Build reusable **DAX measures**
- Separate sales performance from collection performance
- Analyze project-level commercial performance
- Track invoiced versus collected value
- Quantify outstanding financial exposure
- Segment Bank versus Cash activity
- Drill into individual bank performance
- Connect operational sales data with financial installment data
- Present complex real estate information through a structured executive reporting experience

---

## Author

**Kerelos Nakhla Saad**  
Data Analyst | BI Developer

**Core Skills:** Power BI • DAX • Power Query • SQL • Python • Excel • Data Modeling • Business Intelligence

---

<p align="center">
  <strong>NŌR Developments — From Real Estate Transactions to Financial Intelligence.</strong>
</p>
