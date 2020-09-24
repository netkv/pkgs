# scriptpkg
script manager to update remove and install shell scripts and make installing and updating them easier

**where works?**

tested in linux, android termux and freebsd

**instalation**

use installer: __wget https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/installer; sleep 5; sh installer__ ***(recommended)***

use with sudo to install into root writable only directories ***(recommended)***

and after that delete installer

or:

download "spkg" file and put it into folder that you want and make it executable using gui or chmod +x

create file  ~/.config/spkg/destination and write to it destination folder that you want to have scripts saved in (dont forget if you want to install them into root writable only directory you need use sudo and then config dir is /root/.config/spkg

create folder  ~/.config/spkg/packages

create folder  ~/.config/spkg/repos

and then add repos that you want

needs: wget, sh, cat, bash (only for "install" command), curl (only for usage and repo list)

**update spkg itself**

create file ~/.config/spkg/packages/spkg with content: https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/spkg if that file doesnt exist already
(!!!JUST URL LINK, NO END WEBPAGE!!!)

then just: __spkg update spkg__

**sometimes changing of how config is handled will break scriptpkg**

needs manual fix then

# Usage: https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/usage

Main script Repo: https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/repos/main

other repos: https://github.com/Pan00Pernicek/scriptpkg/blob/master/repo-index

*example usage cases*

*to sync scripts between devices*

*to manage sripts easier*

**creating repo:**

you can use anything online that stores **raw text only** **(recommended github)**

then add scripts to it using this template

```script_name=script_url```

and at end of that file put:

```spkg sync ${!1}```

then add it using __spkg repo add url__

*and if you want then you can pull request or inform me in any other way to add it into https://github.com/Pan00Pernicek/scriptpkg/blob/master/repo-index*
