# Day 24: Power Query (Part 2)

## Overview

Today I continued learning about Power Query and explored more advanced methods of importing, transforming, and combining data from different sources.

Power Query allows analysts to connect to external data sources, clean and transform the data, and combine multiple datasets before loading them into Excel.

Today I focused on importing data from websites, SQL databases, CSV files, folders containing multiple CSV files, and PDF documents.

I also learned how to create custom columns, merge columns, and use different types of joins to combine datasets.

## What I Learned

## Advanced Data Import

Power Query can connect to many different data sources.

Instead of manually copying and pasting data into Excel, Power Query can import the data directly and apply transformation steps.

This makes the data preparation process more efficient and repeatable.

## Importing From a Website

Power Query can extract structured data from websites.

This is useful when data is published online in tables.

Instead of manually copying the information, Power Query can connect to the website and import the data into Excel.

This can also make it easier to refresh the data when the source changes.

## Importing From a SQL Database

Power Query can connect directly to SQL databases.

This allows analysts to work with data stored in database systems without manually exporting everything into Excel.

SQL databases can contain large amounts of structured information, making database connections useful for data analysis and reporting.

## Importing CSV Files

CSV files are commonly used for storing tabular data.

Power Query can import CSV files and automatically detect:

- Columns
- Data types
- Headers
- Delimiters

The imported data can then be cleaned and transformed before being loaded into Excel.

## Importing From a Folder

Power Query can connect to an entire folder containing multiple CSV files.

Instead of importing each file individually, Power Query can combine the files into one dataset.

For example:

text
January.csv
February.csv
March.csv
April.csv
````

These files can be combined into one table.

This is especially useful when working with monthly, weekly, or daily datasets that follow the same structure.

## Importing From a PDF

Power Query can also extract structured data from PDF documents.

This can be useful when reports or tables are provided in PDF format.

Instead of manually retyping information, Power Query can identify available tables and import them for further transformation and analysis.

## Custom Columns

Power Query allows analysts to create custom columns using logical conditions.

One example is IF-ELSE logic.

For example:

text
If Sales > 10000
Then "High"
Else "Low"
````

This can be used to categorize or classify records based on specific conditions.

Custom columns are useful for creating new information from existing data.

## IF-ELSE Logic

IF-ELSE logic allows different results to be returned depending on whether a condition is met.

Example:

```text
If Age >= 18
Then "Adult"
Else "Minor"
```

This can help analysts create categories that are useful during analysis.

## Merging Columns

Power Query can combine information from multiple columns into a single column.

For example:

First Name:

```text
John
```

Last Name:

```text
Doe
```

These can be combined into:

```text
John Doe
```

This is useful when information is split across multiple columns but needs to be presented as one field.

## Joins

Joins are used to combine information from two datasets using a common column.

For example, two datasets might contain:

```text
Customer ID
```

The common ID can be used to match records between the datasets.

Joins are important because real-world data is often stored in separate tables.

Instead of keeping the datasets separate, Power Query can combine related information.

## Types of Joins

Power Query provides several types of joins.

### Inner Join

An inner join returns only records that exist in both datasets.

Example:

```text
RSVP List
+
Check-In Log
```

The result contains only people who appear in both lists.

This can be useful when identifying people who registered and also checked in.

### Left Join

A left join keeps all records from the first dataset and matches information from the second dataset where available.

Example:

```text
Waitlist
+
Accepted List
```

The result keeps everyone in the waitlist and adds matching information from the accepted list.

Records without a match are still retained.

### Right Join

A right join keeps all records from the second dataset and matches information from the first dataset.

Example:

```text
Payments
+
Invoices
```

This can be used to compare payment records against invoice records.

The join can help identify invoices that have matching payment information and records that do not.

### Outer Join

An outer join keeps all records from both datasets.

Example:

```text
Old Leads
+
New Leads
```

Records that exist in either dataset are retained.

This is useful when identifying both matching and unmatched records.

## Business Exercise: Combining Business Data

In today's exercises, I worked with multiple datasets and used Power Query to import, transform, and combine them.

The exercises demonstrated how Power Query can be used to solve common data preparation problems.

## Exercises Completed

### RSVP and Check-In Data

Used an inner join to identify records appearing in both an RSVP list and a check-in log.

### Waitlist and Accepted Data

Used a left join to keep all waitlisted records while bringing in matching information from the accepted list.

### Payments and Invoices

Used a right join to combine payment and invoice information and identify matching and unmatched records.

### Old and New Leads

Used an outer join to combine old and new lead datasets while retaining records from both sources.

### SQL Database Exercise

Imported and joined data directly from a SQL database.

This demonstrated how Power Query can combine database information with analytical workflows.

## Why This Matters for Data Analysis

Data analysts often work with information stored in different systems and file formats.

Power Query provides a way to bring these sources together and prepare them for analysis.

It can help analysts:

* Import data from multiple sources
* Combine datasets
* Automate repetitive preparation tasks
* Create calculated categories
* Reduce manual data entry
* Refresh data more easily
* Prepare data for reporting and visualization

Understanding joins is particularly important because business data is often distributed across multiple tables.

## Skills Practiced

Today I practiced:

* Importing data from websites
* Connecting to SQL databases
* Importing CSV files
* Combining multiple CSV files from a folder
* Importing data from PDFs
* Creating custom columns
* Using IF-ELSE logic
* Merging columns
* Performing inner joins
* Performing left joins
* Performing right joins
* Performing outer joins
* Combining data from multiple sources
* Preparing data for analysis

## Key Takeaways

1. Power Query can import data from many different sources.
2. Multiple CSV files can be combined automatically from a folder.
3. SQL databases can be connected directly to Power Query.
4. Custom columns can be created using logical conditions.
5. Columns can be merged to create new fields.
6. Joins are essential for combining related datasets.
7. Different joins produce different results depending on the analytical requirement.
8. Power Query can reduce repetitive manual data preparation.


## Files

* `day-24-practice.xlsx`

## Learning Resource

30 Day Excel Challenge by SDW Online.
