# Full Session Extraction Automation

## Overview
This UiPath automation logs into the ACME System 1 test website, extracts the full Work Items table, and logs out — but instead of doing everything in one file, the logic is split across three separate, reusable workflow files that get called in sequence from Main.xaml.

## What it does
1. `Main.xaml` launches Firefox once, opens a browser session, and stores a reference to that window in a variable
2. That variable is passed into each of the following workflows in order, so they all operate on the same browser window rather than opening new ones:
3. `Login ACME.xaml` — types the Email and Password into the login form and clicks Login
4. `Extract DataTable.xaml` — clicks into the Work Items section and extracts the full table (Actions, WIID, Description, Type, Status, Date) into a DataTable
5. `Logout ACME.xaml` — clicks Log Out, then checks the app state to confirm it has returned to the Login page, logging a success or failure message accordingly

## Workflow
- **Main.xaml**
- **Login ACME.xaml**
- **Extract DataTable.xaml**
- **Logout ACME.xaml**

## Output
- A DataTable containing the extracted Work Items data
- Log messages confirming login, extraction, and logout status

## Key concepts practiced
- Modular automation design using invoked workflows (splitting one process into reusable files)
- Passing UI element references between workflows
- Table data extraction from a web application
- State verification (checking the app returned to the expected page after logout)
- Resilient element targeting: each UI interaction uses a primary method (Selector or FuzzySelector) with Computer Vision (CV) as an automatic fallback, so the automation can still find the right element even if the page layout shifts slightly

## Technical detail: dual-layer window attachment
Each browser window reference in this project is backed by two independent ways of being found. The primary method is the UI element variable passed between workflows, which lets each invoked file attach directly to the exact browser window already open in memory. As a fallback, every window is also defined with its own stored URL, selector, and visual (Computer Vision) fingerprint — so if the passed-in reference ever fails to resolve (for example, if the window reference expires or the page reloads unexpectedly), UiPath's Healing Agent can automatically re-locate the correct window using that stored data instead. This means the automation has a backup path built in at the window level, not just for individual clicks and fields.

## Security note
Login credentials in this workflow have been replaced with placeholder values before publishing. The password field also uses UiPath's secure input mode (`IsPassword`) to mask its value during execution and logging.

## Requirements
- UiPath Studio
- Mozilla Firefox installed
- UiPath.UIAutomation.Activities