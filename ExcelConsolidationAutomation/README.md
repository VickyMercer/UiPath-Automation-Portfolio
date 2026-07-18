# Excel Consolidation Automation

## Overview
This UiPath automation consolidates employee data from multiple Excel reports, filters it down to a specific department, applies a salary adjustment, and exports the result to a new workbook.

## What it does
1. Loops through every Excel file inside the `Input` folder
2. Reads each file into a DataTable and merges all of them into a single combined DataTable
3. Filters the combined data to keep only rows where the Department column equals "Marketing"
4. For each remaining row, increases the Salary value by 2%
5. Writes the filtered, updated data into `Output\HR Report.xlsx`
6. Logs a completion message once processing is finished

## Workflow
- **Main.xaml** — contains the full automation logic (read all input files → merge → filter → update salary → write output → log completion)

## Input/Output
- **Input**: `AppOneReport.xlsx` and `AppTwoReport.xlsx` — both included in this folder, containing sample employee records (Employee Name, Employee ID, Department, Salary, Hire Date)
- **Output**: `HR Report.xlsx` — also included in this folder, already populated with the filtered and updated Marketing department records from a completed run

## Key concepts practiced
- Iterating through files in a folder (`For Each File`)
- DataTable merging (`Merge Data Table`)
- DataTable filtering (`Filter Data Table`)
- Row-level data manipulation (salary calculation)
- Excel read/write operations across multiple files

## Requirements
- UiPath Studio
- UiPath.Excel.Activities