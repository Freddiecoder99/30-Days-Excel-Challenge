<img width="944" height="490" alt="image" src="https://github.com/user-attachments/assets/35226241-e56d-4bf8-bd81-0b468a73f1dc" />
<img width="834" height="491" alt="image" src="https://github.com/user-attachments/assets/38df4d2c-8877-4f4a-89a6-af8681dde4a6" />

# Day 14: Events Attendance Data Project

## Project Overview

Day 14 is my second data project in the 30 Days Excel Challenge.

The project uses an events management dataset containing information about event attendees, their countries, sessions, arrival times, seats, food preferences, and roles.

The goal was to work through a complete data analysis workflow, starting with understanding the business requirements and raw data, checking data quality, cleaning and standardising the dataset, performing exploratory data analysis, and finally building an interactive Excel dashboard.

This project allowed me to apply many of the Excel skills I have learned so far, particularly Pivot Tables, logical functions, data cleaning, data quality checks, conditional formatting, and data visualization.

---

## Business Problem

An events management team needs a clear overview of attendance and event participation.

Before the event can be managed effectively, the team needs to know:

* How many people are attending
* Where guests are travelling from
* Which sessions are attracting the most attendees
* How many VIPs, sponsors, and speakers are attending
* Whether the underlying attendance data contains missing or duplicate records

The objective is therefore to turn the raw attendance data into a reliable and easy-to-understand report that can support event planning and decision-making.

---

## Project Objectives

The project had five main objectives:

1. Understand and explore the raw attendance data.
2. Identify missing values and duplicate records.
3. Clean and standardise the dataset.
4. Use Pivot Tables to perform exploratory data analysis.
5. Build a dashboard that answers the key business questions.

---

## Business Questions

The analysis was designed to answer five questions:

### 1. How many people are attending?

The cleaned dataset contains **450 attendees**.

The original dataset contained 550 records, but data-quality checks identified missing and duplicate records that needed to be addressed before producing the final attendance figure.

### 2. Which countries are guests travelling from?

The analysis identified guests from the following countries:

* Australia
* Brazil
* Canada
* France
* Germany
* India
* Japan
* Nigeria
* United Kingdom
* United States

The country analysis was presented using a horizontal bar chart.

### 3. Which session has the highest attendance?

The session with the highest attendance was:

**Webinar: AI Ethics**

It recorded **86 registrations** in the exploratory analysis.

The other sessions included:

* Panel: Women in Tech
* Training: Dashboard Design
* Keynote: Future of Data
* Workshop: Excel Mastery

### 4. How many VIPs, sponsors and speakers are attending?

The cleaned attendance data showed:

| Role    | Count |
| ------- | ----: |
| VIP     |    17 |
| Sponsor |    44 |
| Speaker |    16 |

The role breakdown was visualised using a donut chart.

### 5. How many missing values are in the data?

The data-quality analysis identified:

**199 blank cells**

The project also identified duplicate records so that the final analysis would not be based on unreliable or repeated records.

---

## Data Quality Assessment

Before performing the main analysis, I assessed the quality of the raw dataset.

The raw dataset contained:

**550 records**

The data-quality scan identified:

* **199 blank cells**
* **200 duplicate records**
* **350 unique records**

This demonstrated why data cleaning needs to happen before analysis.

If duplicate and incomplete records are not identified, the resulting reports and dashboards may give misleading results.

---

## Data Quality Checks

Several checks were performed.

### Missing Values

The dataset was checked for blank values across fields including:

* Name
* Email
* Country
* Session
* Arrival Time
* Seat
* Food Preference
* Role

Missing information was flagged so it could be addressed during the cleaning process.

### Duplicate Records

A temporary record key was created by combining relevant fields from each record.

This key was then used to identify records appearing more than once.

Records were classified as:

* Unique
* Duplicate

This helped identify repeated attendance records.

---

## Data Cleaning

After the initial quality assessment, the data was cleaned and standardised.

The cleaned dataset contains:

**450 records**

The cleaning process included:

* Identifying missing values
* Identifying duplicate records
* Removing or excluding duplicate records from the final dataset
* Standardising blank values
* Standardising time formatting
* Creating helper fields for analysis
* Preparing the dataset for Pivot Tables and dashboard calculations

The original raw data was preserved separately so that the cleaning process did not overwrite the source data.

---

## Workbook Structure

The workbook contains five main worksheets.

### 1. raw_events_attendance_data

This sheet contains the original attendance dataset.

It is kept separate from the cleaned data so that the original source remains available for comparison and verification.

### 2. eda_events_attendance

This sheet contains the exploratory data analysis performed using Pivot Tables.

It includes analysis of:

* Attendees by role
* Guests by country
* Session registrations

It also maps the business questions to the visualisations used in the dashboard.

### 3. data_quality_scan

This sheet contains the data-quality checks.

It was used to identify:

* Blank values
* Duplicate records
* Unique records
* Temporary record identifiers

