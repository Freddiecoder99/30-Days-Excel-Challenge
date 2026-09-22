<img width="826" height="479" alt="image" src="https://github.com/user-attachments/assets/130070a1-b0f4-4d64-a29c-8bb3343ec179" />

# Day 22: Data Visualisation (Part 2)

## Overview

Today I learned how to create dashboards that communicate information clearly instead of simply decorating the data.

The focus was on:

* Understanding what makes a good dashboard
* Keeping dashboards clear and simple
* Using the data-ink ratio
* Writing descriptive chart titles
* Choosing the right chart for the data
* Creating a logical dashboard layout
* Identifying problems with poorly designed dashboards
* Building scorecards
* Using INDEX MATCH in dashboard calculations
* Building retention, adoption, bug, and feedback charts

Good data visualization is important because the purpose of a dashboard is to help people understand information and make decisions quickly.

## What I Learned

# Dashboards That Communicate

A dashboard should communicate useful information clearly.

The goal is not to add as many charts, colours, shapes, or visual elements as possible.

A good dashboard should help the user quickly understand:

* What is happening?
* What is important?
* What has changed?
* Where should attention be focused?

The visual design should support the data rather than distract from it.

---

# Principle 1: Keep It Clear and Simple

One of the key principles from today's lesson is to keep dashboards simple.

Too many visual elements can make a dashboard difficult to understand.

A dashboard can contain unnecessary:

* Colours
* Borders
* Shapes
* Decorations
* Labels
* Gridlines
* Effects

These can distract from the actual information.

The goal is to remove unnecessary elements and allow the important data to stand out.

---

# Data-Ink Ratio

The **data-ink ratio** is the idea that a visualization should use as much of its visual space as possible to communicate useful data.

In simple terms:

> Remove visual elements that do not help communicate the data.

For example, unnecessary decoration can be removed so that attention is focused on:

* Metrics
* Trends
* Comparisons
* Important changes

This helps make dashboards cleaner and easier to understand.

---

# Principle 2: Write Descriptive Chart Titles

Chart titles should clearly explain what the chart is showing.

A vague title such as:

```text
Sales
```

does not tell the viewer much.

A more descriptive title might explain:

* What is being measured
* Which period is being analyzed
* What comparison is being made

A good chart title should allow the viewer to understand the purpose of the chart without needing to study the entire visualization first.

---

# Bad vs Good Chart Titles

### Bad title

```text
Retention
```

This is too general.

### Better title

```text
Customer Retention Rate by Quarter
```

The second title provides more context and tells the viewer what is being measured.

Descriptive titles reduce the amount of interpretation required from the audience.

---

# Principle 3: Use the Right Chart for Your Data

Different charts communicate different types of information.

The chart should match the question being answered.

For example:

### Comparison

Bar or column charts can be useful for comparing categories.

### Trends

Line charts can be useful for showing changes over time.

### Distribution

Charts can be used to show how values are distributed across categories.

### Proportions

Charts can be used when the goal is to communicate parts of a whole.

The important principle is:

> Choose the chart based on the data and the message you want to communicate.

---

# Principle 4: Follow a Logical Layout

A dashboard should have a clear visual structure.

Important information should be easy to find.

A common layout can be:

```text
Dashboard Title
       ↓
Key Metrics / Scorecards
       ↓
Main Charts
       ↓
Supporting Charts / Details
```

The layout should guide the viewer through the information logically.

The most important metrics should not be hidden at the bottom of the dashboard.

---

# Bad Dashboard Example

Today's lesson also looked at an example of a poorly designed dashboard.

Problems with a bad dashboard can include:

* Too much decoration
* Poor layout
* Unclear chart titles
* Too many charts
* Inappropriate chart types
* Too much visual clutter
* Important information being difficult to find

The purpose of reviewing a bad dashboard is to understand what should be avoided when designing our own dashboards.

---

# Designing the Dashboard Layout

Before creating the charts, the dashboard layout should be planned.

