# Multi-Outlet Daily Sales & Reconciliation MIS Tracker

An automated, industry-grade financial MIS reporting and revenue assurance tracker built for **Flying Sparrow Hospitality Pvt. Ltd.** to monitor multi-unit restaurant operations, detect cash leakage, and audit daily shift settlements across 5 prime locations in Delhi-NCR.

---

## 📌 Project Overview
Operating multiple high-velocity F&B units introduces significant operational friction in cash management, card/UPI transactions, and food aggregator payouts (Zomato/Swiggy). This project implements an end-to-end, formula-driven Excel system designed to:
- Standardize **Daily Sales Reporting (DSR)** across 1,525 operational shifts (Nov 2025 – Sep 2026).
- Audit **₹21.76 Crore** in net billed revenue and **2.51 Lakh+ guest covers**.
- Automatically isolate settlement discrepancies (cash shortages vs. POS bill variances) into a dynamic audit exception register.

---

## 🏢 Business Network Architecture
The tracker consolidates operations across 5 casual dining units:
- **DEL-01:** Connaught Place (CP), New Delhi
- **DEL-02:** DLF Cyber Hub, Gurugram
- **DEL-03:** Select CityWalk, Saket
- **DEL-04:** Sector 18, Noida
- **DEL-05:** Worldmark Aerocity, New Delhi

---

## 📊 Workbook Architecture

| Sheet Name | Purpose & Contents | Primary Excel Features Used |
| :--- | :--- | :--- |
| **`Executive MIS Dashboard`** | C-suite high-level KPI cards, EBITDA performance, and outlet financial summary. | Dynamic references, KPI metric cards, Executive audit notes |
| **`Outlet_Performance_Summary`** | Unit-wise matrix tracking Covers, Food/Bev split, Opex, EBITDA Margins (58.5% avg), and Food Cost %. | `SUMIF`, `SUMIFS`, Margin ratios, Target variance |
| **`Audit_Discrepancy_Log`** | Automated register isolating 50 shifts with settlement variances ($\neq 0$) along with cashier shift action logs. | `FILTER`, `INDEX-AGGREGATE`, Conditional `IF` logic |
| **`DSR_Raw_Data`** | 1,525 rows of clean, standardized operational transactional data (18 parameters). | Clean table schema, Cash/Card/Aggregator reconciliation columns |

---

## 🔍 Key Findings & Audit Insights
- **Network Performance:** Flying Sparrow achieved **₹21.76 Cr** in Net Revenue with an Operating EBITDA of **₹12.72 Cr** (**58.5%** operating margin).
- **Highest Earning Outlet:** DLF Cyber Hub led revenue generation (**₹5.36 Cr**) driven by heavy corporate dining footfalls.
- **Revenue Assurance Audit:**
  - Audited 1,525 shift handovers; **1,475 shifts (96.7%) balanced perfectly ($0 variance)**.
  - Flagged **50 reconciliation discrepancies**: 42 cashier cash shortages and 8 unrecorded tips/POS cancellation variances.
  - Total cumulative variance stood at **-₹31,750** (0.015% of net revenue), comfortably within the corporate tolerance limit of ₹50,000, earning all outlets an **`Audited - Approved`** status.

---

## 🛠️ Technical Stack & Excel Functions
- **Lookup & Dynamic Retrieval:** `FILTER`, `XLOOKUP`, `INDEX-MATCH`, `AGGREGATE`
- **Aggregation & Conditional Modeling:** `SUMIFS`, `COUNTIF`, `AVERAGEIFS`
- **Auditing & Logic:** Nested `IF`, `ABS`, `ISNUMBER`
- **Data Integrity:** Table Structured Referencing, Custom Short Date Formatting, Number Scaling (INR Crores/Lakhs)
