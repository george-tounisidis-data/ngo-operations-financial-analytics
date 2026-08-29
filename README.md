# 📊 NGO Operations Financial Analytics - Power BI & SQL Portfolio Project

## 📌 Project Overview

This project delivers a comprehensive **Business Intelligence and Financial Analytics solution** tailored for a real-world Non-Governmental Organization (NGO). The primary goal is to provide the executive board with full cost transparency, strategic insights into monthly expenditures, payroll distribution, and operational resource efficiency across multiple regional branches.

🔒 **Data Security Note (GDPR Compliance):** To protect Personally Identifiable Information (PII) and the internal structure of the organization, all sensitive attributes (employee names, specific project titles, and office locations) have been fully anonymized "on-the-fly" at the database level (SQL Server) using dynamic masking techniques. All financial metrics and numeric relationships remain 100% intact to preserve data integrity and chart accuracy.

📊 Dashboard Preview

<img width="1347" height="2627" alt="NGO Financial Analytics   Operational Cost Optimization dashboard" src="https://github.com/user-attachments/assets/e26f0613-1f34-4cee-a861-9876abbf9afb" />




## 🛠 Tech Stack & Skills Demonstrated

- **Database Engine:** Microsoft SQL Server (T-SQL)
- **Data Warehousing & Transforms:** SQL Views, Common Table Expressions (CTEs), Window Functions
- **Business Intelligence & Visualization:** Power BI Desktop & Power Query
- **Data Modeling & Analytics:** DAX Measures, Advanced Filtering, Cross-Filtering, Workforce Cost Optimization

## 🧹 Data Transformation & Challenges (The "Pro" Analyst Approach)

Real-world data is rarely clean or ready for reporting. During the ETL (Extract, Transform, Load) phase, core transformations and business logic were pushed down to the source database level (**Pushdown Logic**) using **SQL Server Views** to optimize Power BI performance:

1. **Dynamic Data Masking (GDPR):** Utilized `DENSE_RANK() OVER (ORDER BY ...)` to automatically assign sequential, unique pseudonyms to projects and employees (e.g., *Έργο 1*, *Εργαζόμενος 27*). This ensures data protection while enabling accurate aggregation of historical data across different periods.
2. **Advanced Cost Allocation Logic:** Addressed the challenge of shared corporate expenses (e.g., centralized telecommunication bills like *Voiceland*). Implemented a SQL-driven allocation script that splits shared costs equally (`SUM([Amount]) / 4.0`) across the 4 physical branches dynamically every month.
3. **Data Quality & Incomplete Records:** Filtered out overhead vendor records during payroll isolation to strictly isolate direct personnel costs, maintaining an uncorrupted dataset for workforce analytics.

## 📈 Key Business Insights & Data Storytelling

- **The Pareto Principle in Action:** A single major project drives over **53% of the total human resource budget**, with the top two projects combined accounting for more than **78% of overall payroll costs**. This highlights a heavy strategic dependency and resource concentration for the NGO's leadership.
- **Overhead Cost Drivers:** Advanced operational tracking revealed that **Rent and Lease costs command a staggering 63.96%** of total fixed expenditures, identifying physical real estate as the primary target for potential cost-reduction strategies.
- **Branch Efficiency Analysis:** **Office 3 (Γραφείο 3)** emerged as the most expensive operational center, allowing management to evaluate branch utility vs. local output.
- **Real-World Data Lag (Data Quality Audit):** Time-series visualizations successfully exposed an operational logging delay. Personnel data extends to **Month 6 (June)**, while operational expenses halt at **Month 5 (May)** due to pending accounting closures, showcasing the dashboard's ability to act as an internal data audit tool.

## 📂 Repository Structure

- `ΜΚΟ.sql`: Optimized T-SQL script containing database setup, advanced data masking, and cost allocation queries.
- `README.md`: Project documentation and business insight overview.






