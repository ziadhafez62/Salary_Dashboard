# 📊 Excel Salary Dashboard

![Salary Dashboard](0_Resources/Images/1_Salary_Dashboard_Final_Dashboard.gif)

## Introduction

This Data Jobs Salary Dashboard was created to help job seekers investigate salaries for their desired jobs and understand whether they are being adequately compensated.

The data contains detailed information about job titles, salaries, locations, and essential skills. This project demonstrates how Excel can be used to analyze data and create an interactive salary dashboard.

## 📁 Dashboard File

You can view and download the complete Excel dashboard from Google Drive:

👉 **[View / Download Excel Dashboard](https://docs.google.com/spreadsheets/d/1V16DR_6uWwMECygaPgSSPARN7yDzhuVo/edit?usp=sharing&ouid=108000511246099293518&rtpof=true&sd=true)**

## 🛠️ Excel Skills Used

The following Excel skills were utilized to build this dashboard:

- 📉 **Charts**
- 🧮 **Formulas and Functions**
- ❎ **Data Validation**
- 📊 **Data Analysis**
- 🔎 **Filtering and Sorting**

## 📊 Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023.

It includes detailed information about:

- 👨‍💼 **Job Titles**
- 💰 **Salaries**
- 📍 **Locations**
- 🛠️ **Skills**
- ⏰ **Job Schedule Types**

---

# 📈 Dashboard Build

## 📉 Charts

### 📊 Data Science Job Salaries - Bar Chart

<img src="0_Resources/Images/1_Salary_Dashboard_Chart1.png" width="850" height="550" alt="Salary Dashboard Chart">

- 🛠️ **Excel Features:** Utilized Excel's bar chart functionality with formatted salary values.
- 🎨 **Design Choice:** Used a horizontal bar chart for easy comparison of median salaries.
- 📊 **Data Organization:** Job titles were sorted by descending salary.
- 💡 **Insights:** The chart makes it easy to identify salary trends and compare different job roles.

### 🗺️ Country Median Salaries - Map Chart

![Country Median Salaries](0_Resources/Images/1_Salary_Dashboard_Country_Map.gif)

- 🛠️ **Excel Features:** Utilized Excel's Map Chart feature.
- 🎨 **Design Choice:** Used a color-coded map to differentiate salary levels across countries.
- 📊 **Data Representation:** Displays the median salary for each country with available data.
- 👁️ **Visual Enhancement:** Provides a quick visual understanding of geographic salary differences.
- 💡 **Insights:** Highlights countries with relatively higher and lower median salaries.

---

# 🧮 Formulas and Functions

## 💰 Median Salary by Job Title

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
