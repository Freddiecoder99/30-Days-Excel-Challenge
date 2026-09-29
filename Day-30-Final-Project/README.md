# Day 30: Final Data Project

## Overview

Today I completed the final capstone project of the 30 Day Excel Challenge.

The project was based on an edtech startup called LearnFlow and brought together many of the skills I developed throughout the challenge.

Instead of working on one isolated Excel feature, today's project required me to think like a data analyst from beginning to end.

I started by understanding the business questions, explored the available datasets, designed a data model, cleaned and validated the data, created relationships in Power Pivot, wrote DAX measures, built PivotTables, and finally turned the analysis into an interactive dashboard.

This project showed me that data analysis is not simply about creating formulas or charts.

It is about taking a business problem, understanding the data behind it, finding reliable answers, and communicating those answers clearly.

## The LearnFlow Business Scenario

LearnFlow is an edtech startup that wants to understand how users interact with its platform.

The business has multiple datasets containing information about users, platform activity, feedback, features, designs, and other areas of user behaviour.

The management team has seven business questions that need to be answered using the available data.

The goal of the project was to transform the raw data into useful insights that could support business and product decisions.

## Understanding the Business Questions

Before working with the data, I first focused on understanding what the business wanted to know.

The seven business questions provided direction for the entire analysis.

Rather than immediately opening Excel and creating charts, I treated the questions as the starting point for the project.

This helped me think about:

- What information is needed?
- Which tables contain that information?
- How should the tables be connected?
- What calculations are required?
- Which visualizations will communicate the results clearly?

This reinforced an important lesson:

> Good analysis starts with a good question.

## Exploring the Data

The next step was exploring all the available tables.

I reviewed the structure of each table and looked at the type of information it contained.

The purpose was to understand:

- What each table represented
- Which columns were available
- Which columns could be used as keys
- Where duplicate values might exist
- Which tables contained measures or transactions
- Which tables contained descriptive information
- How the tables could potentially be connected

Understanding the data before building the model helped prevent incorrect relationships and unnecessary transformations later.

## Data Modelling Theory

A major part of today's project was understanding how data should be structured for analysis.

Instead of treating every table as an isolated spreadsheet, I learned to think about the dataset as a data model.

The main table types covered were:

- Fact tables
- Dimension tables
- Bridge tables

## Fact Tables

A fact table generally contains measurable events or transactions.

For example, a fact table might contain:

```text
User ID
Date
Feature ID
Click Count
Usage Time
Feedback
```

Fact tables tend to contain multiple records for activities or events.

They are often used as the main source for calculations and metrics.

## Dimension Tables

Dimension tables contain descriptive information about the entities being analyzed.

Examples include:

```text
Users
Features
Designs
Age Groups
Dates
```

A dimension table may contain information such as:

```text
User ID
Name
Age
Country
```

Dimension tables provide the context used to analyze the information in fact tables.

## Bridge Tables

Bridge tables are useful when handling many-to-many relationships.

For example, one user may interact with multiple features, while one feature may be used by many users.

A bridge table can help connect these relationships properly.

A simplified structure could look like:

```text
Users
   |
   |
User Feature Bridge
   |
   |
Features
```

This keeps the data model organized and avoids forcing unrelated tables into a single structure.

## Categorising the Tables

After exploring the datasets, I categorized each table according to its role in the data model.

This helped distinguish between:

```text
Fact Tables
     ↓
Measurements and events

Dimension Tables
     ↓
Descriptions and attributes

Bridge Tables
     ↓
Many-to-many relationships
```

Categorizing the tables also made it easier to determine how relationships should be created later in Power Pivot.

## Planning the Data Model

Before connecting anything, I mapped out the relationships between the tables.

The goal was to identify:

- Primary keys
- Foreign keys
- One-to-many relationships
- Many-to-many relationships
- The direction of relationships
- Which tables should filter other tables

A simplified model might look like:

```text
             Users
               |
               |
        User Activity
          /         \
         /           \
    Features       Feedback
         |
         |
      Designs
```

Planning the model first reduces the risk of creating incorrect relationships.

## Loading Data Into Power Query

Once the structure of the dataset was understood, I loaded the required tables into Power Query.

Power Query provided a workspace for preparing the raw data before it was used in the data model.

The process included:

- Importing the tables
- Reviewing the columns
- Checking data types
- Fixing headers
- Identifying quality problems
- Removing unnecessary issues
- Preparing the tables for Power Pivot

This separated the data preparation stage from the modelling and analysis stage.

## Fixing Column Headers

Some of the imported data required the column headers to be corrected.

Proper headers are important because they make the dataset easier to understand and work with.

A clean header structure should clearly describe the information contained in each field.

For example:

