# wip readme
install: basically run `installer` as root and it will do its thing

##how to use:

run `pkgs fn_exec make_help` (wip) or just `pkgs`

or read your config, easy

default repo is `main` btw

## FAQ

why it errors everytime when installing from repo?

because it tries to clear already cleared cache, not critical bug, just ignore it

how to make repo for pkgs?

take look at example first:
```
fn_repo_init
item <item-name> <item-link>
fn_rawrepo
```
if you want to add item that depends on another item add `depends <item-name> <dependency-name>` , it needs to be in same repo for now (hopefully i will fix that)
if you want to add item that optionaly depends on another item add `optional <item-name> <dependency-name>` , ^^
resulting repo can look like :
```
fn_repo_init
item foo https://bar
  depends foo potato
  optional foo something
item potato https://potato
  depends potato tomato
item something https://something
item tomato https://tomato
fn_rawrepo
```
this should work
you can also look at repotest for example

how to configure pkgs?

see `pkgsconf` , its not that hard
