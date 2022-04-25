# Windows DNS A record add with roll-back

## Description
This workflow starts with a condictional task which checks user input for the desire to also create a PTR record when creating a Windows DNS A recrod.  The workflow also has 3 customer tasks.  1 task adds the A record to Windows DNS with an associated PTR record.  Another tasks effectively does the exact same thing except without the PTR recrod.  The third task is used for rollback of either of the two Add record tasks.

## Instructions
Import the workflow into Intersight Cloud Orchestrator.  Create a powershell target (see PowerShell requirements section below).  Change the Zone Name Worklow input to the zone you would like to use.  You can now run the workflow.

## PowerShell Requirements
The workflow uses PowerShell.  For PowerShell to work a PowerShell target needs to be added.   The target needs to be a Windows box, refer to https://intersight.com/help/saas/resources/Executor_PowerShell#supported_targets in order to add the PowerShell target.  A special script needs to be run on the Windows target in order for Windows to allow remote execution of a PowerShell script from the Intersight Assist.
