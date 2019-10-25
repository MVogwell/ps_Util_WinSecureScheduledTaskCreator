# ps_Util_WinSecureScheduledTaskCreator
This powershell script creates a "secure" scheduled task by only allowing an executable or script to run if it matches a (pre-calculated) SHA256 hash.

## Process;

* This powershell script will 
** Ask for the name that will be used for the scheduled task 
** Ask for details of the executable or script to started in a scheduled.  
** Ask for details of an SMTP server and email options (sender, recipient, subject and body text)
** Calculate the SHA256 hash of the executable to be run.
** Generate a scheduled task argument 

* The admin then creates the scheduled task based on the output of the script

* Running the scheduled task will then check that the executable/script to be started still matches the calculated SHA256 hash.  If the executable/script no longer matches the SHA256 hash it will send an email alert. 

## EXAMPLE
./WinSecureScheduledTaskCreator.ps1

This will run the script. If the config file WinSecureScheduledTaskCreator.json is found in the same folder as the script then it will be used otherwise the script will prompt for the required information

## EXAMPLE 2
./WinSecureScheduledTaskCreator.ps1 -fConfigPath 'full path name to WinSecureScheduledTaskCreator.json'

This will run the script using the config file specified in fConfigPath

## NOTES
Use this as you wish but I take no responsibility whatsoever for the outcomes!  Be excellent to each other.

## LINK
https://github.com/MVogwell/ps_Util_WinSecureScheduledTaskCreator