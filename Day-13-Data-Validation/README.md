# Day 13: Data Validation

## Overview

Today I learned about Data Validation and how Excel can control the type of information users are allowed to enter into cells.

Data Validation is important because accurate analysis depends on accurate data.

If incorrect information enters a dataset, it can affect calculations, reports, and decisions.

## What I Learned

## What is Data Validation?

Data Validation is an Excel feature that restricts what users can enter into a cell.

It helps prevent:

* Incorrect values
* Spelling differences
* Invalid dates
* Impossible numbers
* Inconsistent categories

## Number Validation

Excel can restrict numerical values.

Examples:

Age:

Only allow values between:

18 and 65

Salary:

Only allow values within a specific range.

This prevents unrealistic entries.

## Date Validation

Dates can also be controlled.

Examples:

Allow only dates:

* After a specific date
* Before a specific date
* Within a selected period

This helps maintain accurate time-based records.

## Data Validation Types

Excel provides several validation options:

### Whole Number

Allows only integers.

Example:

Number of employees.

### Decimal

Allows decimal values.

Example:

Product prices.

### List

Creates a dropdown menu.

Example:

Department:

* Finance
* Marketing
* Sales
* HR

### Date

Restricts date entries.

### Time

Controls time values.

### Text Length

Controls the number of characters allowed.

### Custom

Uses formulas to create advanced validation rules.

## Creating Dropdown Lists

Dropdown lists make data entry easier and more consistent.

Instead of typing:

```
Marketing
marketing
MARKETING
```

users select one approved option.

This prevents duplicate categories caused by spelling differences.

## Reference Lists

A common approach is creating a separate worksheet containing approved values.

Example:

A hidden sheet containing department names.

The dropdown list references this sheet.

This keeps validation lists organized and easier to maintain.

## Input Messages

Input messages provide instructions when a user selects a validated cell.

Example:

"Enter a valid order date between January and December 2026."

This helps guide users during data entry.

## Error Alerts

Error alerts appear when someone enters invalid information.

They help prevent incorrect data from being saved.

Types include:

* Stop
* Warning
* Information

## Business Exercise: Ecommerce Data Validation

In today's exercise, I applied validation rules to an ecommerce dataset.

The objective was to improve data quality before analysis.

## Validation Rules Applied

### Order IDs

Validated order IDs to ensure correct entry formats.

### Dates

Restricted order dates to acceptable ranges.

### Prices

Ensured product prices stayed within valid limits.

### Product Names

Created dropdown lists to control product selection.

## Why This Matters for Data Analysis

Data analysts spend significant time working with imperfect datasets.

Preventing errors before they happen is better than correcting them later.

Data Validation improves:

* Accuracy
* Consistency
* Data quality
* Reporting reliability

## Skills Practiced

Today I practiced:

* Creating validation rules
* Creating dropdown lists
* Using reference lists
* Adding input messages
* Creating error alerts
* Controlling numeric values
* Controlling dates
* Improving data entry quality

## Key Takeaways

1. Good analysis starts with good data.
2. Data Validation prevents incorrect entries.
3. Dropdown lists improve consistency.
4. Validation rules reduce cleaning work later.
5. Data quality directly affects analytical results.

## Reflection

Today I learned that analysts do not only analyze data.

They also need to think about how data is collected.

Preventing bad data at the entry stage can save significant time during analysis.

## Files

* `day-13-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
