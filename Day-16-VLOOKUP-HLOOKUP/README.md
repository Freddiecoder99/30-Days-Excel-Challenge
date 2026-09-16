# Day 16: VLOOKUP and HLOOKUP

## Overview

Today I learned about Excel lookup functions and how they can be used to retrieve information from different tables.

The focus was on:

* Understanding how lookups work
* Using VLOOKUP to search vertically
* Using HLOOKUP to search horizontally
* Building a dynamic lookup dashboard
* Combining lookups with dropdown lists

Lookup functions are important because real-world datasets are often stored across multiple tables.

## What I Learned

# What are Lookup Functions?

Lookup functions allow Excel to search for a value in one location and return related information from another location.

Example:

A company may have:

Employee ID | Department

Instead of manually searching for each employee, Excel can automatically return the department when given the Employee ID.

## VLOOKUP

VLOOKUP stands for:

**Vertical Lookup**

It searches for a value down the first column of a table and returns information from another column in the same row.

## VLOOKUP Syntax

Structure:

```excel
=VLOOKUP(lookup_value, table_array, col_index_num, range_lookup)
```

### lookup_value

The value Excel searches for.

Example:

Employee ID

### table_array

The range containing the lookup data.

Example:

Employee information table.

### col_index_num

The column number containing the result to return.

Example:

Department may be in column 3.

### range_lookup

Determines whether the match should be:

TRUE:

Approximate match

FALSE:

Exact match

For most business data, exact matches are commonly used.

Example:

```excel
=VLOOKUP(A2,Employees!A:D,4,FALSE)
```

This searches for the value in A2 and returns information from column 4.

---

# VLOOKUP Example

In today's exercise, I used VLOOKUP to answer questions such as:

* Which department does an employee belong to?
* Which laptop model matches an asset ID?

Instead of manually searching through hundreds of records, Excel retrieves the information automatically.

---

# IT Assets and Security Rules Exercise

The project involved an IT asset management scenario.

The dataset contained information such as:

* Asset ID
* Laptop model
* Employee information
* Security rules
* Access permissions

The goal was to build a lookup dashboard that could quickly retrieve information about company assets.

---

# Lookup Dashboard

A lookup dashboard was created to allow users to search for information without manually browsing large tables.

The dashboard included:

* Search inputs
* Retrieved information
* Dynamic lookup results

This demonstrates how Excel can be used to build simple reporting tools.

---

# Finding Laptop Model Using VLOOKUP

A VLOOKUP formula was used to search for an Asset ID and return the corresponding laptop model.

Example:

Input:

```
Asset ID
```

Output:

```
Laptop Model
```

This type of lookup is useful in real business situations such as:

* Asset tracking
* Inventory management
* Employee records

---

# HLOOKUP

HLOOKUP stands for:

**Horizontal Lookup**

Unlike VLOOKUP, which searches vertically, HLOOKUP searches across the top row of a table.

It is useful when data is arranged horizontally.

## HLOOKUP Syntax

Structure:

```excel
=HLOOKUP(lookup_value, table_array, row_index_num, range_lookup)
```

### lookup_value

The value to search for.

### table_array

The horizontal table containing the information.

### row_index_num

The row number containing the result.

### range_lookup

Determines exact or approximate matching.

---

# HLOOKUP Example

In the exercise, HLOOKUP was used to find VPN access permissions based on laptop model.

Example:

Input:

```
Laptop Model
```

Output:

```
VPN Access Permission
```

This demonstrated how lookup functions can retrieve related information from different layouts.

---

# Dynamic Lookup Dashboard

A dropdown list was added to make the lookup dashboard interactive.

Instead of typing values manually, users can select an option from a list.

The workflow becomes:

```
Dropdown Selection
        ↓
Lookup Formula
        ↓
Retrieved Information
        ↓
Dashboard Result
```

This creates a more user-friendly reporting tool.

---

# Why This Matters for Data Analysis

Lookup functions are essential because business data is often separated into different tables.

Examples:

### Human Resources

Employee ID → Employee details

### Sales

Product ID → Product information

### Inventory

Asset ID → Equipment details

### Finance

Account number → Account information

Lookups allow analysts to combine information without manually copying data.

---

# Skills Practiced

Today I practiced:

* Understanding lookup functions
* Writing VLOOKUP formulas
* Understanding VLOOKUP arguments
* Using exact matches
* Retrieving information from another table
* Using HLOOKUP
* Building lookup dashboards
* Creating dropdown-driven searches

---

# Key Takeaways

1. VLOOKUP searches vertically through a table.
2. HLOOKUP searches horizontally through a table.
3. Lookup functions connect information from different datasets.
4. Exact matches are usually safer for business data.
5. Dropdowns can make lookup tools easier for users.
6. Lookup skills are important before learning database joins in SQL.

---

# Reflection

Today was an important step because I learned how Excel can connect separate datasets.

Previously, I mainly analyzed information that already existed in one table.

Lookup functions showed me how analysts combine information from different sources to answer business questions.

This is also a concept that connects directly to SQL, where tables are joined together to create complete datasets.

---

# Files

* `day-16-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