The layout should consider:

* Dashboard title
* Key scorecards
* Main visualizations
* Supporting information
* Space between sections
* Logical reading order

Planning the layout first helps prevent the dashboard from becoming cluttered.

---

# Building Scorecards

Scorecards display important metrics in a simple format.

For example:

```text
Retention Rate
     82%
```

or:

```text
New Users
    1,250
```

Scorecards allow users to see important numbers immediately without having to interpret a chart.

They are particularly useful for KPIs and summary metrics.

---

# Using INDEX MATCH in the Dashboard

Today's dashboard uses `INDEX MATCH` to retrieve information for the scorecards.

The general structure is:

```excel
=INDEX(return_range,MATCH(lookup_value,lookup_range,0))
```

`MATCH` finds the position of the value.

`INDEX` returns the value from that position.

Together, they allow the dashboard to dynamically retrieve the required information.

This connects today's dashboard work with the lookup skills learned earlier in the challenge.

---

# Dashboard Charts

The dashboard includes several charts focused on product and customer information.

The charts cover:

* Retention rate
* Adoption
* Bugs
* Feedback

Each visualization should communicate a specific aspect of the data.

The charts should also follow the visualization principles from today's lesson:

* Keep them clear
* Use descriptive titles
* Choose appropriate chart types
* Avoid unnecessary decoration
* Place them logically on the dashboard

---

# Retention Rate Chart

The retention rate visualization communicates how well customers are being retained.

The chart should make it easy to understand changes in retention over the relevant periods.

A clear title should explain what is being measured rather than simply using a generic title such as:

```text
Retention
```

---

# Adoption Chart

The adoption chart communicates how customers or users are adopting the product or feature.

The visualization should make comparisons or patterns easy to identify.

The chart type should be selected based on the structure of the data.

---

# Bugs Chart

The bugs visualization communicates information about product bugs.

The goal is to make it easy to identify patterns or differences in the bug data.

The visualization should focus attention on the information that matters rather than unnecessary design elements.

---

# Feedback Chart

The feedback chart communicates information collected from customers or users.

This allows feedback data to be presented visually rather than requiring users to examine raw records.

As with the other charts, the title and chart type should clearly communicate the information being presented.

---

# Why This Matters for Data Analysis

Data visualization is not simply about making spreadsheets look attractive.

The purpose of visualization is to communicate information.

A well-designed dashboard can help a business quickly understand:

* Key performance indicators
* Trends
* Problems
* Customer behaviour
* Product performance
* Areas that require attention

Poor visualization can make correct data difficult to understand.

Good visualization makes the important information easier to see.

---

# Skills Practiced

Today I practiced:

* Dashboard design
* Data visualization principles
* Data-ink ratio
* Writing descriptive chart titles
* Choosing appropriate chart types
* Dashboard layout
* Creating scorecards
* Using INDEX MATCH
* Building retention charts
* Building adoption charts
* Building bug charts
* Building feedback charts

---

# Key Takeaways

1. A dashboard should communicate information, not simply decorate data.
2. Keep dashboards clear and simple.
3. Remove unnecessary visual elements.
4. Use the data-ink ratio to focus attention on useful information.
5. Chart titles should clearly describe what the visualization shows.
6. Choose the chart type based on the data and the question being answered.
7. Use a logical layout so users can easily navigate the dashboard.
8. Scorecards are useful for displaying important KPIs.
9. INDEX MATCH can be used to retrieve information for dashboard metrics.
10. Good visualization helps people understand data and make decisions.

---

# Reflection

Today I learned that creating a dashboard is not just about adding charts to a worksheet.

A good dashboard needs to communicate information clearly.

I learned how simplicity, descriptive titles, appropriate chart selection, and logical layout can make a dashboard easier to understand.

I also practiced using INDEX MATCH to support dashboard scorecards and created visualizations for retention, adoption, bugs, and feedback.

---

# Files

* `day-22-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
