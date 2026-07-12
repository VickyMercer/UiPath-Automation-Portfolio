# Sum Calculation With Invoked Workflow Automation

## Overview
This UiPath automation demonstrates modular workflow design — invoking a 
separate workflow file to perform a calculation, passing data between the main 
and invoked workflows using input, output, and input-output arguments.

## What it does
1. Sets an initial status value in the main workflow
2. Invokes a separate workflow file, passing two numeric input values
3. The invoked workflow logs the received status, calculates the sum of the two 
   values, and updates the status to indicate completion
4. The invoked workflow returns both the calculated result and the updated 
   status back to the main workflow
5. The main workflow logs a final message combining the returned status and result

## Workflow
- **Main.xaml** — invokes the sub-workflow, passes input values, receives and 
  logs the final result
- **CalculateSum.xaml** — performs the calculation and status update, invoked by 
  Main.xaml

## Output
- A message is logged in the invoked workflow showing the initial status
- A final message is logged in the main workflow combining the updated status 
  and calculated result

## Key concepts practiced
- Workflow modularization (Invoke Workflow File)
- Passing arguments between workflows: In, Out, and InOut argument types
- Cross-workflow variable/state tracking
- Log message output at multiple stages

## Requirements
- UiPath Studio
- UiPath.System.Activities package