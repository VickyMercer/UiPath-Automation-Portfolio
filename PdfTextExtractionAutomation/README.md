# Pdf Text Extraction And Save Automation

## Overview
This UiPath automation opens a PDF file, extracts its text content, saves the 
extracted text to a new text file, opens that file for viewing, and displays a 
message confirming completion.

## What it does
1. Opens the input PDF file
2. Extracts all text content from the PDF
3. Writes the extracted text into a new text file
4. Saves the text file
5. Opens the saved text file for viewing
6. Displays a message in the output

## Workflow
- **Main.xaml** — contains the full automation logic (PDF text extraction → text 
  file creation → file save → file open → output message)

## Output
- A text file containing the extracted PDF content is created and opened
- A message is displayed indicating the process is complete
- The generated output text file is included in this project folder as a sample result

## Key concepts practiced
- PDF text extraction
- File creation and writing
- Opening/launching a saved file
- Output messaging on completion

## Requirements
- UiPath Studio
- UiPath.PDF.Activities package
- UiPath.System.Activities package