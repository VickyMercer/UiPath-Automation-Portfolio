# FlightReservationFileGenerationAutomation

## Overview
This automation collects flight reservation details from the user through input dialogs and generates a text file summarizing the booking information.

## What it does
1. Prompts the user to select or enter a destination via an input dialog
2. Prompts the user to select or enter a departure date via an input dialog
3. Prompts the user to select or enter a return date via an input dialog
4. Combines the destination, departure date, and return date into a flight details array
5. Writes a formatted reservation summary to a text file
6. Writes the flight details to the console
7. Writes a confirmation message to the console

## Workflow
- `Main.xaml`

## Output
- A text file (`Flights_array.txt`) containing the formatted reservation summary — included in this project folder as a sample output
- Console output of the flight details and a confirmation message

## Key concepts practiced
- Input dialogs for capturing user input
- Array creation and manipulation
- Writing formatted text to a file
- String concatenation
- Console output with WriteLine

## Requirements
- UiPath Studio
- UiPath.System.Activities package