```text
User ID
Feature
Usage Time
Feedback
Sentiment
```

Instead of unclear or inconsistent names.

Clean headers also make formulas, DAX expressions, PivotTables, and visualizations easier to work with.

## Data Quality Checks

Before building the final analysis, I performed data quality checks.

This was important because analytical results are only as reliable as the data behind them.

The checks included looking for:

- Duplicate records
- Missing values
- Inconsistent information
- Other data quality issues

## Finding Duplicates

Duplicate records can affect counts, averages, and other calculations.

For example:

```text
User ID
1001
1002
1003
1002
```

The repeated value needs to be investigated to determine whether it represents:

- A legitimate repeated activity
- An accidental duplicate
- Multiple records that belong to the same entity

The important point is to distinguish between valid repeated events and actual duplicate records.

## Finding Missing Values

Missing values were also checked during the data quality process.

Missing information can affect:

- Calculations
- Relationships
- Filters
- PivotTables
- Dashboard metrics

Identifying missing information before analysis helps improve confidence in the final results.

## Data Quality Pivot Table

The identified quality issues were summarized using a PivotTable.

This provided a simple overview of the number and type of issues detected.

A quality summary can be structured like:

```text
Issue Type        | Count
------------------|------
Duplicate Records | ...
Missing Values    | ...
Other Issues      | ...
```

This creates a clear record of the data quality checks performed before analysis.

## Combining Issue Tables

The separate issue tables were combined into a single structure.

This made the data quality information easier to manage and analyze.

Combining the issues also demonstrated how Power Query can bring related datasets together before they are loaded into the data model.

## Cleaning the Data

After identifying the issues, I cleaned the affected datasets.

This included removing duplicate records where appropriate.

The objective was not simply to delete unusual information.

Instead, the goal was to determine which records represented genuine data and which represented actual quality problems.

This reinforced an important data analysis principle:

> Data cleaning should be based on understanding the data, not blindly removing anything that looks unusual.

## Loading the Clean Data Into Power Pivot

Once the data had been prepared, the cleaned tables were loaded into Power Pivot.

Power Pivot was used to create the analytical data model.

This allowed the tables to remain separate while still being connected through relationships.

The data model became the foundation for the calculations and PivotTables used later in the project.

## Establishing Relationships in Power Pivot

I created relationships between the relevant tables using Power Pivot's Diagram View.

The relationships connected the different parts of the LearnFlow dataset.

This allowed information from different tables to work together during analysis.

For example:

```text
Dimension Table
       |
       ↓
    Fact Table
       |
       ↓
  Analytical Result
```

The relationships made it possible to analyze activity using descriptive attributes from other tables.

## Why Relationships Matter

Without correct relationships, information from different tables cannot be analyzed reliably.

For example, if user activity is stored separately from user demographics, the relationship between those tables allows activity to be analyzed by:

- Age
- User group
- Other user attributes

The same principle applies when analyzing features, design tags, feedback, and other information.

## Creating DAX Measures

After building the data model, I created DAX measures to answer the business questions.

DAX measures are useful because they can calculate results dynamically based on the filters and context used in PivotTables.

The measures created in the project included calculations related to:

- Click count
- Average time
- Sentiment
- Design tags
- User behaviour

These measures formed the analytical foundation of the final dashboard.

## Click Count Measure

One of the measures focused on user interaction and click activity.

The purpose was to understand how frequently users interacted with features on the platform.

A click-based metric can help answer questions around:

- Feature engagement
- Usage frequency
- User interaction

## Average Time Measure

Another measure focused on average time.

This allowed user behaviour to be analyzed based on how long users spent interacting with the platform or its features.

Average time can provide another perspective on engagement beyond simply counting clicks.

## Sentiment Measure

I also created a measure related to user sentiment.

Sentiment analysis helped summarize how users responded to the platform.

This allowed the feedback data to be incorporated into the wider analysis.

Sentiment could then be viewed over time or across different user groups.

## Design Tag Measures

Additional DAX measures were created to analyze design-related information.

This helped identify patterns in the performance of different design tags.

These metrics were later used in the dashboard.

## User Behaviour Measures

The project also included calculations focused on user behaviour.

This helped move the analysis beyond individual records and toward broader patterns in how users interacted with LearnFlow.

## Calculated Columns

In addition to measures, I created calculated columns.

Calculated columns create a new value for each row based on an expression.

Two examples from the project were:

- Feature click count
- Low usage flag

## Feature Click Count

A calculated column was created to capture feature-level click activity.

This made the interaction data easier to analyze at the feature level.

It could then be used to identify which features received more or less interaction.

## Low Usage Flag

A low usage flag was created to identify records or features with relatively low usage.

The purpose was to create a category that could be used during analysis.

