## HR-dashboard

## Table of Content
- [Project Overview](#Project-Overview)
- [Data Sources](#Data-sources)
- [Tools](#Tools)
- [Data Cleaning/Preparation](#data-cleaningpreparation)
- [exploratory Data Analysis](#exploratory-Data-Analysis)
- [Data Analysis](#Data-Analysis)
- [Result and Findings](#result-and-findings)
- [Recommendations](#Recommendations)
- [References](#References)



### Project Overview
This project aims to analyze and visualize the various factors that a recruitment company considers when hiring employees. By providing insights into the performance of these factors over the years, the project seeks to identify trends and offer data-driven recommendations to enhance the recruitment process.

<img width="587" alt="image" src="https://github.com/user-attachments/assets/99ba05e0-940c-4c2a-b782-eb0e0d3a4ae8" />

### Data Sources
HR Data: The Dataset used for this analysis is a "HRdata.cvs" cleaned file  from a youtube video, containing detailed information about various factors in recuitment process of a company.

### TOOLS

- PowerBI - Creating report
- Power Query - Analysing the data

  ### Data Cleaning/Preparation
  In the intinial data preparation phase, we performed the following task:
  1. Data loaing and inspection.
  2. Cheched for missing value.
  3. No data cleaning because it came as a cleaned data

### exploratory Data Analysis

EDA involved EXploring the sales data to answer key questions, such as

- What is the employee headcount per year, and how many are male or female?
- Which job position is in high demand?
- Which recuitment source do recuiters get their employee base on our dataset?
- Which hiring positing has the heighest salary?

### Data Analysis

``` measures
Male = IF(ISBLANK( CALCULATE([HEAD_COUNT],HRData[Gender]="male")),0,( CALCULATE([HEAD_COUNT],HRData[Gender]="male")))
```

```Switch DAX function
atisfaction_Status = 
SWITCH(
    TRUE(),
    HRData[EmployeeSatisfaction] = 1, "Very Low",
    HRData[EmployeeSatisfaction] = 2, "Low",
    HRData[EmployeeSatisfaction] = 3, "Accepted",
    HRData[EmployeeSatisfaction] = 4, "High",
    HRData[EmployeeSatisfaction] = 5, "Very High"
)```

### Result and Findings
The analysis result are summarized as follow:
The recuitment company have been recuiting over the years acrosss various department, with noticable demand for production officer, both  production technician1 and technician2 respectively.
Indeed then linked are  the heightest recuitment source.

### Recommendations

Production Technician roles are in high demand and should be considered by young adults or individuals seeking a career switch.
Recruiters primarily source employees from Indeed and LinkedIn. Job seekers should optimize their profiles and actively engage on these platforms to increase visibility and opportunities.

### References

YouTube [Simple HR Power BI Dashboard by abdelytics]


