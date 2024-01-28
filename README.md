# backupynh
A bash script to cycle Yunohost backup and mirror the backup folder, and upload backup to remote site
version 28-01-2024
author email: tech@amer.ovh
this script aims to enhance Yunohost backup by 
- calling Yunohost to list the existing backups and delete the extra ones beyond a defined number
- mirroring the yunohost.backup archives folder to another given location
- exporgting the last backup to an external site using curl (not tested yet. please wait for the next tested version)
- logging to syslog, and send email at the end, so it can be run as a cron job with any desired frequency
- being called with parameters, otherwise use the following default values 
This script is provided as a courtesy to the Yunohost community, and without any warranty. Use-it at your own responsibility.
Don't hesitate also to propose enhancements.

Usage:
1- Download the .sh file, 
2- Edit it and check the header. You can adapt the default values, like the email address, to be able to call the script without params
3- Either execute the script on command line, or place it under cron to execute it.
4- call backupynh.sh --help for more details about how to available options
