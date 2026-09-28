# Day 28: Building a Data-Entry Form

## Overview

Today I learned how to build a data-entry form in Excel and how controlled data entry can improve the quality and consistency of information collected.

Uncontrolled data entry can lead to spelling differences, missing information, invalid values, and inconsistent records.

The goal of today's exercise was to create a structured IT equipment request form that controls what users can enter and automatically records submitted requests.

I also learned how to use data validation, conditional formatting, macros, and buttons to create a more practical data-entry system.

## What I Learned

## Why Controlled Data Entry Matters

Uncontrolled data entry can cause problems when different users enter information in different formats.

For example:

```text
Laptop
laptop
LAPTOP
Lap top
````

These values may refer to the same item but could be treated as different categories during analysis.

Other common problems include:

* Missing information
* Invalid values
* Spelling differences
* Incorrect quantities
* Inconsistent categories
* Duplicate records

A controlled data-entry form helps reduce these problems before the information reaches the main dataset.

## Built-In Excel Form

Excel includes a built-in Form feature that can be used for entering records into a table.

The Form provides a structured way to add and review records without directly typing into the worksheet.

This can be useful for simple data-entry tasks.

In today's exercise, I also learned how a custom form can provide more control over the data-entry process.

## Business Scenario: IT Equipment Request Form

Today's main exercise involved building an IT equipment request form.

The form was designed to allow employees to request equipment in a controlled format.

For example, a request could include:

* Employee name
* Department
* Equipment type
* Quantity
* Request details
* Status

The form was connected to a request log where submitted requests were stored.

## Setting Up the Data Table

The first step was creating the main data table that would store the submitted requests.

The table acts as the central log for all requests.

A request log could contain fields such as:

```text
Request ID
Employee Name
Department
Equipment
Quantity
Request Date
Status
```

Keeping the information in a structured table makes it easier to manage, filter, and analyze later.

## Reference Lists

Reference lists were created to provide approved values for the form.

For example:

```text
Departments
Finance
HR
Marketing
IT
Operations
```

Another reference list could contain equipment types:

```text
Equipment
Laptop
Monitor
Keyboard
Mouse
Headset
```

These lists can be used with Data Validation to create controlled dropdown options.

## Data Validation

Data Validation was used to control what users can enter into the form.

Dropdown lists were created for fields where only specific options should be accepted.

For example:

```text
Department:
Finance
HR
Marketing
IT
Operations
```

This prevents users from manually typing different versions of the same category.

## Quantity Limits

Quantity fields were also controlled using Data Validation.

For example, a rule could restrict the quantity to a reasonable range:

```text
Minimum: 1
Maximum: 10
```

This prevents invalid quantities such as:

```text
0
-5
1000
```

from being entered accidentally.

## Designing the Form Layout

The form was designed to make data entry simple and easy to understand.

A clear form layout can separate:

```text
Employee Information
        ↓
Request Information
        ↓
Validation / Status
        ↓
Submit Request
```

Labels were added next to input cells so users know exactly what information is expected.

The form layout is important because a well-organized interface can reduce entry errors.

## Dropdowns and Input Validation

Dropdowns were added to appropriate form cells.

For example:

```text
Department:
[ Finance ▼ ]
```

and:

```text
Equipment:
[ Laptop ▼ ]
```

Users select from approved options rather than entering values manually.

Input validation was also added to control numeric fields such as quantity.

## Status Indicator

A status indicator was added to the form using Conditional Formatting.

The indicator provides feedback about the current state of the request.

For example:

```text
Status: Ready
```

or another status can be displayed depending on whether required information has been entered correctly.

Conditional Formatting can automatically change the appearance of a cell based on its value.

This provides a visual signal to the user.

## Conditional Formatting

Conditional Formatting allows Excel to apply formatting based on rules.

For example:

```text
If Status = "Ready"
Then apply the appropriate formatting
```

This makes important information easier to notice.

Conditional Formatting can be used to highlight:

* Valid entries
* Invalid entries
* Missing information
* Completed requests
* Pending requests

## Setting Up the Request Log

A separate worksheet was created to store submitted requests.

The request log acts as the permanent record of form submissions.

For example:

```text
Request ID | Employee | Department | Equipment | Quantity | Status
```

Each time a request is submitted, a new record is added to the log.

This separates the user interface from the underlying dataset.

## Submit Request Macro

A macro was recorded to handle the submit request process.

The purpose of the macro was to take the information entered into the form and add it to the request log.

The general workflow was:

```text
Enter Request
      ↓
Validate Information
      ↓
Click Submit
      ↓
Copy Form Data
      ↓
