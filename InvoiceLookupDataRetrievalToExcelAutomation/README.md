# Invoice Lookup Data Retrieval To Excel Automation

## Overview
This UiPath automation performs a data-driven web scraping and update cycle: it iterates over invoice records stored in an Excel workbook, retrieves each invoice's authoritative data from a web application via UI Automation, and writes the extracted values back into the source workbook's DataTable representation.

## What it does
1. Reads `VendorID_Input.xlsx` into a `DataTable` variable (`dt_Invoice`) via `Read Range Workbook`, using the first row as headers
2. Launches Firefox and authenticates against the ACME System 1 web application (email/password form submission)
3. Navigates to the invoice search interface
4. Executes a `For Each Row` loop over `dt_Invoice`:
   - Types the current row's `Invoice Number` value into the search field
   - Submits the search
   - Extracts four data points from the resulting HTML table via `Get Text` activities: Vendor Tax ID, Invoice Item, Total, Date
   - Assigns each extracted value back into the corresponding column of the current `DataRow`
   - Returns to the search results view for the next iteration
5. After the loop completes, writes the fully populated `DataTable` back to the workbook via `Write Range Workbook`, overwriting the original sheet with enriched data

## Workflow
- **Main.xaml** — single-file implementation containing the full sequence: Excel I/O, authentication, and the iterative scrape/assign loop

## Technical implementation notes
- Selectors use a hybrid strategy (`FuzzySelector` + `CV`/Computer Vision fallback) for resilience against minor UI/DOM changes
- Web element targeting relies on UiPath's modern UI Automation object (`NApplicationCard`, `NTypeInto`, `NClick`, `NGetText`) rather than legacy selector-only activities
- Table cell extraction uses column/row-indexed selectors (`tableCol`, `tableRow`) scoped to the results `<TABLE>` element

## Input/Output
- **Input**: `VendorID_Input.xlsx` — columns: Invoice Number, Vendor Tax ID, Invoice Item, Total, Date (initially only Invoice Number populated per row)
- **Output**: Same file, same sheet, with Vendor Tax ID / Invoice Item / Total / Date columns populated per row after execution
- The `VendorID_Input.xlsx` file included in this folder already contains the populated output from a completed run, so it can be viewed directly without re-running the automation

## Key concepts practiced
- DataTable manipulation (`ForEachRow`, `DataRow` column assignment)
- Excel I/O via `ReadRange` / `WriteRange`
- Modern UI Automation targeting (fuzzy + CV hybrid selectors)
- Web-based data extraction and round-trip data enrichment

## Security note
Login credentials used during development have been replaced with placeholder values before publishing. No real credentials are stored in this workflow.

## Requirements
- UiPath Studio
- Mozilla Firefox installed
- UiPath.Excel.Activities
- UiPath.UIAutomation.Activities