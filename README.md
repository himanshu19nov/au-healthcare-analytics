# Australia Healthcare Analytics Portfolio Project

An end-to-end data analytics portfolio project built on AIHW (Australian Institute of Health and Welfare) national data, delivering a unified view of Australia's public hospital system across three critical domains: Emergency Department performance, Elective Surgery waitlists, and Health Expenditure.

## Project Overview
Australia's public hospital system is under sustained and growing pressure. This project builds a centralised analytics platform that transforms complex, multi-sheet AIHW Excel releases into a clean, structured reporting layer — enabling performance monitoring, state-level comparisons, and trend analysis across 11 years of national data.
The platform covers three independent but interconnected reporting areas, each with its own data pipeline, star schema model, and Power BI report


## Business Problem
Three systemic challenges motivated this project:
1. Emergency Department Overload
ED presentations are growing every year, with median wait times increasing from 121 minutes in FY20/21 to 138 minutes in FY24/25. The 4-hour benchmark — a key national target — has declined every year and now sits at 41.6%, well below the 75% target. There was no unified view identifying which states, triage categories, or hospital peer groups are failing to meet clinical targets.
2. Elective Surgery Backlogs
Elective surgery volumes collapsed during COVID-19 and have since recovered — but wait time inequality persists. The median patient waits 46 days, while the longest-waiting 10% wait nearly a full year (321 days). No consolidated view existed to compare state performance or identify which specialties are the primary bottlenecks.
3. Health Expenditure Transparency
With health spending rising year-on-year, there is a need to understand where money is going — by state, by funding source, and by expenditure area — and whether increased spending translates to improved outcomes

## Report Structure

Each Power BI report follows the same 3-page structure:

| Page | Purpose |
|------|---------|
| Overview | National-level KPIs, trends, and breakdowns |
| State Detail | Drill-through from any state visual — state vs national comparison |
| Key Findings | Executive summary with insights and conclusion |


## Key Findings
### Emergency Department

- ED demand has grown every year since FY22/23, reaching 9.1M presentations in FY24/25 — the highest on record
- Wait times peaked in FY22/23 and have not recovered to pre-pandemic levels, with % seen on time stagnating at ~59%
- Urgent (Category 3) patients are the most underserved — only ~48% are seen within the 30-minute target nationally
- The 4-hour benchmark has fallen every year from 51% in FY20/21 to 41.6% in FY24/25 — at the current rate, fewer than 40% of patients will be processed within 4 hours by FY26/27
- NSW consistently outperforms the national average on ED metrics, while smaller states show higher volatility

Overview
<img width="1306" height="731" alt="image" src="https://github.com/user-attachments/assets/f8a67b8a-e36d-47c4-a2eb-f613aa016f8b" />

State Detail
<img width="1307" height="732" alt="image" src="https://github.com/user-attachments/assets/dc8e1515-1959-4b0e-87b4-b60de141df00" />

Key Findings
<img width="1304" height="696" alt="image" src="https://github.com/user-attachments/assets/837c1df3-9197-4211-b68c-24478cecd7f7" />




### Elective Surgery

- Admissions dropped sharply in FY21/22 due to COVID-19, with a strong V-shaped recovery through FY24/25
- While volumes have recovered, wait time inequality remains — the gap between the median patient (46 days) and the longest-waiting 10% (321 days) signals a system under sustained backlog pressure
- Orthopaedic surgery has the slowest post-COVID recovery, remaining below pre-pandemic volumes through FY24/25
- NSW underperforms on elective surgery — median wait of 65 days vs national average of 46 days
- Elective surgery in Australia is recovering in quantity but not yet in equity — more patients are being treated, but the hardest cases are still waiting the longest

Overview
<img width="1291" height="723" alt="image" src="https://github.com/user-attachments/assets/00eb8d50-2797-4183-b001-398a2a37090c" />

State Detail
<img width="1307" height="720" alt="image" src="https://github.com/user-attachments/assets/0ec42fb9-46d3-47a2-a088-821ffd9389a1" />

Key Findings
<img width="1305" height="729" alt="image" src="https://github.com/user-attachments/assets/16500e3c-f4b8-41a1-bc1c-97c51759953f" />


## Data Sources

| Domain | Source | Scope |
|--------|--------|-------|
| Emergency Department | AIHW Tables 2.2–6.3 | Wait times, triage, demographics, peer groups |
| Elective Surgery | AIHW Tables 2.1–4.10 | Waitlists, admissions, specialties, urgency |
| Health Expenditure | AIHW Tables 3–B24 | Spending by state, area, and funding source |

Data period: FY2013/14 – FY2024/25

Source: [Australian Institute of Health and Welfare (AIHW)](https://www.aihw.gov.au/reports-data/myhospitals/sectors)



## Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.11+ | Data extraction, cleaning, transformation |
| Pandas | Data manipulation and aggregation |
| Openpyxl | Multi-sheet Excel parsing |
| Jupyter Notebooks | EDA and pipeline development |
| Power BI Desktop | Data modelling, DAX measures, visualisation |
| Star Schema | Dimensional modelling methodology |
