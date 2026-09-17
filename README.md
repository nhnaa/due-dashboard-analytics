# 🎓 DUE Academic & Institutional Analytics Dashboard

An end-to-end Business Intelligence solution developed with **Microsoft SQL Server** and **Power BI Desktop**, designed to support strategic decision-making and operational management at the **University of Economics – The University of Danang (DUE)**.

---

## 📌 Executive Summary

* **Domain:** Higher Education Management & Institutional Research (Data period: 2020 – 2025).
* **Architecture:** Hybrid ETL Pipeline (Server-side SQL Stored Procedures + Power Query + DAX).
* **Data Model:** Mixed Snowflake Schema & Multi-Fact Architecture to prevent circular dependency and maximize query performance.
* **Core Deliverables:** 6 interactive operational and strategic dashboards built for the University Board of Rectors and functional departments.

---

## 🏛️ System Architecture & Dashboard Suites

The reporting system consolidates operations across 6 comprehensive analytical views:

1. **Student Affairs Management (CTSV):** Monitors student demographics (gender, ethnicity, nationality, residency) and enrollment statuses (active, graduated, suspended, withdrawn).
2. **Student Lifecycle Management (QLSV):** Tracks cohort enrollment trends, graduation-on-time velocity, and course repetition/retake behaviors across faculties and majors.
3. **Academic Operations Management (QLĐT 1):** Delivers macro academic KPIs including 10-point and 4-point GPA distributions, pass rates, and academic performance grading (Distinction, Merit, Average).
4. **Course & Instruction Quality Analytics (QLĐT 2):** Drill-down analysis into specific course-level metrics (Top 10 highest fail rates, lowest average scores) correlated with student survey evaluations.
5. **Faculty & Teaching Resource Allocation (ĐNGV):** Manages faculty headcount, academic ranks (Prof., Assoc. Prof.), degrees (Ph.D., Master), professional titles, and teaching quotas against Ministry regulations (200 hours/year baseline).
6. **Teaching & Learning Correlation Analysis (KQGD-HT):** Analyzes grade distributions (0.2-bin score histograms), boxplots, and regression trends between class sizes and student GPAs across individual instructors.

---

## 🛠️ Technical Stack & Data Pipeline

| Layer | Tools & Technologies | Description |
| :--- | :--- | :--- |
| **Database & ETL** | Microsoft SQL Server, T-SQL | Extracted and transformed data from 50+ relational tables using optimized Stored Procedures (`sp_Dash_SinhVien_Snapshotttt`, `DB_SP_QuanLySV`, `sp_Dash_KPI_QuanLyDaoTao`, `sp_ThongKeHocPhan`, `SP_GVSV`, `sp_Dash_DiemSinhVien_TheoGV`). |
| **BI & Analytics** | Power BI Desktop (`.pbip`), Power Query | Native execution (`EXEC SP_...`), custom DAX measures, and multi-tier interactive slicers (Cross-filtering, Drill-down). |
| **Data Modeling** | Snowflake Schema & Multi-Fact Tables | Central Fact tables (`DSSV`, `QuanLy Daotao`, `HocPhan`, `SurveyAgg`, `CLGV`) linked with Dimension tables (`S_DANH_MUC_KHOA`, `GiangVien`, `DimHocPhan`, `CTSV`). |
| **Version Control** | Git, GitHub (`.pbip` format) | Granular version tracking of semantic models and report visual definitions. |

---

## 🚀 How to Run the Project

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/nhnaa/due-dashboard-analytics.git](https://github.com/nhnaa/due-dashboard-analytics.git)
   cd due-dashboard-analytics
