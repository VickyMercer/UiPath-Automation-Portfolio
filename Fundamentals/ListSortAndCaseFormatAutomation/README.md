# List Sort And Case Format Automation

## Overview
This UiPath automation demonstrates merging, sorting, and normalizing text 
casing across multiple lists using a loop.

## What it does
1. Builds a list of values
2. Merges it with a second, separately defined list containing inconsistently 
   cased values
3. Sorts the merged list alphabetically
4. Logs the sorted list
5. Iterates through each item, converting it to proper title case
6. Logs each converted item and appends it to a new list
7. Logs the final list of normalized values

## Workflow
- **Main.xaml** — contains the full automation logic (list building → merging → 
  sorting → iteration and case normalization → log output)

## Output
- A message is logged showing the sorted, merged list
- A message is logged for each item as it is converted to title case
- A message is logged showing the final, fully normalized list

## Key concepts practiced
- Building and merging collections
- Sorting a list via Invoke Method
- Looping through a collection (For Each)
- String case normalization
- Log message output at multiple stages

## Requirements
- UiPath Studio
- UiPath.System.Activities package