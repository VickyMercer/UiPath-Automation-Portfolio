# Excel Data Table Calculation And Update Automation

## Overview
This automation reads tabular data from an Excel workbook, performs a calculated field derivation across all records, and writes the updated data table back to the workbook.

## What it does
1. Reads data from a source sheet in the Excel workbook into a data table
2. Adds a new calculated column to the data table
3. Iterates through each row in the data table
4. Computes the calculated field value using existing column values for each row
5. Writes the updated data table to a new sheet in the same workbook
6. Logs a confirmation message once the update is complete

## Workflow
- `Main.xaml`

## Output
- The Excel workbook updated with a new sheet containing the calculated values — this file is included in the project folder as both the sample input and the resulting output
- A log entry confirming the update was completed

## Key concepts practiced
- Reading data from Excel into a data table
- Adding columns to a data table dynamically
- Iterating through data table rows
- Arithmetic calculations on data table values
- Writing data back to Excel
- Logging with different log levels

## Requirements
- UiPath Studio
- UiPath.Excel.Activities