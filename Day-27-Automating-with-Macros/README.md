# Day 27: Automating With Macros

## Overview

Today I learned about Macros and how they can be used to automate repetitive tasks in Excel.

Macros allow a sequence of actions to be recorded and then repeated automatically.

This can save time when performing the same formatting, data quality checks, reporting, or dashboard-building tasks repeatedly.

Today I focused on recording macros, testing them on new datasets, using formulas within macros, creating dashboards automatically, making adjustments with VBA, and creating a master macro that runs multiple tasks at once.

## What I Learned

## What are Macros?

A macro is a recorded or programmed sequence of actions that can be executed automatically in Excel.

Macros are useful when the same task needs to be repeated multiple times.

For example, instead of manually performing the same formatting steps every day, a macro can perform those steps with a single click.

Macros can be used for:

- Formatting data
- Cleaning datasets
- Creating reports
- Running calculations
- Building charts
- Creating dashboards
- Automating repetitive tasks

## When to Use Macros

Macros are useful when a task:

- Is repetitive
- Follows the same sequence of steps
- Needs to be performed frequently
- Takes a significant amount of time manually
- Needs consistent formatting or output

For example, if a data quality report needs to be created every week using the same process, a macro can automate the task.

## Setting Up Excel for Macros

Before working with macros, I needed to enable the Developer tab in Excel.

The Developer tab provides tools for:

- Recording macros
- Running macros
- Editing VBA code
- Managing macro settings
- Working with form controls

## Saving as XLSM

Workbooks containing macros need to be saved using the Excel Macro-Enabled Workbook format.

The file extension is:

```text
.xlsm
```

For example:

```text
data_analysis_dashboard.xlsm
```

Saving the workbook as `.xlsm` allows the VBA and macro functionality to be preserved.

## Recording My First Macro

My first macro focused on formatting charity donations data.

The purpose was to record a series of formatting actions and then allow Excel to repeat those actions automatically.

The formatting steps included:

- Cleaning headers
- Formatting currency values
- Adding borders
- Improving the presentation of the dataset

## Recording Formatting Steps

While recording the macro, I performed the required formatting actions manually.

The macro recorded the steps so they could be repeated later.

For example:

```text
Clean headers
       ↓
Format currency
       ↓
Add borders
       ↓
Complete formatting
```

Once recorded, the same formatting process could be applied automatically.

## Data Quality Summary Report Macro

I then recorded a second macro for creating a data quality summary report.

The macro automated steps used to review and summarize data quality issues.

This showed how macros can go beyond simple formatting and automate analytical tasks.

## Testing a Macro on a New Dataset

An important part of automation is testing whether the macro works on data it has not previously been used on.

I tested the recorded macro using a new dataset.

This helped demonstrate whether the recorded steps were reusable and whether the macro could produce the expected result.

Testing is important because a macro that works on one dataset may not work correctly on another dataset if the structure or layout is different.

## Data Quality Check Macro With Formulas

I also recorded a macro that included formulas for checking data quality.

The macro could automate the process of adding data quality checks to a dataset.

For example, formulas can be used to identify:

- Missing values
- Duplicate records
- Invalid values
- Other data quality issues

Automating these checks can reduce repetitive manual work.

## Building a Dashboard With a Macro

The third major macro focused on creating a dashboard.

The dashboard included:

- A bar chart
- A pie chart
- Data quality summary information

The macro was used to automate the dashboard-building process.

This demonstrated how macros can be used to automate not only data preparation but also reporting and visualization.

## Bar Chart

The dashboard macro created a bar chart to show different data quality issue types.

A bar chart makes it easier to compare the number of issues across categories.

For example:

```text
Issue Type
Duplicate IDs
Missing Values
Invalid Values
Zero Refunds
```

The macro automated the process of creating the chart from the summary data.

## Pie Chart

The dashboard also included a pie chart.

The pie chart was used to show the distribution of the different data quality issue types.

This provided another visual way of understanding the composition of the identified issues.

## Fixing Chart Positioning With VBA

After running the dashboard macro, I learned that automatically created charts may not always appear in the correct position.

VBA can be used to control chart placement.

For example, VBA can be used to specify where a chart should be positioned on a worksheet.

This allows the automated dashboard to have a more consistent layout.

## What is VBA?

VBA stands for Visual Basic for Applications.

It is the programming language used to automate tasks in Excel and other Microsoft Office applications.

Recorded macros generate VBA code that represents the actions recorded in Excel.

