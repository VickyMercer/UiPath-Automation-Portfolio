# Leap Year Check Automation

## Overview
This UiPath automation takes a year as input and mathematically determines 
whether it is a leap year, displaying the result accordingly. The same logic 
is implemented twice using two different UiPath workflow types — Sequence 
and Flowchart — to demonstrate both approaches.

## What it does
1. Prompts the user via an input dialog to enter a year
2. Evaluates the year using leap year divisibility rules
3. Displays a message indicating whether the entered year is a leap year or not

## Workflow
- **Sequence.xaml** — implements the leap year check using a Sequence workflow
- **Flowchart.xaml** — implements the same leap year check using a Flowchart workflow

## Output
- A message is displayed indicating whether the input year is a leap year or not

## Key concepts practiced
- User input via input dialog
- Conditional logic based on mathematical evaluation
- Sequence vs. Flowchart workflow types
- Output messaging based on evaluated condition

## Requirements
- UiPath Studio
- UiPath.System.Activities package