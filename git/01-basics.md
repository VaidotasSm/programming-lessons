
# Install

## Install Git (Windows)

* Option 1 - using Chocolatey

`choco install git.install`

* Option 2 - Install Msysgit


## Optional - useful software

* ConEmu - Better Windows CMD.
* Visual Studio Code - good editor with some Git support.
* GitKraken/SourceTree - Visual Git client. For now use only to play around, prefer using CMD. 


# Git Setup

## Create/Edit config file

Location: `C:\Users\XXX\.gitconfig` (Windows)

```
[user]
	name = petras petraitis
	email = petras@petraitis.com
[core]
	editor = 'C:\\Programs\\Sublime Text 2\\sublime_text.exe' --wait
[alias]
	lg = log --color --graph --abbrev-commit --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr)%C(bold blue)<%an>%Creset' --all
```

# Git Usage

## Start working - remote repository (from server)

* Clone - download repository. Will create new folder.

`git clone https://github.com/VaidotasSm/programming-lessons.git`

* Pull - download new changes from server (someone might have updated files).

`git pull`

## Start working - local repository

`git init` - create repository in current folder.


## Common Workflow

### Local Branch (not server):

1. Do some work - make changes, create files...

2. Check status - displays your changes and other info.

`git status`

3. Make your changes staged (active)

`git add -A`

4. Commit staged (active) changes - to local history.

`git commit -m "Message Text"`

`git commit` - sublime should popup for entering text

5. Check local history - must see new "HEAD"

`git log`

`git lg` - if using setup config above - nicer history.


### Remote Branch (server):

6. Push - send changes to server.

`git push`