Add Record to Request Log
```

This automates the process of transferring information from the form into the dataset.

## Clear Form Macro

A second macro was created to clear the form after a request had been submitted.

The purpose is to prepare the form for the next request.

The workflow is:

```text
Submitted Request
      ↓
Clear Form
      ↓
Ready for Next Request
```

This prevents users from manually deleting each field before entering a new request.

## Clear Log Macro

A third macro was created to clear the request log.

This can be useful when resetting the workbook for testing or demonstration purposes.

It is important to use this type of macro carefully because clearing the log removes the stored records from the worksheet.

## Creating Buttons

Buttons were added to the form to make the macros easy to use.

The form included buttons for:

```text
[ Submit Request ]
[ Clear Form ]
[ Clear Log ]
```

Each button was assigned to its corresponding macro.

This creates a more user-friendly interface because users can interact with the workbook without opening the Macro menu.

## Assigning Macros to Buttons

Each button was connected to the appropriate macro.

For example:

```text
Submit Request → Submit Request Macro
Clear Form → Clear Form Macro
Clear Log → Clear Log Macro
```

This creates a simple interface for controlling the workbook.

## Data Validation in the Request Log

Data Validation was also added to the request log.

This provides an additional layer of data quality control.

Even though the form already controls user input, validating the request log helps protect the underlying dataset.

This can help maintain consistent values in the stored records.

## Testing the Form

After building the form, I tested all three buttons from start to finish.

The testing process included:

```text
Enter Request
      ↓
Submit Request
      ↓
Check Request Log
      ↓
Clear Form
      ↓
Enter Another Request
      ↓
Test Again
      ↓
Clear Log
```

Testing the complete workflow helped confirm that the form, validation rules, macros, buttons, and request log worked together correctly.

## End-to-End Testing

End-to-end testing means testing the complete process rather than checking individual components separately.

For this exercise, I checked that:

* Data could be entered into the form
* Dropdowns worked correctly
* Quantity limits were enforced
* The status indicator responded correctly
* The Submit Request button worked
* Records were added to the request log
* The Clear Form button worked
* The Clear Log button worked
* Validation rules remained active

This type of testing helps identify issues that may only appear when all parts of the system interact.

## Why This Matters for Data Analysis

Data analysis depends on having structured and reliable information.

A well-designed data-entry form can improve data quality before the analysis stage.

Controlled data entry can help:

* Reduce inconsistent categories
* Prevent invalid values
* Standardize records
* Reduce manual data cleaning
* Improve reporting accuracy
* Make datasets easier to analyze

This connects directly with the data quality concepts learned earlier in the challenge.

## Data Entry Workflow

The complete system created today followed this process:

```text
User Opens Form
       ↓
Enters Request Information
       ↓
Dropdowns and Validation Check Input
       ↓
Status Indicator Shows Form Status
       ↓
Submit Request
       ↓
Record Added to Request Log
       ↓
Clear Form
       ↓
Ready for Next Request
```

## Skills Practiced

Today I practiced:

* Building a data-entry form
* Setting up the Excel Form feature
* Creating structured data tables
* Creating reference lists
* Using Data Validation
* Creating dropdown lists
* Setting quantity limits
* Designing a form layout
* Using Conditional Formatting
* Creating status indicators
* Setting up a request log
* Recording a Submit Request macro
* Recording a Clear Form macro
* Recording a Clear Log macro
* Creating buttons
* Assigning macros to buttons
* Adding validation to the request log
* Testing an automated workflow
* Performing end-to-end testing

## Key Takeaways

1. Uncontrolled data entry can create inconsistent and unreliable datasets.
2. Data Validation can restrict users to approved values.
3. Dropdown lists make data entry more consistent.
4. Quantity limits can prevent invalid numeric entries.
5. Conditional Formatting can provide useful visual status indicators.
6. A request log can store submitted form records in a structured table.
7. Macros can automate the submission and clearing processes.
8. Buttons make macros easier for users to access.
9. Data Validation should also protect the underlying dataset.
10. End-to-end testing is important when building automated Excel tools.
11. A well-designed data-entry system can improve data quality before analysis begins.

## Reflection

Today I learned how different Excel features can be combined to create a practical data-entry system.

The exercise showed me that data quality can be improved at the point where information is collected rather than waiting until the analysis stage to fix problems.

Using dropdowns and validation helped control what users could enter, while macros automated the process of submitting and clearing requests.

I also learned that testing the entire workflow is important because the form, validation, buttons, macros, and request log all need to work together.

This exercise gave me a better understanding of how Excel can be used to create simple business tools rather than only spreadsheets for calculations and analysis.

## Files

* `day-28-practice.xlsm`

## Learning Resource

30 Day Excel Challenge by SDW Online.

```
```
