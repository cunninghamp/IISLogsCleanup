.SYNOPSIS
IISLogsCleanup.ps1 - IIS Log File Cleanup Script

.DESCRIPTION 
Creates zip archives of IIS log files older than the first day
of the previous month.

.PARAMETER Logpath
The IIS log directory to cleanup.

.PARAMETER ArchivePath
The path to a location where zip files are moved to, for example
a central log repository stored on a NAS.

.EXAMPLE
.\IISLogsCleanup.ps1 -Logpath "D:\IIS Logs\W3SVC1"

.EXAMPLE
.\IISLogsCleanup.ps1 -Logpath "D:\IIS Logs\W3SVC1" -ArchivePath "\\nas01\archives\iislogs"

.LINK
http://exchangeserverpro.com/powershell-script-iis-logs-cleanup

.NOTES
Written by: Paul Cunningham

Find me on:

* My Blog:	http://paulcunningham.me
* Twitter:	https://twitter.com/paulcunningham
* LinkedIn:	http://au.linkedin.com/in/cunninghamp/
* Github:	https://github.com/cunninghamp

For more Exchange Server tips, tricks and news
check out Exchange Server Pro.

* Website:	http://exchangeserverpro.com
* Twitter:	http://twitter.com/exchservpro

Additional Credits:
Filip Kasaj - http://ficility.net/2013/02/25/ps-2-0-remove-and-compress-iis-logs-automatically/
Rob Pettigrew - regional date issues
Alain Arnould - Zip file locking issues
