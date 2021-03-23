# wip readme
*finnaly made depencdencies kind of work better, buts its all one big hack, it marks it package implicit and then removes orphans, but it work*


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
if you want add item that depends on some command provided by system add `sys bin <item-name> <cmd>` ,
if you want add item that can run only on certain cpu architectures add `sys arch <item-name> <arch1> <arch2> ...`,
resulting repo can look like :
```
fn_repo_init
item foo https://bar
  depends foo potato
  optional foo something
item potato https://potato
  depends potato tomato
  sys bin potato awk
item something https://something
  sys arch aarch64 armv7l armv7hl
item tomato https://tomato
fn_rawrepo
```
this should work
you can also look at repotest for example

how to configure pkgs?

see `pkgsconf` , its not that hard
