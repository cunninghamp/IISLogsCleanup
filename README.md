# IISLogsCleanup.ps1 - A PowerShell script to compress and archive IIS log files.

This script will check the folder that you specify, and any files older than the first day of the previous month will be compressed into a zip file. If you specify an archive path as well the zip file will be moved to that location.

The recommended use for this script is a once-monthly scheduled task run on the first day of each month. This will compress all files older than the first day of the previous month, resulting in only 1-2 months of log files being stored on the server.

If the script detects any issues with the archive process that may indicate that a file was missed it will not delete the log files from the folder.

The script also writes a log file each time it is run so you can check the results or troubleshoot any issues.

## Parameters

* **-Logpath**, The IIS log directory to cleanup.
* **-ArchivePath**, The path to a location where zip files are moved to, for example a central log repository stored on a NAS.

## Usage Examples

```
.\IISLogsCleanup.ps1 -Logpath "D:\IIS Logs\W3SVC1"
```
This example will compress the log files in "D:\IIS Logs\W3SVC1" and leave the zip files in that location.

```
.\IISLogsCleanup.ps1 -Logpath "D:\IIS Logs\W3SVC1" -ArchivePath "\\nas01\archives\iislogs"
```
This example will compress the log files in "D:\IIS Logs\W3SVC1" and move the zip files to the archive path.

##More info

You can find more information about this script at: http://exchangeserverpro.com/powershell-script-iis-logs-cleanup

##Credits

Written by: Paul Cunningham

Find me on:

* My Blog:	http://paulcunningham.me
* Twitter:	https://twitter.com/paulcunningham
* LinkedIn:	http://au.linkedin.com/in/cunninghamp/
* Github:	https://github.com/cunninghamp

For more Exchange Server tips, tricks and news check out Exchange Server Pro.

* Website:	http://exchangeserverpro.com
* Twitter:	http://twitter.com/exchservpro

Additional Credits:

* Filip Kasaj - http://ficility.net/2013/02/25/ps-2-0-remove-and-compress-iis-logs-automatically/
* Rob Pettigrew - regional date issues
* Alain Arnould - Zip file locking issues
