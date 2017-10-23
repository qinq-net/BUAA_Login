# BUAA_Login
Shell script for BUAA network login

## How to execute
To execute this script, you should download it, change its content and authority, and then execute it.

  mkdir ~/scripts
  cp ~/Downloads/BUAA_Login.sh ~/scripts/BUAA_Login.sh #move the script to desired directory
  #Edit the scripts, change the username and the password on line 5.
  chmod +x ~/scripts/BUAA_Login.sh
  ~/scripts/BUAA_Login.sh
  
The scripts should be up and running. It will re-login every 2 hours.

## How to make this script a startup service

Insert line `~/scripts/BUAA_Login.sh &` into file /etc/rc.local above the final line 'exit 0'.

Then reboot, use `ps -A | grep BUAA_Login.sh` to see if the scripts is running.