VBA can also be edited manually to create more advanced automation.

## Master Macro

I then created a master macro that runs multiple macros together.

Instead of running each macro separately, the master macro can execute the entire workflow.

For example:

```text
Master Macro
     ↓
Format Data
     ↓
Run Data Quality Checks
     ↓
Create Summary
     ↓
Create Dashboard
     ↓
Position Charts
```

This creates a complete automated process.

## Why a Master Macro is Useful

A master macro is useful when several tasks need to be performed in a specific order.

It reduces the number of manual steps required to complete a workflow.

For example, a single macro can:

- Format the raw data
- Run data quality checks
- Create a summary table
- Generate charts
- Build the dashboard

This makes the overall process easier to repeat.

## Assigning Macros to Buttons

Macros can be assigned to buttons inside an Excel worksheet.

This allows users to run an automated process without opening the Macro menu.

For example:

```text
[ Run Dashboard ]
```

Clicking the button can trigger the assigned macro.

Buttons can make automated workbooks easier for other users to operate.

## One-Click Dashboard

The final demonstration showed how the different automation steps could be combined into a one-click dashboard process.

The user can click a button and allow the workbook to:

```text
Format Data
      ↓
Check Data Quality
      ↓
Create Summary
      ↓
Build Charts
      ↓
Update Dashboard
```

This demonstrated how Excel can be turned into a more automated reporting tool.

## Why This Matters for Data Analysis

Data analysts often perform repetitive tasks when preparing data and producing reports.

Automating these tasks can help:

- Reduce repetitive manual work
- Improve consistency
- Save time
- Reduce human error
- Standardize reporting processes
- Make recurring analysis easier

Macros are especially useful when the same process needs to be repeated regularly.

## Automation Workflow

Today's exercise demonstrated a complete reporting workflow:

```text
Raw Data
   ↓
Formatting
   ↓
Data Quality Checks
   ↓
Summary Table
   ↓
Bar Chart
   ↓
Pie Chart
   ↓
Dashboard
```

The workflow was then combined into a master macro.

## Business Exercise: Charity Donations

In the first exercise, I recorded a macro to format charity donations data.

The macro automated:

- Header formatting
- Currency formatting
- Borders
- General presentation

This showed how repetitive formatting tasks can be automated.

## Business Exercise: Data Quality Report

In the second exercise, I created a macro for a data quality summary report.

The macro automated the steps required to check and summarize data quality issues.

I then tested the macro on a new dataset to see whether the recorded process could be reused.

## Business Exercise: Automated Dashboard

In the third exercise, I created a dashboard macro.

The macro generated:

- A data quality summary
- A bar chart
- A pie chart

I also used VBA to correct the chart positioning after the macro was run.

## Skills Practiced

Today I practiced:

- Enabling the Developer tab
- Saving workbooks as `.xlsm`
- Recording macros
- Running macros
- Automating formatting tasks
- Formatting charity donation data
- Creating automated data quality reports
- Testing macros on new datasets
- Using formulas within macros
- Creating dashboards with macros
- Creating bar charts automatically
- Creating pie charts automatically
- Using VBA to adjust chart positioning
- Creating a master macro
- Assigning macros to buttons
- Building a one-click dashboard workflow

## Key Takeaways

1. Macros can automate repetitive Excel tasks.
2. The Developer tab provides tools for working with macros.
3. Macro-enabled workbooks should be saved as `.xlsm`.
4. Recorded macros can automate formatting and data preparation.
5. Macros can be tested on new datasets to check their reusability.
6. VBA can be used to modify and improve recorded macros.
7. Macros can automate reports and dashboards.
8. Chart positioning can be controlled using VBA.
9. Multiple macros can be combined into a master macro.
10. Buttons can provide a simple way to run macros.
11. Automation can reduce repetitive work and improve consistency.

## Reflection

Today I learned how Excel can be used to automate an entire analytical workflow rather than only performing individual calculations.

Recording macros helped me understand how repetitive actions can be captured and repeated automatically.

I also learned that VBA can be used to improve recorded macros when the default automation does not produce the desired result.

The one-click dashboard exercise showed me how formatting, data quality checks, summaries, and visualizations can be combined into one automated process.

This is useful for data analysis because recurring reports and dashboards often require the same steps to be performed repeatedly.

## Files

- `day-27-practice.xlsm`

## Learning Resource

30 Day Excel Challenge by SDW Online.
