# Text File Parsing Automation

## Overview
This automation reads structured data from a text file, extracts specific fields using text-splitting logic, and generates a personalized message using find-and-replace text modification.

## What it does
1. Reads the contents of a text file into a string variable
2. Extracts the first name field by splitting the text around known separators
3. Extracts the last name field using the same splitting approach
4. Trims extra whitespace from the extracted values
5. Builds a message template with placeholder tags for the recipient's name
6. Replaces the placeholder tags with the extracted first and last name
7. Logs the extracted first name, last name, and final message
8. Writes a confirmation message to the console

## Workflow
- `Main.xaml`

## Output
- Log entries recording the extracted first name, last name, and the final generated message
- Console output confirming completion
- The source text file (`EmployeeDetails.txt`) is included in the project folder as sample input

## Key concepts practiced
- Reading data from a text file
- Text splitting using custom separators
- Text trimming and cleanup
- Find-and-replace text modification
- Logging with different log levels
- Console output with WriteLine

## Requirements
- UiPath Studio