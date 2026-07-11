# Application Status Check Automation

## Overview
This UiPath automation checks whether a specified desktop application (e.g., Notepad, a document editor, etc.) is currently open, and displays a message based on the result. An application is treated as "open" even if it is minimized.

## What it does
1. Checks whether the target application is currently open/running on the system
2. Treats a minimized application as **open** (visibility state is not a factor — only running/process state is checked)
3. Displays a message indicating the application's status

## Workflow
- **Main.xaml** — contains the full automation logic (application state check → conditional output message)

## Output
- A message is displayed based on the application's status

## Key concepts practiced
- Application/process state checking
- Conditional logic based on system state
- Output panel messaging based on outcome

## Requirements
- UiPath Studio
- Target application installed (e.g., Notepad)
- UiPath.UIAutomation.Activities & UiPath.System.Activities package