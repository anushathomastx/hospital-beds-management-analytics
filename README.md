A Power BI project analyzing hospital census, admissions/discharges, LOS, satisfaction, and service line performance.

🚀 Project Overview
This project presents a multi‑page Hospital Operations & Clinical Performance Dashboard built using Power BI Desktop, SQL, DAX, and data modeling best practices.

The dashboard provides a comprehensive view of:

Daily and monthly census trends

Rolling 7‑day census smoothing

Admissions & discharges (MTD)

Length of Stay (LOS) analysis

Patient satisfaction

Service line distribution

Operational efficiency insights

Executive‑ready narrative storytelling

I designed and developed this project with the assistance of Microsoft Copilot, using it for DAX optimization, and portfolio preparation.

🔗 Live Dashboard (Power BI Service)
https://app.powerbi.com/view?r=eyJrIjoiZjExYjM2MDktMmU4Yy00ZTRiLTkwYjgtNmVlODI0NjNhOWY0IiwidCI6IjMxZDdlMmE1LWJkZDgtNDE0ZS05ZTk3LWJlYTk5OGViZGZlMSJ9

🖼️ Dashboard Screenshots
Monthly Census
<img src="screenshots/monthly-census.png" width="600">

Rolling 7‑Day Census
<img src="screenshots/rolling-7day.png" width="600">

Admissions vs Discharges
<img src="screenshots/admissions-discharges.png" width="600">

Clinical Performance Dashboard
<img src="screenshots/clinical-dashboard.png" width="600">

🧠 Key Insights
1. Census & Throughput
Monthly census fluctuates between 20–25 patients.

Rolling 7‑day census smooths daily volatility and reveals operational rhythm.

Balanced admissions and discharges (~50/50) indicate high throughout efficiency.

2. Clinical Cost Optimization
Average LOS is 7.41 days, high for a 50‑bed facility.

Longer LOS increases variable costs (labor, supplies, food).

Reducing LOS while maintaining census improves revenue mix.

3. Service Line Performance
Emergency, Surgery, General Medicine, and ICU volumes are evenly distributed.

Satisfaction scores across all service lines remain in the high 70s to low 80s.

Strong performance suggests opportunities for strategic investment and growth.

🛠️ Tools & Technologies
Power BI Desktop

DAX (Data Analysis Expressions)

Power Query

SQL (data cleaning & preparation)

Microsoft Fabric Free 

GitHub for version control

Microsoft Copilot for:

DAX assistance

Dashboard structuring

Narrative writing

README creation

Portfolio guidance

📁 Repository Structure
Code
/screenshots
    monthly-census.png
    rolling-7day.png
    admissions-discharges.png
    clinical-dashboard.png

/powerbi-file
    hospital-operations-dashboard.pbix

/dax-measures
    rolling-7day-census.dax
    admissions-mtd.dax
    discharges-mtd.dax
    monthly-average-census.dax

/sql
    data-cleaning.sql
    data-load.sql

README.md

DAX Highlights
Rolling 7‑Day Census
DAX
Rolling 7 Day Census =
AVERAGEX(
    DATESINPERIOD(
        'aprildb hospital_daily_kpis'[day],
        MAX('aprildb hospital_daily_kpis'[day]),
        -7,
        DAY),
    CALCULATE(AVERAGE('aprildb hospital_daily_kpis'[census]))
)

Admissions (MTD)
DAX
Admissions (MTD) =
TOTALMTD(
    SUM('aprildb hospital_daily_kpis'[admissions]),
    'aprildb hospital_daily_kpis'[day]
)

🎯 What This Project Demonstrates
Healthcare analytics expertise

Operational + clinical KPI understanding

Strong Power BI design skills

Storytelling with data

DAX proficiency

Ability to build executive‑ready dashboards

Clean GitHub documentation

Effective use of AI tools (Microsoft Copilot) in analytics workflows


📬 Contact
If you'd like to connect or discuss healthcare analytics roles:

Anusha — Data Analyst & Clinical Research Scientist  
📍 Dallas, TX
💼 Healthcare Analytics | Clinical Data | Power BI | SQL
