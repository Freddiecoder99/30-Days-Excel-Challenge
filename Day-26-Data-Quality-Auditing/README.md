# Day 26: Data Quality

## Overview

Data quality is about checking whether data is accurate, complete, consistent, valid, and suitable for analysis.

Today we focus on:

* Data quality vs data validation
* Missing values
* Duplicate records
* Validity checks
* Identifying outliers
* Creating a data quality summary
* Visualizing data-quality issues

---

## What I Learned

### 1. Data Quality vs Data Validation

**Data quality** is the process of checking whether existing data is reliable and suitable for use.

**Data validation** is about controlling what data can be entered into a dataset.

A simple way to remember the difference:

```text
Data Validation → Prevent bad data
Data Quality    → Check existing data
```

For example:

* Data Validation can restrict a Country column to approved countries.
* Data Quality can check an existing dataset for invalid countries.

---

### 2. Checking for Missing Values

Missing cells can indicate incomplete data.

For example, HR employee data may contain missing:

* Employee names
* Departments
* Salaries
* Other employee information

Checking for missing values helps determine whether the dataset is complete enough for analysis.

---

### 3. Finding Duplicate Records

Duplicate records can cause incorrect counts and analysis.

`COUNTIF` can be used to identify duplicate values.

Example:

```excel id="7p2nqf"
=COUNTIF($A$2:$A$100,A2)
```

If the result is greater than `1`, the value appears more than once.

This can be used to flag duplicate ticket IDs or other identifiers.

---

### 4. Validity Checks

A validity check determines whether a value is acceptable according to a defined rule.

For example, a Country column may only allow a specific list of valid countries.

If a country falls outside that list, it can be flagged as invalid.

This is different from simply checking whether the cell is blank.

A value can be:

* Present but valid
* Present but invalid
* Missing

---

## Main Exercise: Returned and Damaged Goods

Today's main exercise focuses on auditing returned and damaged goods data.

The objective is to identify data-quality issues and summarize them clearly.

The exercise includes:

* Duplicate return IDs
* Zero refund amounts
* Data quality summary
* Issue-type visualization

---

### 5. Flagging Duplicate Return IDs

`COUNTIF` is used to check whether a return ID appears more than once.

Example:

```excel id="j4qv5c"
=COUNTIF($A$2:$A$100,A2)>1
```

This can return:

```text
TRUE
```

when the ID is duplicated.

The duplicate records can then be investigated.

---

### 6. Flagging Outliers

The exercise identifies **zero refund amounts** as a data-quality issue/outlier.

A simple logical check can flag them:

```excel id="g1x9r2"
=RefundAmount=0
```

or, when working with a cell:

```excel id="q6p7td"
=IF(E2=0,"Check","OK")
```

The purpose is not necessarily to assume that every zero refund is incorrect, but to **flag the record for investigation**.

---

### 7. Data Quality Summary Table

After identifying the problems, the issues are summarized in a data quality table.

For example:

| Issue Type     | Number of Issues |
| -------------- | ---------------: |
| Duplicate IDs  |              ... |
| Missing Values |              ... |
| Invalid Values |              ... |
| Zero Refunds   |              ... |

The summary provides a quick overview of the quality of the dataset.

---

### 8. Visualizing Data Quality Issues

The project uses charts to communicate the identified issues.

#### Bar Chart

A bar chart is created to compare the different issue types.

This makes it easier to see which types of data-quality problems occur most frequently.

#### Pie Chart

A pie chart is also created to show the distribution of the identified issues.

These visualizations turn the data-quality audit into something that can be quickly communicated to others.

---

## Why This Matters for Data Analysis

Poor data quality can lead to unreliable analysis.

For example:

```text
Duplicate records
      ↓
Incorrect counts
      ↓
Incorrect analysis
      ↓
Incorrect conclusions
```

Data-quality checks help identify problems before they affect reports, dashboards, and decisions.

This is especially important when working with business data such as:

* Employees
* Customers
* Support tickets
* Orders
* Returns
* Financial records

---

## Skills Practiced

* Understanding data quality
* Distinguishing data quality from data validation
* Checking missing values
* Finding duplicates
* Using `COUNTIF`
* Performing validity checks
* Identifying outliers
* Creating data-quality flags
* Building summary tables
* Creating bar charts
* Creating pie charts

---

## Key Takeaways

* Data quality checks existing data; data validation helps control new data entry.
* Missing values should be identified before analysis.
* `COUNTIF` can help identify duplicate records.
* Validity checks determine whether values meet defined rules.
* Outliers or unusual values should be flagged for investigation.
* A data quality summary provides a quick overview of identified problems.
* Charts can make data-quality issues easier to communicate.

---

## Reflection

Today I learned how to audit a dataset for common data-quality problems.

I practiced checking for missing values, duplicate IDs, invalid values, and unusual refund amounts. I also learned how to summarize these issues and visualize them using charts.

---

## Files

```
day-26-practice.xlsx
```

## Learning Resource

30 Day Excel Challenge by SDW Online.
