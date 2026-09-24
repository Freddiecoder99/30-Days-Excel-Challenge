# Day 23: Dynamic Array Functions

## Overview

Today I learned about **dynamic array functions** in Excel and how they can return multiple results from a single formula.

The focus was on:

* Understanding dynamic arrays
* Using `UNIQUE` to extract distinct values
* Using `SORTBY` to sort data based on another column
* Using `FILTER` to return rows matching a condition
* Using `SEQUENCE` to generate a sequence of numbers
* Using `CHOOSECOLS` to select specific columns
* Using `ROWS` to count rows
* Using `TAKE` to return a specified number of rows
* Applying dynamic array functions to nonprofit donation data

Dynamic array functions are useful because they can make data analysis more flexible and reduce the need for manually creating separate formulas for each result.

## What I Learned

# Dynamic Array Functions

Dynamic array functions can return multiple values from one formula.

Instead of creating a formula in every row, Excel can automatically **spill** the results into the cells below or beside the formula.

This makes it easier to create dynamic lists and filtered datasets.

---

# UNIQUE

`UNIQUE` extracts distinct values from a range.

## UNIQUE Syntax

Structure:

```excel
=UNIQUE(array)
```

Example:

```excel
=UNIQUE(A2:A100)
```

This returns each unique value from the range.

For example, if the original data contains:

```text
Kenya
Uganda
Kenya
Tanzania
Uganda
```

`UNIQUE` returns:

```text
Kenya
Uganda
Tanzania
```

This is useful for creating lists of unique:

* Donors
* Countries
* Products
* Departments
* Categories

---

# SORTBY

`SORTBY` sorts a range based on another range.

## SORTBY Syntax

Structure:

```excel
=SORTBY(array, by_array)
```

Example:

```excel
=SORTBY(A2:B20,B2:B20,-1)
```

The `-1` sorts in descending order.

This can be useful when I want to sort donors based on their donation amount without manually sorting the original dataset.

---

# FILTER

`FILTER` returns rows that meet a specific condition.

## FILTER Syntax

Structure:

```excel
=FILTER(array, include)
```

Example:

```excel
=FILTER(A2:D100,C2:C100="PayPal")
```

This returns the rows where the payment method is `PayPal`.

FILTER is useful when I want to create a dynamic subset of a dataset without changing the original data.

---

# SEQUENCE

`SEQUENCE` generates a sequence of numbers automatically.

## SEQUENCE Syntax

Structure:

```excel
=SEQUENCE(rows)
```

Example:

```excel
=SEQUENCE(10)
```

This generates:

```text
1
2
3
4
5
6
7
8
9
10
```

SEQUENCE can be useful when generating numbered lists or creating dynamic sequences for analysis.

---

# CHOOSECOLS

`CHOOSECOLS` allows me to return selected columns from a dataset.

## CHOOSECOLS Syntax

Structure:

```excel
=CHOOSECOLS(array,col_num1,col_num2,...)
```

Example:

```excel
=CHOOSECOLS(A2:E100,1,3,5)
```

This returns columns 1, 3, and 5 from the selected range.

This is useful when I only need certain columns from a larger dataset.

---

# ROWS

`ROWS` returns the number of rows in a range or array.

## ROWS Syntax

Structure:

```excel
=ROWS(array)
```

Example:

```excel
=ROWS(A2:A20)
```

This returns the number of rows in the range.

It can also be combined with dynamic arrays.

For example:

```excel
=ROWS(UNIQUE(A2:A100))
```

This can be used to count the number of unique values.

---

# TAKE

`TAKE` returns a specified number of rows or columns from an array.

## TAKE Syntax

Structure:

```excel
=TAKE(array,rows)
```

Example:

```excel
=TAKE(A2:B100,10)
```

This returns the first 10 rows.

To return the last 10 rows:

```excel
=TAKE(A2:B100,-10)
```

This is useful for creating lists such as the top 10 results after sorting data.

---

# Nonprofit Donation Exercise

Today's exercise uses nonprofit donation data to practice dynamic array functions.

The exercises include:

* Creating a unique donor list
* Sorting donors by donation amount
* Filtering PayPal donations
* Counting unique donors
* Returning the top 10 donors

---

# UNIQUE for Donor List

`UNIQUE` is used to create a list of distinct donors.

Example:

```excel
=UNIQUE(DonorRange)
```

This prevents the same donor from appearing multiple times in the resulting list.

---

# SORTBY for Top Donors

`SORTBY` is used to sort donation records based on the donation amount.

For example:

```excel
=SORTBY(A2:B100,B2:B100,-1)
```

This sorts the data from the largest donation to the smallest.

This provides a way to identify the highest-value donors.

---

# FILTER for PayPal Donations

`FILTER` is used to return only donations made through PayPal.

Example:

```excel
=FILTER(A2:E100,C2:C100="PayPal")
```

The result contains only the records matching the PayPal condition.

---

# Counting Unique Donors

`ROWS` and `UNIQUE` can be combined to count distinct donors.

Example:

```excel
=ROWS(UNIQUE(A2:A100))
```

`UNIQUE` creates the distinct donor list, while `ROWS` counts how many values are in that list.

---

# Top 10 Donors

`SORTBY` and `TAKE` can be combined to create a top-10 list.

The basic idea is:

```text
Donation Data
      ↓
SORTBY
      ↓
Highest Donations First
      ↓
TAKE
      ↓
Top 10
```

This creates a dynamic list of the highest donations without manually sorting and selecting the records.

---

# Why This Matters for Data Analysis

Dynamic array functions make it easier to create flexible and automatically updating analysis.

They are useful for tasks such as:

* Creating unique lists
* Filtering datasets
* Sorting results
* Selecting columns
* Counting distinct values
* Creating top-N lists

Instead of manually copying and updating results, dynamic formulas can update automatically when the source data changes.

---

# Key Takeaways

1. Dynamic array functions can return multiple results from one formula.
2. `UNIQUE` extracts distinct values.
3. `SORTBY` sorts data using another range.
4. `FILTER` returns records matching a condition.
5. `SEQUENCE` generates a sequence of numbers.
6. `CHOOSECOLS` selects specific columns from an array.
7. `ROWS` can count the results of a dynamic array.
8. `TAKE` can return a specified number of rows or columns.
9. Dynamic arrays can make analysis more flexible and automated.
10. Multiple dynamic array functions can be combined to solve more complex analysis problems.
11. Dynamic array functions are used when data is likely to grow or shrink.

---

# Files

* `day-23-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
