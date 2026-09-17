# Day 17: INDEX + MATCH

## Overview

Today I learned about INDEX and MATCH, two Excel functions that can be combined to create more flexible lookup solutions.

In Day 16, I learned VLOOKUP and HLOOKUP.

While those functions are useful, they have limitations because they depend heavily on the structure and position of columns.

INDEX and MATCH overcome some of these limitations by separating:

* Finding where a value is located
* Returning the value from that location

This makes them powerful tools for more advanced Excel analysis.

---

# What I Learned

## The Supermarket Analogy

The easiest way to understand INDEX and MATCH is to think about a supermarket.

### MATCH

MATCH answers:

> "Where is this item located?"

Example:

You ask:

"Which shelf contains milk?"

MATCH finds the position.

### INDEX

INDEX answers:

> "What is stored in this position?"

Example:

You go to that shelf and retrieve the item.

Together:

MATCH finds the location.

INDEX retrieves the information.

---

# INDEX Function

The INDEX function returns a value from a specific position in a range.

## INDEX Syntax

```excel
=INDEX(array, row_num, [column_num])
```

### array

The range containing the data.

### row_num

The row position of the value to return.

### column_num

The column position when working with multiple columns.

## Example

If a list contains:

| Row | Product |
| --- | ------- |
| 1   | Laptop  |
| 2   | Tablet  |
| 3   | Monitor |

Formula:

```excel
=INDEX(A2:A4,2)
```

returns:

```text
Tablet
```

because Tablet is in position 2.

---

# MATCH Function

MATCH finds the position of a value inside a range.

## MATCH Syntax

```excel
=MATCH(lookup_value, lookup_array, match_type)
```

### lookup_value

The value being searched for.

### lookup_array

The range where Excel searches.

### match_type

Determines the type of match.

For exact matches:

```excel
0
```

is commonly used.

## Example

Formula:

```excel
=MATCH("Tablet",A2:A4,0)
```

returns:

```text
2
```

because Tablet is the second item in the list.

---

# Combining INDEX and MATCH

INDEX and MATCH become powerful when combined.

The workflow is:

```text
Find the position
        ↓
MATCH
        ↓
Return the value
        ↓
INDEX
```

Example:

```excel
=INDEX(C2:C10,MATCH(A2,A2:A10,0))
```

This allows Excel to:

1. Find the matching record.
2. Identify its position.
3. Return information from another column.

---

# Why INDEX + MATCH is Useful

Compared with VLOOKUP, INDEX + MATCH provides more flexibility.

Advantages:

* Can look left or right
* Does not depend on column position
* More adaptable when tables change
* Allows more complex lookup solutions

---

# IT Assets and Security Rules Exercise

Today's exercise used an IT asset management dataset.

The goal was to create a lookup system that could retrieve information about company assets.

The dataset included information such as:

* Employee details
* Department
* Asset ID
* Laptop model
* Security policies
* Login rules

---

# Pulling Department Information

INDEX + MATCH was used to retrieve department information based on an employee or asset identifier.

The lookup process:

Input:

```text
Employee ID
```

↓

MATCH finds the correct row.

↓

INDEX returns:

```text
Department
```

---

# Pulling Asset Information

The lookup dashboard was used to retrieve:

* Asset ID
* Department
* Security policies
* Laptop information

This demonstrated how Excel can act as a simple information retrieval system.

---

# Nested INDEX MATCH

A nested INDEX MATCH formula was used to retrieve laptop information from multiple criteria.

This approach allows Excel to handle more complex lookup requirements.

Example scenario:

Find:

```text
Employee
+
Asset
```

Return:

```text
Laptop Model
```

This is useful when one lookup condition is not enough.

---

# Maximum Login Attempts

INDEX MATCH was also used to retrieve security information such as maximum login attempts.

Example:

Input:

```text
Laptop Model
```

Return:

```text
Maximum Login Attempts
```

This demonstrates how lookup formulas can retrieve security and configuration information.

---

# Dynamic Lookup Dashboard

A dropdown list was added to make the lookup tool interactive.

Instead of manually entering values, users can select an option from a list.

The process:

```text
Dropdown Selection
        ↓
MATCH finds position
        ↓
INDEX returns information
        ↓
Dashboard updates
```

This creates a user-friendly lookup tool.

---

# Why This Matters for Data Analysis

Analysts often work with information stored across multiple tables.

Examples:

## Employees

Employee ID → Employee details

## Inventory

Asset ID → Equipment information

## Sales

Product ID → Product information

## Customers

Customer ID → Customer details

INDEX + MATCH helps combine information from separate sources.

---

# Skills Practiced

Today I practiced:

* Understanding INDEX
* Understanding MATCH
* Combining INDEX and MATCH
* Creating flexible lookup formulas
* Retrieving information from datasets
* Building dynamic lookup dashboards
* Using dropdown selections with lookup formulas

---

# Key Takeaways

1. MATCH finds the position of a value.
2. INDEX returns information from a position.
3. Together they create powerful lookup solutions.
4. INDEX + MATCH is more flexible than traditional VLOOKUP.
5. Lookup skills help prepare for working with multiple database tables.
6. Dynamic dashboards can be created using dropdowns and formulas.

---

# Reflection

Today was a major step forward in understanding how Excel handles relationships between datasets.

VLOOKUP introduced the idea of retrieving information from another table.

INDEX + MATCH showed me how to create more flexible solutions where the lookup logic and return value are separated.

This way of thinking is very similar to how data is combined in databases using SQL joins.

---

# Files

* `day-17-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
