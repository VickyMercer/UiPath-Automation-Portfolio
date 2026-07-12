# String Parsing And Formatting Automation

## Overview
This UiPath automation demonstrates extracting specific structured data from a 
single sentence using string parsing functions, then reassembling the extracted 
values into a clean, formatted output string.

## What it does
1. Defines a source sentence containing a name and a list of related items
2. Extracts the name from the sentence using string index/substring operations
3. Extracts the list of items from the same sentence by splitting on delimiters
4. Builds a final formatted string combining the extracted name and item list
5. Logs the final formatted output

## Workflow
- **Main.xaml** — contains the full automation logic (string parsing → data 
  extraction → string formatting → log output)

## Output
- A message is logged showing the final formatted string

## Key concepts practiced
- String splitting and substring extraction
- Index-based string parsing (LastIndexOf, Substring, Trim)
- List conversion from parsed string data
- String formatting and joining

## Requirements
- UiPath Studio
- UiPath.System.Activities package