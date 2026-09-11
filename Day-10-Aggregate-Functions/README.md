# Day 10: Aggregate Functions

## Overview

Today I learned about aggregate functions in Excel.

Aggregate functions allow me to summarize large amounts of data by calculating totals, averages, counts, and other summary statistics.

These functions are commonly used in data analysis because they transform raw records into meaningful information.

## What I Learned

## SUM

SUM adds numbers together.

Example:

```excel
=SUM(B2:B100)
```

Used for calculating totals.

Examples:

* Total sales
* Total expenses
* Total revenue

## AVERAGE

AVERAGE calculates the mean value.

Example:

```excel
=AVERAGE(B2:B100)
```

Useful for understanding typical values.

Examples:

* Average order value
* Average salary
* Average expense

## COUNT

COUNT counts cells containing numbers.

Example:

```excel
=COUNT(B2:B100)
```

Useful for understanding how many numerical records exist.

## COUNTA

COUNTA counts cells that are not empty.

Example:

```excel
=COUNTA(A2:A100)
```

Useful when counting records containing text or numbers.

## COUNTBLANK

COUNTBLANK counts empty cells.

Example:

```excel
=COUNTBLANK(A2:A100)
```

Useful for identifying missing information.

## MIN and MAX

MIN finds the smallest value.

MAX finds the largest value.

Examples:

```excel
=MIN(B2:B100)
```

```excel
=MAX(B2:B100)
```

Useful for identifying extremes in datasets.

## LARGE and SMALL

These functions return specific ranked values.

Example:

```excel
=LARGE(B2:B100,5)
```

Returns the fifth largest value.

Example:

```excel
=SMALL(B2:B100,3)
```

Returns the third smallest value.

## Why This Matters for Data Analysis

Aggregate functions help answer questions such as:

* What is the total revenue?
* What is the average expense?
* What was the highest transaction?
* How many customers exist?
* Are there missing values?

These calculations form the foundation of reporting.

## Practice

Today I practiced:

* Calculating totals
* Finding averages
* Counting records
* Identifying maximum and minimum values
* Summarizing datasets

## Key Takeaways

1. Aggregate functions summarize information.
2. They help transform raw data into insights.
3. COUNT and COUNTA serve different purposes.
4. Summary calculations are essential before creating reports.

## Reflection

Today helped me understand how analysts quickly summarize large datasets.

Instead of manually reviewing thousands of rows, aggregate functions allow Excel to provide useful information instantly.

## Files

* `day-10-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
