# Day 15: Conditional Formatting Part 2

## Overview

Today I continued learning conditional formatting and moved from basic visual highlighting into more practical data analysis use cases.

The focus was on using conditional formatting to automatically identify important records, exceptions, trends, and potential problems in a dataset.

I learned how conditional formatting can work together with formulas, Pivot Tables, and business rules to make important information stand out automatically.

## What I Learned

### Highlighting Orders by Status

Conditional formatting can be used to identify records based on their status.

For example:

* Cancelled orders
* Pending orders
* Completed orders

This allows important order statuses to be identified quickly without manually scanning every row.

### Flagging Weekend Orders

I learned how to use the `WEEKDAY` function together with conditional formatting to identify orders placed on weekends.

The `WEEKDAY` function returns a number representing the day of the week.

For example, a formula can be used to determine whether an order date falls on a Saturday or Sunday.

This demonstrates how formulas can be combined with conditional formatting to create more useful business rules.

### Top 10% Revenue Products

I used a Pivot Table to summarize revenue by product and then applied conditional formatting to identify the top 10% of products by revenue.

This makes it easier to identify the products contributing the most revenue.

### Colour Scales

Colour scales were used to visually compare performance from highest to lowest.

A colour scale can make patterns easier to identify because the formatting changes according to the value.

For example:

* Strong performers can be highlighted differently from
* Average performers and
* Lower performers

This provides a quick visual overview of performance.

### Icon Sets

I used icon sets to create a traffic-light style indicator for profit margins.

The icons provide a quick way to classify performance levels.

For example:

* Green = stronger performance
* Yellow = moderate performance
* Red = weaker performance

The exact thresholds depend on the business rule being applied.

### Flagging Late Orders

I learned how conditional formatting can use a formula containing multiple conditions.

This can be used to identify orders that meet more than one requirement.

For example, an order might be flagged when:

* The order is late, and
* The order has not been completed.

This is more powerful than applying a simple formatting rule to one column.

### Flagging High Profit Margin Outliers

Conditional formatting was also used to identify unusually high profit margins.

This can help an analyst investigate values that may represent:

* Exceptional performance
* Data-entry errors
* Unusual transactions
* Potential outliers

An important lesson is that an outlier should be investigated rather than automatically assumed to be an error.

## Why This Matters for Data Analysis

Conditional formatting can turn a large table into a visual monitoring tool.

Instead of manually searching for important records, an analyst can create rules that automatically highlight them.

Examples include:

* Late orders
* Cancelled orders
* Pending orders
* High-revenue products
* Low-performing products
* High-profit transactions
* Weekend activity
* Potential outliers

This makes conditional formatting useful for both analysis and reporting.

## Skills Practiced

Today I practiced:

* Highlighting records based on status
* Using formulas with conditional formatting
* Using `WEEKDAY`
* Identifying weekend orders
* Highlighting the top 10% of values
* Applying colour scales
* Applying icon sets
* Creating traffic-light indicators
* Using multiple conditions
* Identifying potential outliers
* Combining Pivot Tables with conditional formatting

## Business Rules

The main idea behind today's exercises was to convert business requirements into Excel rules.

For example:

| Business Requirement      | Excel Approach                         |
| ------------------------- | -------------------------------------- |
| Find cancelled orders     | Conditional formatting based on status |
| Find pending orders       | Conditional formatting based on status |
| Find weekend orders       | `WEEKDAY` formula                      |
| Find top revenue products | Pivot Table + Top 10%                  |
| Compare performance       | Colour scale                           |
| Monitor profit margins    | Icon set                               |
| Find late orders          | Multiple-condition formula             |
| Find unusual margins      | Conditional formatting                 |

## Key Takeaways

1. Conditional formatting can be used for analysis, not just decoration.
2. Formulas can make conditional formatting much more powerful.
3. Business rules can be translated into Excel conditions.
4. Colour scales help compare values quickly.
5. Icon sets can communicate performance levels.
6. Conditional formatting can help identify potential outliers.
7. Pivot Tables and conditional formatting can work together to highlight important results.

## Reflection

Today's lesson changed the way I think about conditional formatting.

Previously, I mainly viewed it as a way to make important numbers stand out.

Now I understand that it can be used to create automated flags based on business rules.

For example, instead of manually checking every order to find late deliveries, I can create a rule that identifies them automatically.

This makes Excel much more useful as a monitoring and decision-support tool.

## Files

* `day-15-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
