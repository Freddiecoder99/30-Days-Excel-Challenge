# Day 8: Logical Functions

## Overview

Today I learned how Excel can make decisions automatically using logical functions.

Logical functions allow Excel to evaluate whether a condition is true or false and return different results depending on the outcome.

These functions are important because they allow analysts to create rules, categories, and decision-making logic inside a dataset.

## What I Learned

## TRUE and FALSE Logic

Excel logical functions work by evaluating conditions.

A condition can result in:

* TRUE
* FALSE

Example:

```excel
=A1>100
```

If A1 is greater than 100, Excel returns TRUE.

If not, it returns FALSE.

## IF Function

The IF function allows Excel to return one value when a condition is true and another value when the condition is false.

Structure:

```excel
=IF(condition, value_if_true, value_if_false)
```

Example:

```excel
=IF(B2>=50,"Pass","Fail")
```

This checks whether B2 is greater than or equal to 50.

If true:

Pass

If false:

Fail

## Nested IF Statements

Multiple IF statements can be combined to create multiple conditions.

Example:

```excel
=IF(A2>=80,"High",IF(A2>=50,"Medium","Low"))
```

This allows Excel to categorize values into different groups.

## AND Function

The AND function checks whether multiple conditions are true at the same time.

Example:

```excel
=AND(B2>=50,C2="Yes")
```

The result is TRUE only when both conditions are satisfied.

## OR Function

The OR function checks whether at least one condition is true.

Example:

```excel
=OR(B2>=50,C2="Yes")
```

The result is TRUE if either condition is satisfied.

## NOT Function

The NOT function reverses a logical value.

Example:

```excel
=NOT(A2="Completed")
```

This returns TRUE when the value is not Completed.

## Why This Matters for Data Analysis

Logical functions allow analysts to create categories and identify important records automatically.

Examples:

* Flagging overspending departments
* Identifying profitable products
* Categorizing customers
* Creating performance ratings
* Highlighting missing information

## Practice

Today I practiced:

* Creating IF statements
* Combining conditions using AND
* Combining conditions using OR
* Creating categories using logical rules
* Building automatic flags

## Key Takeaways

1. Logical functions allow Excel to make decisions.
2. IF is one of the most important Excel functions.
3. AND requires all conditions to be true.
4. OR requires at least one condition to be true.
5. Logical functions help automate analysis.

## Reflection

Today I learned that Excel can do more than calculate numbers.

Logical functions allow spreadsheets to behave more like decision-making tools by automatically classifying information based on rules.

## Files

* `day-08-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
