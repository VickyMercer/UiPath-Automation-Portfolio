# SimpleInterestCalculationWithInvokedWorkflowAutomation

## Overview
This automation calculates simple interest and final balance based on user-provided deposit amount and time period, using a separate invoked workflow to perform the interest calculation.

## What it does
1. Prompts the user to enter an initial deposit amount via an input dialog
2. Prompts the user to select or enter a time period (in years) via an input dialog
3. Invokes a separate workflow (`SimpleInterest.xaml`), passing the period, a fixed interest rate, and the deposit amount as inputs
4. Receives the calculated interest amount back from the invoked workflow
5. Calculates the final balance by adding the deposit amount and interest amount
6. Displays a message showing the interest amount and final balance
7. Logs the interest amount and final balance

## Workflow
- `Main.xaml`
- `SimpleInterest.xaml`

## Output
- A message is displayed showing the calculated interest amount and final deposit balance
- Log entries recording the interest amount and final balance

## Key concepts practiced
- Input dialogs for capturing user input
- Invoking a separate workflow file with in/out arguments
- Passing and receiving data between workflows
- Arithmetic operations for financial calculations
- Message boxes for user feedback
- Logging with different log levels

## Requirements
- UiPath Studio