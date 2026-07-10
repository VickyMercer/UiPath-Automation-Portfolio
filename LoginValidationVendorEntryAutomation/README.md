# Login Validation and Vendor Entry Automation

## Overview
This UiPath automation logs into the UiPath ACME test website and verifies whether the login was successful. If login succeeds, it proceeds to add a single new vendor record and confirms this with a second message. If login fails, it displays an error message and the program stops.

## What it does
1. Launches Firefox and navigates to the ACME website's login page
2. Enters login credentials and submits the form
3. Verifies whether login was successful by checking the post-login landing page
4. Displays a message indicating login status:
   - **"Login successful"**, or
   - **"Failed to login"**
5. **If login succeeded:**
   - Navigates to the vendor entry section
   - Adds **one vendor record** with the following details:
     - Tax ID
     - Business Name
     - Address (City, Country)
   - Saves the entry
   - Displays a second message: **"Vendor is successfully added"**
6. **If login failed:**
   - Displays the failure message
   - Program stops (no further action taken)

## Workflow
- **Main.xaml** — contains the full automation logic (login → verify → status message → conditional vendor entry / stop)

## Output
- Login status message: `Login successful` or `Failed to login`
- On successful login only: `Vendor is successfully added`

## Key concepts practiced
- Browser automation (login flow)
- Conditional logic based on UI verification
- Single-record form data entry automation
- Multi-stage output messaging based on outcome

## Security note
Login credentials used during development have been replaced with placeholder values before publishing. No real credentials are stored in this workflow.

## Requirements
- UiPath Studio
- Mozilla Firefox installed
- UiPath.UIAutomation.Activities & UiPath.System.Activities package