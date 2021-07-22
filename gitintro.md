# Git Tutorial

## Version Control
* Local Version Control - one database on your hard disk that stores your changes to files
* Centralized Version Control - (CVCS) same as local, but can be accessed by various clients (server is a single point of failure)
* Distributed Version Control - (DVCS) same as centralized, but allows clients to create mirrored repositories

## What is Git?
Git is a DVCS that stores data as snapshots in a file system. 
* Snapshots - Git created a snapshot of each saved and edited version of your project (commit) and stores a reference to it. 
* Local Operations - Most necessary information can be found in local resources and this allows for process expediency since a project's history lives on the local disk. This eliminates the need to get history from the server and allows you to work on a project even when offline.
* Tracking Changes - Every change applied to a file or directory is tracked by Git, so file corruptions and loss of information will be detected.
* Loss of Data - Git makes it *extremely* difficult for your files to be damaged or lost.
* States - Files in Git can be either:
  * Committed - Data is stored securely in local database
  * Modified - File has been changed, but not committed
  * Staged - Flagged a file's changes to be committed in the next snapshot

## Git's History
It's roots are in the open source software project Linux kernel. Devs began by using a DVCS called BitKeeper in 2002, but by 2005 many stopped using it due to tension between the community of Linux kernel and BitKeeper's parent company and the revocation of the DVCS' gratis status. Linus Torvalds began creating Git. Since then, Git has become one of the most used VCS in the world.

# Getting Started

## Download Git
Git can be installed by:
* Installing as a package
* Installing via another installer
* Downloading and compiling the source code

### Mac OS X
* Terminal - Easiest 
* Git Website - http://git-scm.com/download/mac
* GitHub - http://mac.github.com

## Graphical Clients
Git includes GUI tools. You can also use third-party tools. Here's a variety of GUI clients: https://git-scm.com/downloads/guis

## Initial Customizaiton
* Configuration of Variables
  * `git config` allows the setting of config variables that control Git's operation and outlook
* Identity Setting
  * `git config --global user.name "Jane Smith"`  and  `git config --global user.email "example@email.com"` to set username and email
  * Using the `--global` option, this will apply to anything on the system

## Default Text Editor
Git will use the system default editor (probably Vim). To swtich editor, like Emacs, run the following in your Terminal (may need to find different instructions): `$ git config --global core.editor emacs`

## Check Settings
`$ git config --list` to check settings

## Getting Help
* `git help [command]`
* `git [command] --help`
* `man git-[command]`

# Setting up a Git Repository

## Importing
* Switch to target directory
  * `$ cd test`
* Use this command
  * `$ git inint`
You have now created a subdirectory named .git that has the respository
* Track these repository files by performing an initial commit
  * `$ git add *.c`
  * `$ git add LICENSE`
  * `$ commit -m [any message]`
Your files are now tracked and there's a commit

## Cloning
* `$ git clone https://github.com/test` - This copies all versions of all files for this project. 
* `$ git clone https://github.com/test mydirectory` - This copies and changes the name of all versions and files for this project.

# Workflow

## Local Repository Structure
Three components:
* Working Directory - files live here
* Index - used for staging
* Head - shows most recent commit

## Saving Changes
* Tracked - can be modified, unmodified, or staged in last snapshot (after cloning files are tracked)
* Untracked - not in last snapshot and do not reside in staging area

## Life Cycle of File Satus
1. After editing file, Git flags it modified
2. Stage the file
3. Commit

## Check File Status
`$ git status`

## Tracking and Staging New File
* Single file - `git add filename`
* All files - `$ git add *`

## Committing a File
`$ git commit -m [made change x,y,z]` - run after staging new file(s) and record your changes

## Committing All Changes
`$ git commit -a`

## Pushing Changes
`$ git push origin master` - pushes changes to a remote repo, for cloned repos Git will give the name "origin" to the server and "master" to repo

## Stashing Changes
* `git stash` - temp removes changes and hides them for a clean directory
* `git stash apply` - retrieves hidden changes

# Remote Repositories

## Seeing Your Remotes
* `git remote` - view the short names of all specific remote handles
* `git remote -v` - view all remote URLs next to their names

