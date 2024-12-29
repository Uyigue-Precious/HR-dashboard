## HR-dashboard
### Project Overview
This project aims to analyze and visualize the various factors that a recruitment company considers when hiring employees. By providing insights into the performance of these factors over the years, the project seeks to identify trends and offer data-driven recommendations to enhance the recruitment process.

### Data Sources
HR Data: The Dataset used for this analysis is a "HRdata.cvs" cleaned file  from a youtube video, containing detailed information about various factors in recuitment process of a company.

### TOOLS

- PowerBI - Creating report
- Power Query - Analysing the data

  ### DAta Cleaning/Preparation
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

### Result/ Findings
The analysis result are summarized as follow:
The recuitment company have been recuiting over the years acrosss various department, with noticable demand for production officer, both  production technician1 and technician2 respectively.
Indeed then linked are  the heightest recuitment source.

### Recomendation
Based on the analysis, we recommend the following action:
Production technician is a l



