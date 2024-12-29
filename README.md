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
- How many of the employee contract was activated or terminated per year?
- Which recuitment source do recuiters get their employee base on our dataset?

### Data Analysis

``` measures
Male = IF(ISBLANK( CALCULATE([HEAD_COUNT],HRData[Gender]="male")),0,( CALCULATE([HEAD_COUNT],HRData[Gender]="male")))
```




