
Usage:
-------------------------------------------------------------
install: spkg install item-name (you will be asked for repo that you want install from)
-------------------------------------------------------------
sync script from url: spkg sync item-url wanted-item-name (you will be asked for name that you want save script as if you wont enter name )
-------------------------------------------------------------
sync file to defined directory instead of default one: spkg sync file file-url file-destination+file-name (example /bin/text.txt)
-------------------------------------------------------------
update script: spkg update item-name
-------------------------------------------------------------
remove script: spkg remove item-name
-------------------------------------------------------------
list scripts: spkg list (if you install items with sudo then you need also use sudo here)
-------------------------------------------------------------
add repo: spkg repo add repo-url
-------------------------------------------------------------
remove repo: spkg repo remove repo-name
-------------------------------------------------------------
get list of core repos that exist: spkg repo getcore
-------------------------------------------------------------
get configuration of item or destination: spkg catconf item
-------------------------------------------------------------
more info: https://github.com/Pan00Pernicek/scriptpkg
-------------------------------------------------------------
