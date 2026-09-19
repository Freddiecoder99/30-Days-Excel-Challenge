# Day 19: Data Cleaning

## Overview

Data cleaning is the process of finding and fixing problems in a dataset before analyzing it.

Today we focus on:

* Duplicate records
* Blank cells
* Inconsistent casing
* Hidden spaces
* Inconsistent country names
* Cleaning a customer support ticket dataset

---

## What I Learned

### 1. Duplicate Records

Duplicates are records that appear more than once in a dataset.

Excel provides **Data → Remove Duplicates** to remove duplicate records.

When checking duplicates, it is important to consider multiple columns because one column alone may not uniquely identify a record.

### Concatenation Trick

Multiple columns can be combined to help identify duplicates:

```excel
=A2&"|"&B2&"|"&C2
```

This creates one combined value from several columns.

I can then use `COUNTIF` to see how many times that combination appears:

```excel
=COUNTIF($D$2:$D$100,D2)
```

---

### 2. Blank Cells

Missing values are another common data-cleaning problem.

Use `COUNTBLANK` to count empty cells:

```excel
=COUNTBLANK(A2:A100)
```

This helps identify columns that contain missing information.

Blank cells can then be filled using **Find and Replace** when the correct replacement value is known.

---

### 3. Inconsistent Casing

The same value can appear in different forms:

```text
Sales
sales
SALES
```

Excel provides three functions for standardizing text.

**UPPER**

```excel
=UPPER(A2)
```

Converts text to uppercase.

**LOWER**

```excel
=LOWER(A2)
```

Converts text to lowercase.

**PROPER**

```excel
=PROPER(A2)
```

Converts text to title case.

These functions help standardize department names and other text values.

---

### 4. Hidden Spaces

Extra spaces can make values look identical even though the underlying text is different.

For example:

```text
Sales
Sales 
```

The second value contains an extra space.

Use `TRIM` to remove unnecessary spaces:

```excel
=TRIM(A2)
```

### Using LEN to Check Spaces

`LEN` counts the number of characters:

```excel
=LEN(A2)
```

We can compare:

```excel
=LEN(A2)
```

with:

```excel
=LEN(TRIM(A2))
```

If the numbers are different, extra spaces were present.

---

### 5. Standardizing Country Names

Country names may appear in different formats or abbreviations.

For example, the same country may have multiple representations.

Before analysis, these values should be standardized so that the same country is consistently represented.

This prevents one country from being treated as multiple categories in analysis.

---

## Customer Support Ticket Exercise

The final exercise applies the cleaning techniques to a customer support ticket dataset.

The cleaning process includes:

1. Finding duplicate records
2. Checking for blank cells
3. Fixing inconsistent casing
4. Removing hidden spaces
5. Standardizing country names
6. Removing duplicates
7. Verifying the cleaned dataset with `COUNTBLANK`

---

## Why This Matters for Data Analysis

Data cleaning is important because analysis depends on the quality of the data.

Duplicates can inflate counts.

Blank cells can create incomplete analysis.

Inconsistent text can split one category into multiple categories.

Hidden spaces can cause matching and lookup problems.

Cleaning the data before analysis helps make Pivot Tables, formulas, dashboards, and other analysis more reliable.

---

## Skills Practiced

* Identifying duplicates
* Removing duplicates
* Concatenating columns
* `COUNTIF`
* `COUNTBLANK`
* `UPPER`
* `LOWER`
* `PROPER`
* `TRIM`
* `LEN`
* Standardizing text
* Cleaning customer support data

---

## Key Takeaways

* Always check data quality before analyzing data.
* Duplicates can produce incorrect results.
* `COUNTBLANK` helps identify missing values.
* `UPPER`, `LOWER`, and `PROPER` standardize text casing.
* `TRIM` removes unnecessary spaces.
* `LEN` can help identify hidden spaces.
* Consistent country and category names make analysis more reliable.
* Always verify the dataset after cleaning.

---

## Reflection

Today I learned that data cleaning is an important step before analysis. I practiced identifying duplicates, missing values, inconsistent text, hidden spaces, and inconsistent country names. I also learned how Excel functions such as `COUNTBLANK`, `TRIM`, `LEN`, `UPPER`, `LOWER`, and `PROPER` can help clean a dataset.

---

## Files

```text
Day-19-Data-Cleaning/
├── README.md
└── day-19-practice.xlsx
```

## Learning Resource

30 Day Excel Challenge by SDW Online.
