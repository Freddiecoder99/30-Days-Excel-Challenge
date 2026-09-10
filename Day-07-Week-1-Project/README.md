# Day 7: Expense Report Project

## Project Overview

This project is the first complete Excel project in my 30 Days Excel Challenge.

The goal of this project was to apply the Excel skills learned during the first week to create an expense report that helps a manager understand departmental spending, identify overspending, and make better budget decisions.

Instead of only practicing individual Excel features, this project combined formatting, formulas, conditional formatting, and data visualization into a complete reporting workflow.

## Business Problem

The manager currently does not have a clear view of:

* Which departments are spending the most money
* Where expenses are being allocated
* Whether departments are staying within their budgets
* Which departments require attention before overspending becomes a bigger issue

The main challenge is that problems are usually discovered after money has already been spent.

The objective of this report is to provide an easier way to monitor spending and identify potential budget issues early.

## User Requirements

### User

The main user of this report is:

**A department manager**

### User Needs

The manager needs:

* A clear view of departmental spending
* A way to compare expenses against budgets
* A method to identify departments exceeding their budgets
* A visual summary showing where money is being spent

## Project Objective

The objective was to build an expense report that can:

1. Show department spending.
2. Track expense movement across departments.
3. Identify departments that exceed their budgets.
4. Help managers make smarter budget decisions.

## Dataset Structure

The report uses the following fields:

| Field         | Description                                          |
| ------------- | ---------------------------------------------------- |
| Department    | The department responsible for the expense           |
| Category      | The type of expense                                  |
| Expense ($)   | The amount spent                                     |
| Budget ($)    | The allocated budget amount                          |
| Budget Status | Indicates whether spending is within or above budget |

## Analysis Process

The project workflow involved:

### 1. Data Organization

The raw expense data was structured into a clear table containing:

* Department names
* Expense categories
* Expense amounts
* Budget amounts
* Budget status indicators

### 2. Budget Comparison

Expenses were compared against allocated budgets to determine whether departments were staying within their limits.

A budget status field was created to help identify departments that required attention.

### 3. Conditional Formatting

Conditional formatting was used to highlight important information automatically.

This allowed overspending areas to stand out visually without manually checking every department.

## Dashboard and Visualizations

Two visualizations were created to communicate the results.

## 1. Expenses vs Budget by Department

A clustered column chart was created to compare:

* Total expenses per department
* Budget allocation per department

This visualization helps identify departments that are spending close to or above their allocated budgets.

## 2. Expense Distribution

A treemap visualization was created to show how expenses are distributed across categories.

This helps the user understand where the majority of spending is concentrated.

## Excel Skills Applied

This project applied the Excel skills learned during Week 1:

### Excel Fundamentals

* Workbook organization
* Worksheet management
* Data entry and navigation

### Formatting

* Number formatting
* Currency formatting
* Table formatting
* Improving readability

### Formulas and Functions

* Basic calculations
* Comparing values
* Creating calculated fields

### Sorting and Filtering

* Exploring expense records
* Identifying specific departments and categories

### Conditional Formatting

* Highlighting budget issues
* Creating visual indicators for important values

### Data Visualization

* Clustered column charts
* Treemap visualization
* Communicating insights through visuals

## Key Insights

The completed report allows the manager to quickly answer questions such as:

* Which departments have the highest expenses?
* Which departments are exceeding their budgets?
* Which expense categories represent the largest spending areas?
* Where should management focus attention?

## Project Outcome

The final expense report provides the manager with a clearer overview of spending patterns and makes it easier to identify potential budget problems before they become larger issues.

The project demonstrates how Excel can be used not only for calculations but also for building practical reporting tools that support decision-making.

## What I Learned

This project helped me understand how individual Excel skills connect together in a real analysis workflow.

Before this project, I learned formulas, formatting, sorting, filtering, charts, and conditional formatting separately.

During this project, I learned how those skills combine to solve a real business problem.

The biggest lesson was that a good Excel report is not just about presenting numbers. It should help someone understand a situation and make better decisions.

## Files

```text
Day-07-Week-1-Project/
│
├── README.md
└── day-07-guided-project.xlsx
```

## Learning Resource

30 Day Excel Challenge by SDW Online.
