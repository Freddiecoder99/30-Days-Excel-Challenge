# Day 9: Text Functions

## Overview

Today I learned how Excel can manipulate and clean text data using text functions.

Text functions are especially useful when working with real-world datasets because information is often inconsistent or combined together.

Examples include:

* Names
* Addresses
* Product codes
* Categories
* IDs

## What I Learned

## LEFT Function

The LEFT function extracts characters from the beginning of text.

Example:

```excel
=LEFT(A2,5)
```
This extracts the first five characters from A2.

### In other instances for example Working with names of any length(Splitting Names - First and Last name):

First Name Formula

```excel
=LEFT(B2, FIND(" ", B2)-1)
```
How it works:

* FIND(" ", B2) = locates the space position
* LEFT() = extracts characters from the left
* "-1" = stops before the space

Example: "Kevin Robertson" → "Kevin"

## RIGHT Function

The RIGHT function extracts characters from the end of text.

Example:

```excel
=RIGHT(A2,4)
```

This extracts the last four characters.

### When extracting Last name and Working with names of any length

Last Name Formula

```excel
=RIGHT(B2, LEN(B2)-FIND(" ", B2))
```

How it works:

* FIND(" ", B2) = locates the space position
* LEN(B2) = total length of the name
* RIGHT() = extracts characters from the right
* Calculates characters after the space

Example: "Kevin Robertson" → "Robertson"

## MID Function

The MID function extracts characters from the middle of text.

Example:

```excel
=MID(A2,3,5)
```

This starts at the third character and extracts five characters.

## LEN Function

The LEN function counts the number of characters in a text value.

Example:

```excel
=LEN(A2)
```

This can help identify inconsistencies in text length.

## TRIM Function

TRIM removes unnecessary spaces from text.

Example:

```excel
=TRIM(A2)
```

This is useful when cleaning messy datasets.

## CONCATENATE / CONCAT

These functions combine multiple pieces of text.

Example:

```excel
=CONCAT(A2," ",B2)
```

This can combine first and last names.

## TEXT Function

The TEXT function changes how numbers appear as text.

Example:

```excel
=TEXT(A2,"mmmm")
```

This can display a date as a month name.

## Why This Matters for Data Analysis

Real-world data is often messy.

Text functions help analysts:

* Clean inconsistent values
* Separate information
* Combine columns
* Standardize formats
* Prepare data for analysis

## Practice

Today I practiced:

* Extracting characters
* Combining text
* Removing unnecessary spaces
* Counting characters
* Formatting text values

## Key Takeaways

1. Text functions help clean and transform data.
2. Clean data produces better analysis.
3. Small formatting problems can create large analytical problems.
4. Text manipulation is an important data preparation skill.

## Reflection

Today I realized that data analysis does not begin with charts or formulas.

Before analysis can happen, data often needs to be cleaned and standardized.

Text functions provide useful tools for preparing messy datasets.

## Files

* `day-09-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
