# Australia Healthcare Analytics Portfolio Project

An end-to-end data analytics solution focused on Australia's public hospital system efficiency, using AIHW (Australian Institute of Health and Welfare) data for 2024–25.

## Project Overview
This project addresses critical performance metrics in the Australian healthcare system, specifically focusing on Emergency Department (ED) wait times, Elective Surgery backlogs, and Health Expenditure trends.

## Data Architecture
The project follows a **Medallion Architecture** to ensure data integrity and traceability:
- **Raw:** Filtered AIHW master files (Excel).
- **Processed:** Cleaned and standardized CSVs.
- **Modelled:** Final Star Schema with Fact and Dimension tables optimized for Power BI.

## Key Features
- **Data Pipeline:** Python-based extraction and cleaning of complex multi-sheet AIHW datasets.
- **Data Model:** Structured Star Schema including dimensions for States, Years, Triage Categories, and Peer Groups.
- **Power BI Dashboard:** (In Progress) System performance monitoring and cost efficiency analysis.

## Tech Stack
- **Python 3.11+** (pandas, openpyxl)
- **Power BI** (Data Modeling & DAX)
- **Jupyter Notebooks** (EDA & Pipeline Development)
