# _CD People Scoreboard Dashboard_
<img width="6000" height="4000" alt="gettyimages-2257793880" src="https://github.com/user-attachments/assets/2b6a3e5d-a51b-4865-aa5e-17d501d3b74c" />

## Overview
This project presents a **Power BI dashboard** focused on **Workforce Capacity Analysis**, offering valuable insights into headcount seat fill, regional staffing health, and talent mobility. The dashboard highlights key attributes such as active headcount, budgeted positions, seat fill variance, and grade residence time, enabling HR leadership to identify critical staffing gaps. By analyzing these metrics across various geographic clusters, management work levels, and trade channels, stakeholders can optimize recruitment strategies, streamline internal mobility, and improve retention. Additionally, the dashboard empowers decision-makers to allocate resources more efficiently by targeting the most critical and under-filled operational units.

## How to Access this Dashboard:
1. Go to the 'About' section in the repository.
2. Open the One Drive website link.
3. Download the dashboard using the download button.
4. Make sure to have the PowerBI software installed in your PC.
5. Open the downloaded file through PowerBI.

## Problem Statement
Companies seek to derive actionable insights from workforce headcount and talent data to ensure operational readiness and optimal staffing across regional divisions. There is a need to track active headcount against budgeted capacity across different units, work levels, trade channels, and geographic clusters. Understanding these seat fill patterns enables HR leadership to identify critical staffing deficits, fast-track talent mobility, optimize recruitment costs, and mitigate retention risks—ultimately driving organizational agility and performance.

## Objective
This analysis aims to extract actionable workforce insights from HR headcount data, with a focus on evaluating seatfill capacity, segmenting management tiers, and supporting automated monthly talent strategies.

The specific objectives of this analysis include:

• **Providing a structured overview of the workforce dataset, highlighting key employee attributes such as active headcount, budgeted capacity, tenure, grade residence time, and hiring sources.**

• **Segmenting employees based on management tiers (WL1ABC vs. WL1D+) and trade channels (General Trade vs. Non-GT) to evaluate leadership pipelines and operational staffing health.**

• **Analyzing relationships between employee traits, regional clusters, and career stagnation to uncover retention risks and hiring dependencies.**

• **Enabling data-driven decision-making through an interactive Power BI dashboard backed by an automated monthly data refresh pipeline.**

## Key features
The dashboard addresses the following aspects:

✨ **Work Level & Channel Categorization:**
Engineered custom conditional logic to bucket salary grades into 1ABC (junior/mid-level) and 1D+ (senior management), alongside standardizing operational units into General Trade (GT) and Non-GT segments.

✨ **Automated Backend Data Pipeline:**
Established a dynamic local folder connector (Folder.Files) in Power Query to automate monthly data refreshes, allowing new monthly Excel files dropped into the directory to update all report pages instantly upon clicking Refresh.

✨ **Data Cleaning & Consolidation:**
Combined disparate sheets (Employee Data 1 and Employee Data 2) into a unified Master Sheet, unpivoted the cross-tab target matrix into a normalized structure, and imputed missing attributes (Branch/Team, Salary Grade) to prevent data loss.

✨ **Star Schema Data Modelling:**
Architected a robust star schema data model using dedicated lookup dimension tables (Dim_Branch, Dim_WorkLevel, Calendar) linked via 1-to-Many ($1:*$) single-direction relationships to eliminate circular filter risks.

✨ **Headcount & Seat fill Capacity Visualizations:**
Visualized cluster-wise seat fill percentage using clustered column charts with $100\%$ target benchmark lines, alongside stacked bar and donut charts to analyze gender diversity and source-of-hire distribution across work levels.

✨ **Workforce Mobility & Career Stagnation Analysis:**
Analyzed employee tenure (Length of Service) and Grade Residence Time to highlight career stagnation risks (employees $>3$ years in same grade) and evaluate reliance on external recruitment agencies versus internal job postings (IJP).

✨ **KPI Summary Cards:**
Showcased key organizational metrics—including Overall Seat fill %, Active Employees, Budgeted Headcount, Seat fill Variance, and External Offers Accepted—using formatted KPI cards for at-a-glance executive review.

✨ **Centralized DAX Calculation Engine:**
Formulated explicit, reusable DAX measures using safe division (DIVIDE) and filter context overrides (CALCULATE, USERELATIONSHIP) stored in a dedicated _All Measures table.

✨ **Interactive Tile Slicers & Dynamic Filtering:**
Implemented horizontal tile slicers for regional units (North, South, East, West, Central, Non-GT) to enable real-time dynamic slicing across all charts and summary cards simultaneously.

✨ **Executive Multi-Page Architecture & Process Documentation:**
Designed a structured, multi-page dashboard separating the core Seat fill Scorecard, Workforce Mobility & Diversity Analysis, and Backend Process Documentation for seamless evaluation and storytelling.

## Dataset Reference
You can refer to the dataset used in this project from my GitHub repository: [People Scoreboard Analysis Dataset](https://github.com/rish-1412/CD_People_Scoreboard_Dashboard/blob/main/Raw_Dataset.xlsx)

## About Me
I'm passionate about data analysis and visualization, with a focus on delivering actionable insights through intuitive dashboards. Connect with me on [LinkedIn](https://www.linkedin.com/in/rishabh-jain-b6b420286/) to collaborate or discuss more projects.

## License
This project is open-source and available for educational and non-commercial purposes. Feel free to fork and modify the repository as needed.
