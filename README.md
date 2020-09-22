# scriptpkg
script manager to update remove and install shell scripts and make installing and updating them easier

**instalation**

download "spkg" file and put it into /usr/local/bin and make it executable using gui or chmod +x

create file  ~/.config/spkg/destination and write to it destination folder that you want to have scripts saved in

needs: wget, sh

---------------------------------------------------------------------------------
Usage:
---------------------------------------------------------------------------------

install script:
spkg install script-url (you will be asked for name that you want save script as)

update script:
spkg update script-name

remove script:
spkg remove script-name

