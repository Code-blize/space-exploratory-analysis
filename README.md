# space-exploratory-analysis
Data cleaning, EDA, DAX, and Power BI storytelling for the Maven Return To Space Challenge


The Golden Era of Space
Maven Analytics – Return to Space Challenge

This repository contains my full workflow and final dashboard submission for the Maven Return to Space Challenge, where I analyzed 4,600+ space missions (1957–2020) to uncover the decade that truly defined human space exploration — The Golden Era.

This project represents my first full storytelling dashboard built in Power BI, supported by Python for data cleaning and EDA.


Project Summary

Using mission data from various global space agencies, I explored:

Which decade had the highest mission success rate

Which era had the most launches

Which organizations were the most active

How mission outcomes evolved over time

The analysis revealed that the 1970s stood out as the Golden Era of Space Exploration — a decade marked by high activity, major technological milestones, and an exceptional success rate.


| Stage          | Tools                        |
| -------------- | ---------------------------- |
| Data Cleaning  | Python (Pandas, NumPy)       |
| EDA            | Python (Matplotlib, Seaborn) |
| Data Modelling | Power BI, Power Query        |
| Calculations   | DAX                          |
| Visualization  | Power BI                     |
| Documentation  | GitHub                       |

Repository Structure

maven-golden-era-space
 ┣ python
 ┃ ┗ README.md
 ┣ dax
 ┃ ┗ measures.dax
 ┣  dashboard
 ┃ ┗ Golden_Era.pbix
 ┣  data
 ┃ ┗ cleaned_space_missions.csv
 ┣  images
 ┃ ┗ dashboard_preview.png
 ┗ README.md

 Key Steps in the Project
 Data Extraction

Downloaded the official Maven dataset containing:

4,630 rows

9 original fields (Company, Date, Rocket, Mission, Status, etc.)

 Data Cleaning (Python)

Performed cleanup to prepare the data for BI modeling:

Converted date and time columns

Extracted Year and Decade features

Standardized MissionStatus values

Removed or marked missing data

Cleaned text inconsistencies

Exported the cleaned dataset to CSV

 Exploratory Data Analysis (EDA)

Explored trends such as:

Mission counts per decade

Success vs failure distribution

Most active companies and rockets

This guided the visual and narrative structure of the Power BI dashboard.

 Data Modeling & DAX Measures (Power BI)

Created essential metrics, including:

 Total Missions
Total Missions = COUNTROWS(cleaned_space_missions)

 Successful Missions
Successful Missions =
CALCULATE(
    COUNTROWS(cleaned_space_missions),
    cleaned_space_missions[MissionStatus] = "Success"
)

 Success Rate
Success Rate =
DIVIDE(
    [Successful Missions],
    [Total Missions],
    0
)

 Missions by Decade

Created a Decade column in Power Query using Year // 10 * 10.

Dashboard Design & Storytelling

Designed a full-page space-themed dashboard including:

KPI cards (Total Missions, Success Rate, Golden Decade)

Line Chart (Success trends across decades)

Bubble Chart (Launches vs Success rate per decade)

Top Space Agencies bar chart

Insight text boxes to explain findings

My goal was to focus on clarity, visual hierarchy, and storytelling — not just charts.

 Final Insight

The 1970s were the Golden Era of Space Exploration.
They displayed high mission volume, exceptional success rates, and major global advancements in space programs.

Dashboard Preview

<img width="1592" height="1905" alt="image" src="https://github.com/user-attachments/assets/37418e8f-c9b1-43d7-bfb5-e25dd30a79f6" />


Learning Experience

This was my first time using Power BI, and it taught me:

How to turn raw data into insight

How EDA guides visualization

How DAX powers dynamic storytelling

How design choices shape the narrative

I’m excited to keep growing as a data analyst and build more impactful projects.

Acknowledgements

Thank you to Maven Analytics for the challenge and to the data community for the continuous inspiration.