For example:

```text
Usage
  ↓
Low Usage?
  ↓
Yes / No
```

This demonstrates how calculated columns can turn raw values into meaningful analytical categories.

## Creating PivotTables

After creating the data model and DAX measures, I built PivotTables to answer the seven business questions.

Each PivotTable was designed around a specific analytical requirement.

The PivotTables allowed me to:

- Summarize metrics
- Compare categories
- Analyze trends
- Explore user behaviour
- Evaluate feature usage
- Examine sentiment
- Identify patterns

This step transformed the raw datasets into structured answers that could be used for the dashboard.

## Connecting the Analysis to the Business Questions

I learned that every PivotTable and visualization should have a reason for existing.

Rather than creating charts simply because they look useful, I connected each analysis back to one of the business questions.

The process was:

```text
Business Question
       ↓
Required Data
       ↓
Data Model
       ↓
DAX Measure
       ↓
PivotTable
       ↓
Visualization
       ↓
Business Insight
```

This created a clear connection between the original business problem and the final dashboard.

## Dashboard Wireframe

Before designing the final dashboard, I created a wireframe.

A wireframe is a basic plan showing where different dashboard elements will be placed.

The wireframe helped determine:

- Where the KPIs would go
- Where charts would be positioned
- How much space each visual needed
- How the dashboard would be organized
- How users would move through the information

Planning the layout first helped avoid simply adding visuals wherever there was available space.

## Dashboard Structure

The dashboard was organized into several sections.

A simplified structure was:

```text
--------------------------------------------------
|              LEARNFLOW DASHBOARD               |
--------------------------------------------------
| KPI 1 | KPI 2 | KPI 3 | KPI 4 | KPI 5         |
--------------------------------------------------
|       Sentiment Trend Over Time               |
--------------------------------------------------
| Usage by Age Group | User Sentiment           |
--------------------------------------------------
| Features Used Most | Best Performing Tags     |
--------------------------------------------------
```

The layout was designed to provide a high-level overview first and then allow the user to explore individual areas in more detail.

## KPI Scorecards

KPI scorecards were added to the top section of the dashboard.

The purpose of a KPI is to provide a quick view of an important metric.

The scorecards summarized key measures from the analysis.

Examples included metrics related to:

- Click activity
- Average usage time
- Sentiment
- Feature usage
- User behaviour

KPI cards are useful because they provide immediate context before the user looks at the detailed charts.

## Line Chart: Sentiment Trend Over Time

The first major visualization was a line chart showing sentiment over time.

A line chart is useful for identifying changes and trends across a period.

It can help answer questions such as:

- Is sentiment improving?
- Is sentiment declining?
- Are there periods of significant change?
- Are there noticeable patterns over time?

The chart made it easier to see how sentiment changed rather than looking at individual records.

## Clustered Bar Chart: Usage by Age Group

The next visualization was a clustered bar chart showing usage by age group.

This allowed user activity to be compared across different age categories.

The chart provided a visual comparison of how different groups interacted with LearnFlow.

This type of analysis can help identify whether usage patterns differ between user groups.

## Donut Chart: User Feedback Sentiment

A donut chart was used to show the distribution of user feedback sentiment.

The chart represented the proportion of different sentiment categories.

For example:

```text
Positive
Neutral
Negative
```

This made the overall feedback profile easier to understand at a glance.

## Clustered Bar Chart: Features Used Most

Another clustered bar chart showed which features were used most frequently.

This helped identify the features receiving the greatest amount of user interaction.

Feature usage is useful for understanding:

- User engagement
- Popular functionality
- Feature adoption
- Areas receiving less interaction

## Heat Map: Best Performing Design Tags

The final major visualization was a heat map showing the best-performing design tags.

A heat map uses differences in cell intensity to make patterns easier to spot across categories.

This provided a quick visual comparison of design tag performance.

It also demonstrated that dashboards do not need to rely only on traditional charts.

## Five Dashboard Visuals

The final dashboard included five main visualizations:

1. Sentiment trend over time
2. Usage by age group
3. User feedback sentiment
4. Features used most
5. Best performing design tags

Each visualization served a different analytical purpose.

## Dashboard Design Principles

While building the dashboard, I focused on keeping the presentation clear.

The dashboard needed to make information easy to find without overwhelming the user.

Important design considerations included:

- Clear headings
- Consistent spacing
- Logical placement
- Readable labels
- Consistent formatting
- Appropriate chart selection
- Clear KPI presentation
- Visual hierarchy

The goal was to make the dashboard understandable even for someone who did not build the underlying analysis.

## Final Formatting

The final stage involved polishing the dashboard and workbook.

This included reviewing:

