# Number Guessing Game Automation

## Overview
This automation implements a number guessing game where the user has a limited number of attempts to guess a randomly generated secret number.

## What it does
1. Generates a random secret number between 1 and 50
2. Prompts the user to enter a guess via an input dialog, repeating for up to 3 attempts
3. Checks each guess against the secret number
4. Displays a message indicating whether the guess was correct or incorrect
5. Ends the loop early if the correct number is guessed, or after 3 attempts
6. Displays a final message revealing the secret number
7. Logs the secret number

## Workflow
- `Main.xaml`

## Output
- Messages displayed after each guess indicating correct or incorrect
- A final message revealing the secret number
- A log entry recording the secret number

## Key concepts practiced
- Random number generation
- Do While loop with a maximum iteration limit
- Conditional logic for evaluating guesses
- Message boxes for user feedback
- Logging with different log levels

## Requirements
- UiPath Studio