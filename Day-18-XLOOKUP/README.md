# Day 18: XLOOKUP

## Overview

Today I learned about XLOOKUP, a modern Excel lookup function designed to make searching and retrieving information easier and more flexible.

Before learning XLOOKUP, I worked with:

* VLOOKUP
* HLOOKUP
* INDEX + MATCH

These functions are useful, but each has limitations.

XLOOKUP provides a more flexible way to search for a value and return related information.

Today's lesson focused on understanding those limitations and learning how XLOOKUP can solve many of them.

---

# Problems with Earlier Lookup Methods

## VLOOKUP

VLOOKUP works well for many simple lookups, but it has limitations.

For example:

* The lookup column normally needs to be on the left.
* The return column is identified using a column number.
* Changes to the table structure can cause problems.
* It is primarily designed for vertical lookups.

## HLOOKUP

HLOOKUP is useful when data is arranged horizontally, but it has similar structural limitations.

## INDEX + MATCH

INDEX + MATCH is much more flexible and powerful, but the formula can be more complicated because two functions must be combined.

XLOOKUP provides a simpler way to perform many of these tasks.

---

# XLOOKUP

XLOOKUP searches for a value in one range and returns a corresponding value from another range.

## Basic Syntax

```excel
=XLOOKUP(lookup_value, lookup_array, return_array)
```

There are additional optional arguments that can be used to control error handling and matching behavior.

## Main Arguments

### lookup_value

The value I want Excel to search for.

Example:

```text
Employee ID
```

### lookup_array

The range where Excel should search for the lookup value.

Example:

```text
Employee ID column
```

### return_array

The range containing the information I want returned.

Example:

```text
Department column
```

---

# Basic XLOOKUP Example

Suppose I have:

| Employee ID | Employee Name | Department |
| ----------- | ------------- | ---------- |
| E001        | John          | IT         |
| E002        | Mary          | Finance    |
| E003        | Peter         | HR         |

If I enter:

```text
E002
```

and want Excel to return the department, I can use:

```excel
=XLOOKUP(A2,A5:A7,C5:C7)
```

Excel searches for the Employee ID and returns the corresponding department.

---

# Finding a Department by Employee ID

In today's demonstration, I used XLOOKUP to retrieve a department from an Employee ID.

The workflow was:

```text
Employee ID
      ↓
XLOOKUP
      ↓
Department
```

This is similar to the lookup I performed using VLOOKUP and INDEX + MATCH, but the XLOOKUP formula is simpler.

---

# Searching in Reverse

One important feature of XLOOKUP is that it can search in either direction.

For example, I can search for an employee's name based on a department or another related value, depending on how the data is structured.

This avoids one of the major limitations of VLOOKUP, where the lookup column generally needs to appear before the return column.

---

# Custom Error Messages

XLOOKUP can return a custom message when a matching value cannot be found.

The syntax can include an `if_not_found` argument.

Example:

```excel
=XLOOKUP(A2,A5:A20,B5:B20,"Not Found")
```

If the value doesn't exist, Excel returns:

```text
Not Found
```

instead of an error such as `#N/A`.

This creates a better user experience in reports and dashboards.

---

# Two-Way XLOOKUP

XLOOKUP can also be used for two-dimensional lookups.

This means I can search across:

* Rows
* Columns

to find a value at the intersection of two criteria.

For example:

```text
Product + Region
       ↓
Required value
```

This is useful when information is stored in matrix-style tables.

---

# Nested XLOOKUP

Two XLOOKUP functions can be combined to perform a more advanced matrix lookup.

The basic idea is:

```text
First XLOOKUP
      ↓
Find the correct row or column
      ↓
Second XLOOKUP
      ↓
Return the required value
```

This makes XLOOKUP suitable for more complex lookup scenarios.

---

# IT Assets Exercise

Today's exercise continued using the IT assets and security dataset from Days 16 and 17.

The purpose was to use XLOOKUP to build a more flexible lookup dashboard.

The dashboard was used to retrieve information about employees, devices, and security requirements.

---

# Lookup Dashboard

The lookup dashboard allows the user to provide a value and retrieve related information automatically.

Examples include:

* Employee information
* Department
* Asset information
* Laptop model
* VPN access
* Salary band
* Security-related information

A dropdown can also be used to make the lookup dynamic.

The basic workflow is:

```text
User Selection
      ↓
XLOOKUP
      ↓
Retrieved Information
      ↓
Dashboard
```

---

# Salary Band Lookup

XLOOKUP was used to retrieve the appropriate salary band based on the selected employee or related information.

This demonstrates how lookup functions can support HR and organizational reporting.

---

# VPN Access Lookup

The IT asset dataset was also used to retrieve VPN access information.

Example:

```text
Laptop Model
      ↓
XLOOKUP
      ↓
VPN Access
```

This can be useful in an IT asset and security management report.

---

# Dynamic Dropdown

A dropdown list was added to allow the user to select an item rather than manually typing it.

This made the lookup dashboard more interactive.

The workflow becomes:

```text
Dropdown
   ↓
Selected Employee / Asset
   ↓
XLOOKUP
   ↓
Department / Asset / Security Information
```

---

# Why This Matters for Data Analysis

Lookup functions are used when information is stored across different tables or when users need to retrieve related information quickly.

Examples include:

### HR

Employee ID → Department

### IT

Asset ID → Laptop Model

### Security

Laptop Model → VPN Access

### Finance

Employee → Salary Band

### Sales

Product ID → Product Details

XLOOKUP makes these tasks easier to build and maintain.

---

# Skills Practiced

Today I practiced:

* Understanding XLOOKUP
* Writing XLOOKUP formulas
* Understanding lookup and return arrays
* Returning custom error messages
* Searching in different directions
* Performing two-way lookups
* Using nested XLOOKUP
* Building dynamic lookup tools
* Using dropdowns with lookup formulas

---

# Key Takeaways

1. XLOOKUP is a flexible modern lookup function.
2. It separates the lookup array from the return array.
3. XLOOKUP can search in different directions.
4. XLOOKUP can return custom messages when values are not found.
5. It can be used for horizontal, vertical, and more complex lookups.
6. Nested XLOOKUP formulas can solve matrix-style lookup problems.
7. Dropdowns can make lookup dashboards interactive.
8. Lookup functions are important when information is stored across multiple datasets.

---

# Reflection

Today's lesson helped me understand why XLOOKUP is such a useful Excel skill.

VLOOKUP introduced me to retrieving information from another table.

INDEX + MATCH showed me how to create more flexible lookups.

XLOOKUP brought many of those capabilities together in a simpler formula structure.

The most useful part for me was learning how a lookup can be connected to a dropdown so that the spreadsheet behaves like a small interactive application.

---

# Files

* `day-18-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.

## Project Status

Completed
