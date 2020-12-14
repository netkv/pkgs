# scriptpkg

**new repos without need of bash and basic support of deps and meta packages coming soon, test tesing repo and see**

**spkg now uses curl instead of wget, might add support for both later**

**!!!If you installed spkg before 10/10 2020 reinstall it, due to config changes it wont work anymore, (remove spkg folder in .config and spkg file in directory where you installed spkg and install again!!!**

A script package manager to update remove and install shell scripts (and appimages, and dotfiles and any file now) and make installing and updating them easier.

**Where does it works?**

Tested on Linux, Android Termux, Solaris and FreeBSD. It also works on WSL.

**Instalation**

use installer: `wget https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/installer; sh installer; rm installer`

use with sudo to install into root writable only directories

and after that delete installer

or:

download "spkg" file and put it into folder that you want and make it executable using gui or chmod +x

create file  ~/.config/spkg/destination and write to it destination folder that you want to have scripts saved in (dont forget if you want to install them into root writable only directory you need use sudo and then config dir is /root/.config/spkg)

create folder  ~/.config/spkg/packages

create folder  ~/.config/spkg/repos

and then add repos that you want

needs: ~~wget~~, sh, cat, bash (only for "install" command), curl ~~(only for usage and repo list)~~

**update spkg itself**

create file ~/.config/spkg/packages/spkg with content: ```https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/spkg/url``` if that file doesnt exist already

then just: __spkg update spkg__

**sometimes changing of how config is handled will break scriptpkg**

needs manual fix then

# Usage: 
https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/usage

Main script Repo: https://raw.githubusercontent.com/Pan00Pernicek/scriptpkg/master/repos/main

other repos: https://github.com/Pan00Pernicek/scriptpkg/blob/master/repo-index

*example usage cases*

*to sync scripts between devices*

*to manage apps and scripts easier*

**creating repo:** (normal, check testing repo for example of advanced repo methods)

you can use anything online that stores **raw text only**

then add items to it using this template

```name=url```

and at end of that file put:

```spkg sync ${!1}```

or

```spkg sync ${!1} $2```

if you want allow non-interactive use of your repo

then add it using __spkg repo add url__

*and if you want then you can pull request or inform me in any other way to add it into https://github.com/Pan00Pernicek/scriptpkg/blob/master/repo-index*

# etc

todo: better managing of non executable files, better installer

upgrading (changing url in repo)

~~make my own distro~~
