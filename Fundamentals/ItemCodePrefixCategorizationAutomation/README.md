# Item Code Prefix Categorization Automation

## Overview
This automation categorizes a list of item codes into separate groups based on their two-letter prefix, using a switch statement for classification.

## What it does
1. Initializes an array of item codes with varying prefixes
2. Iterates through each item code in the array
3. Checks the first two characters of each item code using a switch statement
4. Adds the item to the corresponding group array (Ax, Bx, or Cx) based on its prefix
5. Displays a message for any item that doesn't match a recognized prefix
6. Logs the final contents of each group array

## Workflow
- `Main.xaml`

## Output
- A message displayed for any item with an unrecognized prefix format
- Log entries showing the final contents of the Ax, Bx, and Cx group arrays

## Key concepts practiced
- Array initialization and iteration
- Switch statement for multi-way branching
- String substring extraction
- Array concatenation
- Logging with different log levels

## Requirements
- UiPath Studio