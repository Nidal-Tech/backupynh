# backupynh
A bash script to cycle Yunohost backups and mirror the backup folder, and upload the last backup to a remote site
version 28-01-2024
Author's email: tech@amer.ovh
This script aims to enhance Yunohost backup by: 
- calling Yunohost backup CLI to list the existing backups and delete the extra ones beyond a defined number
- mirroring the yunohost.backup/archives folder to another given location
- exporgting the last backup to an external site using curl (not tested yet. please wait for the next tested version)
- logging to syslog, and sending email at the end of the process, so it can be run as a cron job with any desired frequency
- being called on command line with parameters, otherwise using the default values

IMPORTANT: This script is provided under a CC license, as a contribution to the Yunohost community, and without any warranty. Use-it at your own responsibility.
Don't hesitate also to propose enhancements.

Usage:
1- Download the .sh file, 
2- Edit it and check the header. You can adapt the default values, like the email address, to be able to call the script without params
3- Either execute the script on command line, or place it under cron to execute it periodically.
4- call backupynh.sh --help for more details about how to use the available options
