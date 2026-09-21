# Day 20: Power Query (Part 1)

## Overview

Power Query is an Excel tool used to import, clean, transform, and prepare data for analysis.

Instead of manually cleaning data every time, Power Query records the transformation steps so they can be repeated.

Today we focus on:

* What Power Query is
* Why manual cleaning can be risky and repetitive
* Removing blank rows
* Standardising text casing
* Removing duplicates
* Splitting columns
* Filling blanks
* Creating custom columns
* Unpivoting data
* Loading cleaned data back into Excel

---

## What I Learned

### 1. What Is Power Query?

Power Query is a data transformation tool in Excel.

It allows me to:

* Import data
* Clean data
* Transform data
* Restructure data
* Load the cleaned result back into Excel

One of its biggest advantages is that **Power Query records the steps I perform**.

This means I can repeat the same cleaning process when new data becomes available instead of manually performing every step again.

---

### 2. Why Power Query Is Useful

Manual cleaning can be:

* Repetitive
* Time-consuming
* Easy to perform inconsistently
* Difficult to repeat

Power Query provides a more repeatable process.

The basic idea is:

```text
Raw Data
   ↓
Power Query
   ↓
Cleaning & Transformation Steps
   ↓
Clean Data
   ↓
Load Back to Excel
```

---

### 3. Opening Power Query

Power Query can be accessed from Excel through the **Data** tab.

The exact option depends on how the data is being imported, but the main workflow is to bring the data into the **Power Query Editor**, perform transformations, and then load the result back into Excel.

---

### 4. Removing Blank Rows

Power Query can remove blank rows without manually searching through the dataset.

This is useful when working with larger datasets where manually finding and deleting blank rows would take time.

The transformation becomes part of the recorded query steps.

---

### 5. Standardising Casing

Power Query can standardise text casing.

For example, inconsistent feature names such as:

```text
Login
LOGIN
login
```

can be transformed into a consistent format.

This helps keep categories consistent throughout the dataset.

---

### 6. Removing Duplicates

Power Query can remove duplicate rows from a dataset.

This is similar to the duplicate-cleaning work from Day 19, but the important difference is that the process becomes part of the Power Query transformation steps.

This makes the cleaning process easier to repeat.

---

### 7. Splitting Columns

Power Query can split one column into multiple columns.

For example, a column containing:

```text
John Smith
```

can be split into:

| First Name | Last Name |
| ---------- | --------- |
| John       | Smith     |

This is useful when information is stored together but needs to be analyzed separately.

---

### 8. Filling Blank Values

Power Query can be used to fill missing values in a column.

This is useful when the correct replacement value is known.

As with Day 19, I should not simply guess missing information.

---

### 9. Unpivoting Data

Unpivoting is one of the most important concepts introduced today.

Sometimes data is stored in a **wide format**.

For example:

| Product   | January | February | March |
| --------- | ------: | -------: | ----: |
| Product A |     100 |      120 |   150 |
| Product B |      80 |       90 |   110 |

Power Query can transform this into a **flat/long format**:

| Product   | Month    | Sales |
| --------- | -------- | ----: |
| Product A | January  |   100 |
| Product A | February |   120 |
| Product A | March    |   150 |
| Product B | January  |    80 |
| Product B | February |    90 |
| Product B | March    |   110 |

This is called **unpivoting**.

It makes the data easier to analyze and work with.

---

### 10. Custom Columns

Power Query allows me to create a new column using a formula.

In today's exercise, a custom column is used to create a **status field** based on the team information.

This allows the transformation logic to become part of the query rather than manually creating the column in Excel.

---

## Product Team Quarterly Data Exercise

Today's main exercise uses product team quarterly data.

The cleaning process includes:

1. Opening the dataset in Power Query
2. Fixing inconsistent feature-name casing
3. Removing duplicate rows
4. Filling missing values
5. Creating a custom status column
6. Creating a custom column using a formula
7. Unpivoting the hours columns
8. Cleaning the budget column
9. Loading the transformed data back into Excel

---

## Why This Matters for Data Analysis

Power Query is important because real-world datasets often need to be cleaned and transformed before analysis.

Instead of manually repeating the same cleaning process, Power Query allows the steps to be recorded and reused.

This becomes especially useful when:

* Working with larger datasets
* Receiving updated data regularly
* Repeating the same analysis
* Preparing data for dashboards
* Combining and transforming multiple datasets

---

## Skills Practiced

* Opening Power Query
* Removing blank rows
* Standardising text
* Removing duplicates
* Splitting columns
* Filling missing values
* Creating custom columns
* Unpivoting data
* Cleaning numeric columns
* Loading transformed data back into Excel

---

## Key Takeaways

* Power Query is used to clean and transform data.
* It records the transformation steps.
* Recorded steps make cleaning more repeatable.
* Power Query can remove blank rows and duplicates.
* Columns can be split into separate fields.
* Missing values can be filled when the correct value is known.
* Custom columns can be created using formulas.
* Unpivoting converts wide data into a more analysis-friendly format.
* Power Query reduces the need for repetitive manual cleaning.

---

## Files

```text
Day-20-Power-Query-Part-1/
├── README.md
└── day-20-practice.xlsx
```

## Learning Resource

30 Day Excel Challenge by SDW Online.
