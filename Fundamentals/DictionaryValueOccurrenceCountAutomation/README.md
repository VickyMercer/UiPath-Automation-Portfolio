# Dictionary Value Occurrence Count Automation

## Overview
This automation counts how many times each value occurs across a dictionary's entries and displays the tally for each unique value.

## What it does
1. Initializes a dictionary containing key-value pairs
2. Iterates through each value in the dictionary
3. Checks if the value already exists in a results dictionary
4. Increments the count if the value exists, or adds it with an initial count of 1 if it doesn't
5. Iterates through the results dictionary
6. Writes each unique value along with its occurrence count to the console
7. Logs a completion message

## Workflow
- `Main.xaml`

## Output
- Console output listing each unique value and how many times it occurred
- A log entry confirming completion

## Key concepts practiced
- Dictionary initialization and iteration
- Conditional key existence checks (ContainsKey)
- Incrementing counts within a dictionary
- Iterating over KeyValuePair collections
- Console output with WriteLine
- Logging with different log levels

## Requirements
- UiPath Studio