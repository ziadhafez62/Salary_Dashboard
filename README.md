```markdown
# Excel Salary Dashboard

## Introduction

This Data Jobs Salary Dashboard was created to help job seekers investigate salaries for their desired jobs and understand whether they are being adequately compensated.

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The dataset contains detailed information about job titles, salaries, locations, and essential skills.

## Dashboard File

My final Excel dashboard is available here:

[📊 Download Excel Dashboard](https://github.com/ziadhafez62/Salary_Dashboard/raw/refs/heads/main/1_Salary_Dashboard.xlsx)

## Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**
- **📊 Data Analysis**
- **🔎 Filtering and Sorting**

## Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023.

It includes detailed information on:

- **👨‍💼 Job Titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**
- **⏰ Job Schedule Types**

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

A horizontal bar chart was used to compare median salaries across different data-related job titles.

- **Excel Features:** Used Excel's bar chart functionality with formatted salary values.
- **Design Choice:** Horizontal bar chart for easy comparison of median salaries.
- **Data Organization:** Job titles were sorted by descending salary.
- **Insights Gained:** The chart helps identify salary trends and compare different job roles.

#### 🗺️ Country Median Salaries - Map Chart

An Excel Map Chart was used to analyze median salaries across different countries.

- **Excel Features:** Utilized Excel's Map Chart feature.
- **Design Choice:** Used geographic visualization to compare salary levels across countries.
- **Data Representation:** Displays median salary for each country with available data.
- **Insights Gained:** Helps identify geographic differences in salary levels.

## 🧮 Formulas and Functions

### 💰 Median Salary by Job Titles

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
```

- **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes zero salaries.
- **Array Formula:** Uses the `MEDIAN()` function with a nested `IF()` statement.
- **Tailored Insights:** Provides salary information based on job title, country, and schedule type.
- **Formula Purpose:** Returns the median salary based on the selected criteria.

### ⏰ Count of Job Schedule Type

```excel
=FILTER(
    J2#,
    (NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*
    (J2#<>0)
)
```

- **Unique List Generation:** Uses the `FILTER()` function to exclude entries containing `"and"` or commas.
- **Zero Values:** Removes zero values from the resulting list.
- **Formula Purpose:** Generates a clean list of job schedule types.

## ❎ Data Validation

Data Validation was implemented for the **Job Title**, **Country**, and **Type** selections.

This ensures:

- 🎯 User input is restricted to predefined values.
- 🚫 Incorrect or inconsistent entries are prevented.
- 👥 Dashboard usability is improved.
- 🔄 Users can easily interact with the dashboard filters.

## 📌 Key Features

- 💰 Salary analysis by job title
- 🌍 Salary analysis by country
- ⏰ Analysis by job schedule type
- 📊 Interactive charts
- 🧮 Excel formulas and functions
- ❎ Data validation
- 🔎 Filtering and sorting

## Conclusion

This project demonstrates how Microsoft Excel can be used to transform raw job-market data into meaningful insights through data analysis and visualization.

The dashboard allows users to explore salary trends across different job titles, countries, and job schedule types, helping them better understand the data job market and make more informed career decisions.

## 👨‍💻 Author

**Ziad Hafez**

GitHub: [ziadhafez62](https://github.com/ziadhafez62)
```
