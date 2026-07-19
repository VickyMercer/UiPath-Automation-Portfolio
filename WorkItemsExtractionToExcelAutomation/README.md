# Work Items Extraction To Excel Automation

## Overview
This UiPath automation logs into the ACME System 1 test website, navigates to the Work Items page, extracts the full list of assigned work items (including paginated results), and writes the extracted data into an Excel workbook.

## What it does
1. Launches Firefox and logs into the ACME System 1 test website using email and password
2. Navigates to the Work Items page after login
3. Extracts the work items table, including:
   - WIID (Work Item ID)
   - Description
   - Type
   - Status
   - Date
4. Automatically pages through all result pages using the table's "Next" link until all records are captured
5. Writes the complete extracted dataset into `WorkItems.xlsx`
6. Logs a completion message once data retrieval is finished

## Workflow
- **Main.xaml** — contains the full automation logic (login → navigate → extract paginated table data → write to Excel → log completion)

## Output
- `WorkItems.xlsx` — populated with all extracted work item records
- Log message confirming data retrieval is complete

## Key concepts practiced
- Browser automation (login flow)
- Structured data extraction from paginated web tables
- Excel write operations from a DataTable
- Logging for process confirmation

## Security note
Login credentials used during development have been replaced with placeholder values before publishing. No real credentials are stored in this workflow. The password field also uses UiPath's secure input mode (`IsPassword`) to mask its value during execution and logging.

## Requirements
- UiPath Studio
- Mozilla Firefox installed
- UiPath.Excel.Activities
- UiPath.UIAutomation.Activities