- Alignment
- Spacing
- Titles
- Chart sizes
- KPI placement
- Number formatting
- Table presentation
- Overall consistency

Small formatting details can make a large difference in how easily a dashboard can be understood.

## End-to-End Analytical Workflow

The entire project followed an analytical workflow:

```text
Business Questions
        ↓
Explore Data
        ↓
Categorise Tables
        ↓
Plan Data Model
        ↓
Power Query
        ↓
Data Quality Checks
        ↓
Clean Data
        ↓
Power Pivot
        ↓
Create Relationships
        ↓
DAX Measures
        ↓
Calculated Columns
        ↓
PivotTables
        ↓
Dashboard Wireframe
        ↓
KPI Scorecards
        ↓
Charts
        ↓
Final Dashboard
```

This workflow brought together many of the techniques I learned throughout the challenge.

## What This Project Taught Me

The final project showed me that Excel data analysis is not just about knowing individual features.

The real value comes from knowing when and how to combine those features.

For example:

```text
Power Query
     +
Power Pivot
     +
DAX
     +
PivotTables
     +
Charts
     +
Dashboard Design
```

can be combined into a complete analytical workflow.

Each tool performs a different role, but together they allow raw data to be transformed into useful information.

## Skills Practiced

Throughout the final project, I practiced:

- Understanding business requirements
- Translating business questions into analytical tasks
- Exploring multiple datasets
- Understanding fact tables
- Understanding dimension tables
- Understanding bridge tables
- Categorising tables
- Mapping table relationships
- Loading data into Power Query
- Fixing column headers
- Checking for duplicates
- Checking for missing values
- Summarizing data quality issues
- Combining issue tables
- Cleaning datasets
- Loading data into Power Pivot
- Creating table relationships
- Using Diagram View
- Creating DAX measures
- Creating calculated columns
- Using click count metrics
- Calculating average time
- Analyzing sentiment
- Analyzing design tags
- Analyzing user behaviour
- Creating PivotTables
- Answering business questions with data
- Wireframing a dashboard
- Creating KPI scorecards
- Creating line charts
- Creating clustered bar charts
- Creating donut charts
- Creating heat maps
- Formatting dashboards
- Communicating analytical results

## Key Takeaways

1. Data analysis should begin with the business problem, not the spreadsheet.
2. Business questions provide direction for the entire analytical workflow.
3. Understanding the structure of each table is essential before building a data model.
4. Fact tables contain events or measurable activity, while dimension tables provide descriptive context.
5. Bridge tables can help resolve many-to-many relationships.
6. Power Query is useful for preparing and cleaning data before analysis.
7. Data quality checks should happen before important calculations are made.
8. Power Pivot makes it possible to analyze multiple related tables as one data model.
9. Relationships are fundamental to reliable multi-table analysis.
10. DAX measures allow dynamic calculations to be performed within the data model.
11. Calculated columns can create useful categories and analytical fields.
12. PivotTables can convert a large data model into answers to specific business questions.
13. A dashboard should communicate insights, not simply display charts.
14. KPI scorecards provide a quick summary of important metrics.
15. Chart selection should match the question being answered.
16. Dashboard layout and formatting are part of effective data communication.
17. A strong analytical workflow connects business questions, data, calculations, and visualizations.

## Final Reflection

Today felt different from the previous days because I was no longer learning Excel features in isolation.

I was bringing everything together.

I started with a business problem and had to work backwards to determine what data I needed, how that data should be structured, how the tables should relate to one another, and which calculations would answer the questions.

The data quality stage reminded me that analysis is only as strong as the data behind it.

The Power Query and Power Pivot stages showed me how important data preparation and data modelling are when working with multiple datasets.

Creating DAX measures and PivotTables then allowed me to turn the cleaned data into meaningful analysis.

Finally, building the dashboard taught me that presenting the results is just as important as calculating them.

A technically correct analysis can still be difficult to use if the information is poorly organized or difficult to interpret.

This final project gave me a much clearer picture of what a real data analysis workflow can look like:

```text
Question
   ↓
Data
   ↓
Quality
   ↓
Model
   ↓
Analysis
   ↓
Insight
   ↓
Visualization
   ↓
Decision Support
```

Completing this 30 Day Excel Challenge has helped me move from learning individual Excel functions to thinking more like a data analyst.

## Challenge Recap

Across the 30 days, I worked through a broad range of Excel and data analysis skills, including:

- Data cleaning
- Formulas
- Lookups
- Conditional logic
- Data validation
- PivotTables
- Data visualization
- Power Query
- Power Pivot
- DAX
- Data quality
- Macros
- Data-entry forms
- Keyboard shortcuts
- Data modelling
- Dashboard development

The final project brought many of these skills together into one end-to-end workflow.

## Files

- `day-30-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
