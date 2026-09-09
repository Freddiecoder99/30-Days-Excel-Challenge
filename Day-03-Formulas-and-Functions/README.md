# Day 3: Formulas and Functions

## Overview

Today I started using Excel to perform calculations.

This was an important step because formulas and functions allow Excel to turn stored data into useful information.

## What I Learned

### Formulas

An Excel formula normally begins with an equals sign.

Example:

`=A2+B2`

Excel calculates the result using the values stored in the referenced cells.

Another example:

`=C2*D2`

could be used to calculate quantity multiplied by price.

### SUM

SUM adds values together.

Example:

`=SUM(B2:B10)`

This adds all numeric values between B2 and B10.

### AVERAGE

AVERAGE calculates the arithmetic mean.

Example:

`=AVERAGE(B2:B10)`

### MAX

MAX returns the largest numeric value.

Example:

`=MAX(B2:B10)`

### MIN

MIN returns the smallest numeric value.

Example:

`=MIN(B2:B10)`

### COUNT

COUNT returns the number of cells containing numeric values.

Example:

`=COUNT(B2:B10)`

### Relative Cell References

A relative reference changes when a formula is copied.

For example:

`=B2*C2`

When copied down one row, Excel changes it to:

`=B3*C3`

This is useful when performing the same calculation for many rows.

### Absolute Cell References

An absolute reference stays fixed when a formula is copied.

Example:

`=$B$1`

If B1 contains a tax rate and I want every row to use the same rate, I can use:

`=C2*$B$1`

When copied down, `$B$1` remains unchanged.

### Autofill

Instead of typing the same formula repeatedly, Excel allows formulas to be copied into additional rows.

This saves time when working with larger datasets.

### Common Formula Errors

I also learned that errors can help identify problems in formulas.

Examples include:

`#DIV/0!`

This usually appears when dividing by zero.

`#VALUE!`

This can appear when Excel receives the wrong type of value for a calculation.

`#NAME?`

This often means Excel does not recognize part of the formula.

`#REF!`

This means the formula contains an invalid cell reference.

## Why This Matters for Data Analysis

Formulas allow an analyst to calculate:

* Totals
* Averages
* Minimum values
* Maximum values
* Counts
* Differences
* Percentages

Instead of manually calculating values, Excel can perform calculations automatically and update them when the underlying data changes.

## Practice

Today I practiced:

* Writing formulas
* Using SUM
* Using AVERAGE
* Using MAX
* Using MIN
* Using COUNT
* Copying formulas
* Using relative references
* Using absolute references
* Identifying formula errors

## Key Takeaways

1. Excel formulas begin with `=`.
2. Functions are predefined calculations.
3. Relative references change when copied.
4. Absolute references remain fixed.
5. Formula errors should be investigated rather than ignored.

## Reflection

Today felt like the point where Excel started becoming a real analysis tool.

I now understand that formulas let me take raw values and calculate new information from them.

The difference between relative and absolute references was especially important because it affects what happens when formulas are copied.

## Files

* `Day03_Practice_Challenge.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
