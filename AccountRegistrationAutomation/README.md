# Account Registration Automation

## Overview
This UiPath automation handles a full account registration flow on the ACME System 1 test website — from clicking "Register" on the login page, through filling out the form, to submitting it and confirming success.

## What it does
1. Launches Firefox and opens the ACME System 1 login page using an Application Card targeting the login screen
2. Clicks the "Register" link to navigate to the registration form
3. Types values into the Email, Password, and Retype Password input fields (password fields use secure input mode)
4. Clicks the checkbox to agree to the updated Terms of Use and Privacy Policy
5. Clicks the "I'm not a robot" reCAPTCHA checkbox to satisfy the verification widget
6. Submits the form by clicking the "Register" button
7. Logs a confirmation message: **"User registered!!"**

## Workflow
- **Main.xaml** — contains the full registration sequence, from opening the browser to logging completion

## Output
- Log message confirming successful registration

## Key concepts practiced
- Multi-step web form automation
- Secure input handling for password fields (`IsPassword`)
- Checkbox and reCAPTCHA interaction
- Basic logging for process confirmation

## Security note
Both password fields use UiPath's secure input mode (`IsPassword`), which masks their values during execution and in logs. All credential values in this workflow have also been replaced with placeholder text before publishing.

## Requirements
- UiPath Studio
- Mozilla Firefox installed
- UiPath.UIAutomation.Activities