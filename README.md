# jenkins
common cleanup house tasks like deleting logs, temp folder and mysql backups


## my customer server gets full , what could be the solution ?
	
	generally server log files gets big overtime, you should keep compress it , retention period 7 days are enough.
	second reason is temp folders created overtime of long running server, you should stop service , delete temp folder and start service.
	mysql backup zipping
	csv files injection from third party application
	
## windows task scheduler and cron job is working fine on old server, what could be better way ?

	I guess you are missing GUI there, Jenkins is good thing for you. Here you can see all job list at single page and history of "scheduled job run".
	
## How will I keep 7 days log by date ?

	forfiles /p "E:\jboss\standalone\log" /s /m *.log /D -7 /C "cmd /c del @path"
