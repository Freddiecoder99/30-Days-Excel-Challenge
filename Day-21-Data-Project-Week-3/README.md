<img width="814" height="502" alt="image" src="https://github.com/user-attachments/assets/4f77e1c8-b937-4ad9-b4ba-3f69649c7025" />
<img width="715" height="224" alt="image" src="https://github.com/user-attachments/assets/15ecbd20-1a97-45d9-99a4-1a08ceaee4c9" />

# Day 21: Data Project — Week 3

## Overview

Day 21 is the **third weekly data project** in the 30-Day Excel Challenge.

This project uses a **nonprofit environmental campaign dataset**. The goal is to explore the data, check its quality, clean it, answer business questions, and build an Excel dashboard.

The project combines skills learned so far, including:

* Data cleaning
* Data quality checks
* XLOOKUP
* Helper columns
* Pivot Tables
* Scorecards
* Charts
* Dashboard design

---

## Project Brief

The nonprofit wants to understand how its environmental campaigns are performing and how volunteers are participating.

The analysis should help answer important questions about:

* Volunteer participation
* Campaign impact
* Overall sentiment
* Volunteer attendance
* Data quality

---

## Planning — What They Want to Know

The project needs to answer five main questions:

1. **Which areas have the highest number of volunteers?**
2. **Which campaigns generated the most impact?**
3. **What is the overall sentiment towards their cause?**
4. **How many volunteers fail to show up?**
5. **How many missing values and duplicates were found in the source datasets?**

These questions guide the analysis and dashboard design.

---

## What I Learned

### 1. Exploring the Data

Before building the dashboard, I first explore the available datasets.

I look at:

* Columns
* Data types
* Records
* Relationships between datasets
* Potential data-quality issues

The purpose is to understand the data before making calculations or visualizations.

---

### 2. Data Quality Checks

The project checks for two important data-quality problems:

* Duplicate keys
* Missing values

This helps determine whether the source data can be trusted before analysis.

A **data quality summary** is then created to document the problems found.

---

### 3. Using XLOOKUP

XLOOKUP is used to pull campaign names from another sheet.

The general structure is:

```excel id="4m0d2k"
=XLOOKUP(lookup_value,lookup_array,return_array)
```

This connects information across the project datasets.

---

### 4. Planning the Dashboard

Before creating charts, the dashboard is planned around the questions the organization wants answered.

The dashboard should make important information easy to understand at a glance.

The project uses:

* Scorecards
* Pivot Tables
* Charts
* Supporting information

---

### 5. Cleaning the Data

The project includes cleaning the source data before creating the final dashboard.

This includes:

* Removing duplicates
* Creating helper columns
* Preparing the data for analysis

Helper columns allow additional calculations or classifications to be created without changing the original source information.

---

### 6. Building Scorecards

Pivot Tables are used to create summary information for the dashboard.

These summaries can then be presented as **scorecards** showing important project metrics.

Scorecards provide quick answers to key questions without requiring the user to examine the entire dataset.

---

### 7. Building Charts

The dashboard includes visualizations for:

* Sentiment
* Volunteer distribution

These charts make patterns easier to understand than looking at raw data alone.

---

## Project Workflow

```text
Explore the data
       ↓
Check data quality
       ↓
Create data quality summary
       ↓
Use XLOOKUP to connect information
       ↓
Plan dashboard
       ↓
Clean the data
       ↓
Create helper columns
       ↓
Build Pivot Tables
       ↓
Create scorecards
       ↓
Build charts
       ↓
Format final dashboard
```

---

## Why This Matters for Data Analysis

This project brings together many of the skills learned during the challenge.

It demonstrates that data analysis is not just about creating charts.

A complete analysis involves:

**Understanding → Checking → Cleaning → Transforming → Analyzing → Visualizing**

The quality checks are particularly important because the dashboard should be based on reliable data.

---

## Skills Practiced

* Data exploration
* Data quality checking
* Duplicate detection
* Missing-value analysis
* XLOOKUP
* Data cleaning
* Helper columns
* Pivot Tables
* Scorecards
* Chart creation
* Dashboard planning
* Dashboard formatting

---

## Key Takeaways

* Started the project by understanding the data and the questions being asked.
* Data quality should be checked before analysis.
* XLOOKUP can connect information across worksheets.
* Helper columns can support additional analysis.
* Pivot Tables can be used to create dashboard metrics.
* Scorecards provide quick summaries of important KPIs.
* Charts help communicate patterns and distributions.
* A good dashboard should be designed around the questions the audience needs answered.

---

## Reflection

This project helped me combine the Excel skills I have learned so far into a complete data-analysis workflow.

Instead of practicing one Excel function at a time, I worked through a real-world-style problem by exploring the data, checking its quality, cleaning it, analyzing it, and presenting the results in a dashboard.

---

## Project Deliverable

The final project contains:

* Cleaned source data
* Data quality checks
* Data quality summary
* XLOOKUP-based information
* Helper columns
* Pivot Tables
* Dashboard scorecards
* Sentiment chart
* Volunteer distribution chart
* Final formatted dashboard

---

## Files

```text id="2f1r8d"
Day-21-Data-Project-Week-3/
├── README.md
└── day-21-project.xlsx
```

Learning Resource

30 Day Excel Challenge by SDW Online.

This is the third weekly project in the 30-Day Excel Challenge and demonstrates the application of the skills learned during Days 15–20.
