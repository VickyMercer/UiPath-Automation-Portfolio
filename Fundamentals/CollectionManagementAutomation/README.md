# Collection Management Automation

## Overview
This UiPath automation demonstrates working with a dictionary of collections — 
building grouped lists of values, modifying them by adding and removing items, 
and logging the final state.

## What it does
1. Initializes a dictionary where each key maps to a list of string values
2. Builds a collection of values under one key
3. Builds a second collection of values under a different key
4. Appends additional items to the second collection
5. Removes a specific item from the first collection
6. Logs the final contents of both collections

## Workflow
- **Main.xaml** — contains the full automation logic (dictionary initialization → 
  collection building → item append → item removal → log output)

## Output
- A message is logged showing the final contents of both collections

## Key concepts practiced
- Dictionary of collections (Dictionary of key to List)
- Building collections dynamically
- Adding and removing items from a collection
- Log message output

## Requirements
- UiPath Studio
- UiPath.System.Activities package