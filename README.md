# scriptpkg
script manager to update remove and install shell scripts and make installing and updating them easier

**where works?**

tested in linux, android termux and freebsd

**instalation**

use installer: wget https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/installer; sleep 5; sh installer

use with sudo to install into root writable only directories (recommended)

and after that delete installer

or:

download "spkg" file and put it into folder that you want and make it executable using gui or chmod +x

create file  ~/.config/spkg/destination and write to it destination folder that you want to have scripts saved in (dont forget if you want to install them into root writable only directory you need use sudo and then config dir is /root/.config/spkg

needs: wget, sh, cat, bash (only for "install" command)

**update spkg itself**

create file ~/.config/spkg/packages/spkg with content: https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/spkg if that file doesnt exist already

then just: spkg update spkg

---------------------------------------------------------------------------------
Usage: https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/usage
---------------------------------------------------------------------------------
Main script Repo: https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/repos/main

other repos: https://github.com/Pan00Pernicek/scriptpkg/blob/master/repo-index


