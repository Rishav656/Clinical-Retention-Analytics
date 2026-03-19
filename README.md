# Clinical-Retention-Analytics
Simulated a hospital system using a relational dataset (Doctor, Patient, Appointment, Treatment, Billing) with ICU load, doctor shifts, and critical care scenarios. Used SQL for data cleaning, joins, and KPIs, and built an interactive dashboard in Power BI to analyze workload, ICU usage, and revenue.


Hospital Operations & Patient Experience Analysis
📌 Project Overview The "Origin Medical" project addresses a common healthcare challenge: Patient Leakage. We noticed a high volume of "one-time" patients—people who visit a specialist once but never return for a follow-up.
My goal was to determine if these patients were leaving because they were cured, or because of operational friction, specifically High Wait Times and Doctor Overload.



🛠️ Tech Stack SQL (MS SQL Server): Used for deep-dive analysis, CTEs, and calculating retention metrics.
Power BI: Created a "Budget Variance" and "Risk Matrix" to track financial and operational performance.
Data Analysis: Applied business logic to identify correlations between wait times and churn.


🔍 The Deep Dive:How I Solved It.:-
1.Identifying Patient Loyalty (SQL Logic) I built a SQL model to categorize patients based on their visit frequency. By calculating a Retention Ratio (TotalVisits/UniquePatients), I defined two groups:Satisfied (High Retention): Patients with a follow-up history (Ratio > 1.5).At Risk (Low Retention): One-time visitors who might have had a bad experience.
2.	The Wait Time Correlation I cross-referenced these loyalty groups with Average Wait Times. The data revealed a clear "Leakage Point": doctors with an average wait time exceeding 40 minutes saw a significant spike in "At Risk" patients. This proved that operational delays were directly hurting the hospital's revenue and reputation.
3.	Financial Risk & Budgeting (Power BI) I developed a Budget Variance Matrix in Power BI to monitor department-level spending. Conditional Formatting: Highlighted "Red Zones" where spending was over-budget. Diagnosis Tracking: Tied operational costs to specific medical conditions to see which areas were most resource-heavy.

💡 Key Insights The 40-Minute Threshold: Patients are willing to wait, but only up to a point. Beyond 40 minutes, the likelihood of a return visit drops by nearly 30%. Operational Stress: High-load doctors (those working at >110% capacity) have the lowest retention rates, suggesting that burnout impacts patient communication. Revenue Impact: By identifying "leakage points," the hospital can potentially reclaim lost follow-up revenue by optimizing doctor schedules.
🚀 Final Recommendation To improve patient retention, the hospital needs to implement Buffer Scheduling during peak hours and provide Communication Coaching for specialists who have high clinical success but low return rates.