### 4. cleaned_events_attendance_data

This sheet contains the cleaned and standardised dataset used for the final analysis.

Additional helper fields were created to support the analysis, including:

* Empty Cells Check
* Temporary Record Key
* Duplicate Checks
* VIP indicator

### 5. events_attendance_dashboard

This sheet contains the final dashboard.

It presents the main findings in a format designed for quick interpretation.

---

## Exploratory Data Analysis

Pivot Tables were used to explore the dataset before building the dashboard.

### Attendance by Role

The role analysis showed:

* 473 attendees in the raw EDA
* 16 speakers
* 44 sponsors
* 17 VIPs

The raw role counts helped provide an initial understanding of the event audience.

### Guests by Country

The country analysis showed attendance from ten countries.

The highest counts in the EDA were:

* India: 54
* Japan: 53
* Australia: 52
* Canada: 51
* Nigeria: 51

### Session Attendance

The session analysis showed:

* Workshop: Excel Mastery - 73
* Keynote: Future of Data - 74
* Training: Dashboard Design - 75
* Panel: Women in Tech - 79
* Webinar: AI Ethics - 86

The Webinar: AI Ethics session had the highest attendance.

---

## Dashboard

The final dashboard was designed around the five business questions.

### Scorecard

A scorecard was used to communicate the total number of people attending.

### Country Analysis

A horizontal bar chart was used to show where guests were travelling from.

A horizontal bar chart makes country names easier to read while allowing the attendance counts to be compared.

### Session Attendance

A horizontal bar chart was used to compare attendance across sessions.

This makes it easy to identify the most popular session.

### Role Distribution

A donut chart was used to show the distribution of:

* VIPs
* Sponsors
* Speakers

### Missing Values

A scorecard was used to highlight the number of missing values identified during the data-quality assessment.

---

## Dashboard Verification

Before completing the project, I checked the dashboard against the original business requirements.

| Business Question                                   | Answered? |
| --------------------------------------------------- | --------- |
| How many people are attending?                      | Yes       |
| Which countries are guests travelling from?         | Yes       |
| Which session has the highest attendance?           | Yes       |
| How many VIPs, sponsors and speakers are attending? | Yes       |
| How many missing values are in the data?            | Yes       |

All five questions were answered by the final dashboard.

---

## Excel Skills Applied

This project brought together many of the skills learned during the challenge.

### Data Quality

* Identifying missing values
* Identifying duplicate records
* Creating helper fields
* Checking data consistency

### Logical Functions

* IF
* OR
* ISBLANK
* COUNTIF

### Text Functions

* Combining fields to create temporary record keys
* Standardising text values

### Aggregate Functions

* COUNT
* COUNTA
* Summary calculations

### Pivot Tables

* Grouping records
* Counting records
* Comparing categories
* Exploring attendance patterns

### Data Visualization

* Scorecards
* Horizontal bar charts
* Donut charts
* Dashboard layout

### Data Cleaning

* Removing duplicate records
* Handling missing values
* Standardising values
* Preparing data for analysis

---

## Analysis Workflow

The project followed this workflow:

```text
Business Requirements
        ↓
Explore Raw Data
        ↓
Check Data Quality
        ↓
Identify Missing Values
        ↓
Identify Duplicates
        ↓
Clean and Standardise Data
        ↓
Exploratory Data Analysis
        ↓
Answer Business Questions
        ↓
Plan Dashboard
        ↓
Build Dashboard
        ↓
Verify Results
```

This workflow helped me understand that data analysis is not simply creating charts.

The quality and preparation of the data directly affect the quality of the final analysis.

---

## Key Findings

The analysis produced several useful findings:

1. The cleaned dataset contains **473 attendees**.
2. Guests travelled from **10 countries**.
3. **Webinar: AI Ethics** had the highest session attendance in the EDA, with **86 registrations**.
4. The event included **17 VIPs, 44 sponsors, 16 speakers and 473 Attendees**.
5. The raw dataset contained **199 blank cells** and **200 duplicate records**, demonstrating the importance of data-quality checks before analysis.

---

## What I Learned

This project was an important step forward from the first Excel project.

In my first project, I mainly focused on analyzing an already structured dataset.

This project introduced an additional stage:

**checking whether the data could be trusted before analyzing it.**

I learned that data analysis involves more than formulas and charts.

A strong analysis should:

1. Start with a clear business question.
2. Understand the structure of the data.
3. Check data quality.
4. Clean and standardise the data.
5. Explore the data.
6. Answer the business questions.
7. Present the results clearly.
8. Verify that the final report actually answers the original requirements.

I also learned how Pivot Tables can make exploratory analysis much faster and how dashboards can turn multiple analyses into a single report for a decision-maker.

---

## Files

```text
Day-14-Events-Attendance-Project/
│
├── README.md
└── day-14-project.xlsx
```

## Learning Resource

30 Day Excel Challenge by SDW Online.

## Project Status

Completed
