# tilda-starter

This script is a workaround for config files nuking issue in Tilda. 
If any config is found to be zero bytes long it will be restored from backup. 
Tilda is then started.

It can also be used to create backups (config_n.bak), either for specified 
config files only, or else for all found inside "~/.config/tilda/".
Existing backups will overwriten!

If you're about to use this script for the first time,
make sure to create backup(s) first. See bellow.  

Backup arguments:

 -c "config_1 config_2 config_3"  
 > Backup only specified config files and exit.	  !!Always use quotes as in the example!!  
       
 -b		
 > Backup each config file found and exit.  

Normal usage arguments:

 -i number_of_instances_to_run	
 >Number of Tilda instances to run. Can be ommited for a single one.

Output, including Tilda's, is logged to "tilda-starter.log" which is located
in the directory that contains this script ( if writable ( ~/.config/tilda should be just fine ).
To disable logging, comment the line 75.

2015 Filip Danilovic <filip@openmailbox.org>
