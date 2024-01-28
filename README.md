# backupynh
A bash script to cycle Yunohost backup and mirror the backup folder, and upload backup to remote site
version 28-01-2024
author email: tech@amer.ovh
this script aims to enhance Yunohost backup by 
- calling Yunohost to list the existing backups and delete the extra ones beyond a defined number
- mirroring the yunohost.backup archives folder to another given location
- exporgting the last backup to an external site using curl
- logging to syslog, and send email at the end, so it can be run as a cron job with any desired frequency
- be called with parameters, otherwise use the following default values 
This script is provided as a courtesy to the Yunohost community, and without any warranty. Use-it at your own responsibility.
Don't hesitate also to propose enhancements.
