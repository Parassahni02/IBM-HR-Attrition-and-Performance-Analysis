# 🧑‍💼 HR Analytics Project — IBM Employee Attrition Analysis

![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

---

## 📌 Project Overview

An end-to-end HR Analytics project analyzing employee attrition, salary distribution, satisfaction levels, and workforce demographics using the IBM HR Analytics Dataset. The project covers the full data analytics pipeline — from raw data cleaning in Excel, to SQL-based analysis in PostgreSQL, to an interactive Power BI dashboard.

> **Goal:** Identify the key drivers of employee attrition and build actionable insights that HR teams can use to improve retention strategies.

---

## 🗂️ Project Structure

```
HR-Analytics-Project/
│
├── 📁 Excel/
│   └── IBM_HR_Analytics_New.xlsx        ← Cleaned data + 9 Pivot Tables + Dashboard
│
├── 📁 SQL/
│   └── SQL_Queries.txt                  ← 10 business analysis queries (PostgreSQL)
│
├── 📁 PowerBI/
│   └── IBM_HR_Analyticss.pbix           ← 1-page interactive dashboard
│
└── README.md
```

---

## 📊 Dataset

| Detail | Info |
|---|---|
| Source | IBM HR Analytics Dataset (Kaggle) |
| Rows | 1,470 employees |
| Columns | 35 original + 6 engineered features |
| Departments | Sales, Research & Development, Human Resources |
| Job Roles | 9 unique roles |
| Income Range | $1,009 – $19,999/month |

### 🔧 Feature Engineering
Created 6 new columns from raw data:

| New Column | Logic |
|---|---|
| `AgeGroup` | Bins: 18-25, 26-35, 36-45, 46-60 |
| `SalaryBand` | Low (≤3K), Mid (3-6K), High (6-10K), Very High (>10K) |
| `TenureBand` | 0-2 yrs, 3-5 yrs, 6-10 yrs, 10+ yrs |
| `AttritionFlag` | Yes → 1, No → 0 |
| `JobSatisfactionLabel` | 1-Low, 2-Medium, 3-High, 4-Very High |
| `WorkLifeBalanceLabel` | 1-Bad, 2-Good, 3-Better, 4-Best |

---

## 🔑 Key KPIs

| Metric | Value |
|---|---|
| 👥 Total Employees | 1,470 |
| 📉 Overall Attrition Rate | **16.12%** |
| ✅ Active Employees | 1,233 |
| ⚠️ Attrited Employees | 237 |
| 💰 Avg Monthly Income | $6,503 |
| 🎂 Avg Employee Age | 36.9 years |
| 📅 Avg Tenure | 7.0 years |
| 🚨 High Risk Employees | 97 (still active, likely to leave) |

---

## 📈 Key Insights

### 1️⃣ Attrition by Department
| Department | Total | Attrited | Attrition Rate |
|---|---|---|---|
| Sales | 446 | 92 | **20.6%** 🔴 |
| Human Resources | 63 | 12 | **19.1%** 🔴 |
| Research & Development | 961 | 133 | **13.8%** 🟡 |

> 💡 **Insight:** Sales department has the highest attrition rate at 20.6% — nearly 1 in 5 sales employees leave. HR should prioritize retention programs in Sales first.

---

### 2️⃣ Attrition by Job Role
| Job Role | Attrition Rate |
|---|---|
| Sales Representative | **39.8%** 🔴 |
| Laboratory Technician | **23.9%** 🔴 |
| Human Resources | **23.1%** 🔴 |
| Research Director | **2.5%** 🟢 |
| Manager | **4.9%** 🟢 |

> 💡 **Insight:** Sales Representatives have an alarming 39.8% attrition rate — nearly 4 in 10 leave. Senior roles (Manager, Research Director) show far lower attrition, suggesting career growth reduces turnover.

---

### 3️⃣ Overtime Drives Attrition
| Overtime | Total | Attrited | Attrition Rate |
|---|---|---|---|
| Yes | 416 | 127 | **30.5%** 🔴 |
| No | 1,054 | 110 | **10.4%** 🟢 |

> 💡 **Insight:** Employees on overtime are **3x more likely to leave** than those who aren't. This is one of the strongest single predictors of attrition in the dataset.

---

### 4️⃣ Attrition by Age Group
| Age Group | Attrition Rate |
|---|---|
| 18–25 | **35.8%** 🔴 |
| 26–35 | **19.1%** 🔴 |
| 36–45 | **9.2%** 🟢 |
| 46–60 | **12.5%** 🟡 |

> 💡 **Insight:** Young employees (18-25) have the highest attrition at 35.8%. This is likely due to fewer commitments and higher career mobility. Structured career development programs for early-career employees could significantly reduce this.

---

### 5️⃣ Attrition by Marital Status
| Marital Status | Attrition Rate |
|---|---|
| Single | **25.5%** 🔴 |
| Married | **12.5%** 🟡 |
| Divorced | **10.1%** 🟢 |

> 💡 **Insight:** Single employees are 2.5x more likely to leave than divorced employees. Single employees have fewer financial obligations and more career flexibility.

---

### 6️⃣ Job Level vs Attrition
| Job Level | Avg Salary | Attrition Rate |
|---|---|---|
| Level 1 | $2,787 | **26.3%** 🔴 |
| Level 2 | $5,502 | **9.7%** 🟢 |
| Level 3 | $9,817 | **14.7%** 🟡 |
| Level 4 | $15,504 | **4.7%** 🟢 |
| Level 5 | $19,192 | **7.3%** 🟢 |

> 💡 **Insight:** Entry-level employees (Level 1) with the lowest salaries have a 26.3% attrition rate — nearly 3x the company average. Salary improvements at Level 1 could have the highest ROI for retention.

---

### 7️⃣ Business Travel Impact
| Travel Frequency | Attrition Rate |
|---|---|
| Travel Frequently | **24.9%** 🔴 |
| Travel Rarely | **15.0%** 🟡 |
| Non-Travel | **8.0%** 🟢 |

> 💡 **Insight:** Frequent travelers are 3x more likely to quit than non-travelers. Travel fatigue is a significant but often overlooked attrition driver.

---

### 8️⃣ 🚨 High Risk Employee Profile
97 currently active employees were flagged as high risk using a custom **Weighted Risk Score Model:**

```
RiskScore = (3 - JobSatisfaction) × 3 + (3 - WorkLifeBalance) × 2 + YearsSinceLastPromotion
```

**Why these weights?**
- Job Satisfaction × 3 → strongest predictor of attrition (IBM HR research)
- Work Life Balance × 2 → second strongest predictor (Gallup research)
- Years Since Promotion × 1 → stagnation drives silent attrition

**Common profile of a high-risk employee:**
- Works overtime ✅
- Job Satisfaction ≤ 2 (Low/Medium) ✅
- Poor Work-Life Balance ✅
- Not promoted in several years ✅

---

## 🛠️ Tools & Technologies

### Phase 1 — Excel
- Data cleaning (removed 3 constant columns, fixed data types)
- Feature engineering (6 new calculated columns)
- 12 Pivot Tables across 2 analysis sheets
- KPI Dashboard with linked formulas
- Conditional formatting with traffic-light color scales

### Phase 2 — PostgreSQL
- Created `hr_analytics` database and table
- Imported cleaned CSV data
- Wrote 10 business analysis queries covering:
  - Overall attrition KPIs
  - Department & Job Role analysis
  - Overtime, salary, age, tenure analysis
  - Satisfaction vs attrition correlation
  - Performance & compensation analysis
  - Comparison profile: Who Left vs Who Stayed

### Phase 3 — Power BI
- Connected directly to Excel workbook
- Created 8 DAX measures
- Built 1-page interactive dashboard:
  - **Page 1:** Overview (KPI cards, department slicer, bar charts, donut charts)
- Applied custom dark purple theme
- Added conditional formatting on table visuals

---

## 💡 Business Recommendations

Based on the analysis, here are 5 actionable HR recommendations:

1. **🎯 Fix Overtime Policy** — Employees on overtime leave at 30.5% vs 10.4% for others. Cap mandatory overtime or compensate better.

2. **💰 Raise Entry-Level Salaries** — Job Level 1 employees leave at 26.3%. A targeted salary revision could dramatically reduce this.

3. **🚀 Create Career Growth Programs for Young Employees** — 18-25 year olds leave at 35.8%. Structured mentorship and fast-track promotion paths can retain this group.

4. **✈️ Reduce Frequent Travel Requirements** — Frequent travelers leave at 24.9%. Remote collaboration tools can reduce this burden.

5. **🚨 Immediate Intervention for 97 High-Risk Employees** — These active employees match the leaving profile. One-on-one HR check-ins, promotion reviews, or role changes could prevent 97 resignations.

---

## 📁 Files in This Repository

| File | Description |
|---|---|
| `IBM_HR_Analytics_New.xlsx` | Cleaned dataset + 9 pivot tables + KPI dashboard |
| `SQL_Queries.txt` | 10 PostgreSQL business analysis queries with comments |
| `IBM_HR_Analyticss.pbix` | Power BI 2-page interactive dashboard |
| `README.md` | Project documentation (this file) |

---

## 🖼️ Dashboard Preview

### Excel Dashboard
> *(Add screenshot of your Excel dashboard here)*

### Power BI Page 1 — Overview
> *(Add screenshot of Power BI Page 1 here)*

### Power BI Page 2 — Deep Dive
> *(Add screenshot of Power BI Page 2 here)*

---

## 👨‍💻 About This Project

This project was built as a portfolio piece demonstrating end-to-end data analytics skills across three industry-standard tools. The analysis covers the full workflow a data analyst would follow in a real HR analytics role — from raw data ingestion to executive-ready dashboards.

**Skills demonstrated:**
- Data cleaning & feature engineering
- Pivot table analysis
- SQL query writing (aggregations, filters, CASE statements, UNION)
- DAX measure creation
- Dashboard design & data visualization
- Business insight generation & storytelling

---

*Dataset: IBM HR Analytics Employee Attrition & Performance (Kaggle)*
