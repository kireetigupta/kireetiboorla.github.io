---
layout: post
title: Git commands, tips & tricks.
---

## Git configuration 
3 levels of configuration. (system level, user level, 
1.System Level
  * at /etc/gitconfig
  * git config --system
2.User level
  * ~/.gitconfig
  * git config --system
3.Project level
  * proj/.git/config

to set configuration at different level use "git cofig --level". level could be system/user/proj.

## Autocompletion in Git
 1. download git autocompletion script. 
 2. move it to home directory
 3. modify bash_rc or zsh_rc to source the above file on loading. 
 
## Git Help
 1. git help <command>  --> returns info on the command. 
 2. ex: git help log
 3. f-> forward, b-> back, q-> quit. 

## Initialize a repository
git init --> initialize a git project. 
creates a '.git' directory to maintain git files
** most import file is the config**

## Commit changes
commit = tell git to track changes to comitted files. 
## Viewing commit messages
git log helps viewing all the commits. 
git log 
options: 
n <0> : number of commit messages needs to be returned
since=<date> : return commits only after certain date
until=<date>
author=<name>
grep="search terms" : greps commit messages. 
 
 
 ## Git architecture has three stages:
 1.remote
 2.local repo
 3. staging index. 
 Commits from local go into staging and then to remote. Pulls go directly from remote to local. 
 
 Changes to files are stored as change sets. Only changes rather than the whole different versions are stored. Each commit/change set is referred by a  SHA hash.
 
 ### HEAD pointer
 Head points to the latest changes in the currently checked out repository. 
 It points to latest commit. 
 
## Status
shows a list of untracked files and modified files which are added to the staging index. 
* git status 

## View changes made to files. 
1. To view changes in working directory use: 
    * git diff or git diff <modified_file_name>
2. To view changes between the staged index and repository use: 
    * git diff --staged <file_name> 

### Delete/move/rename files through git. 
If we do it through normal fs we need to add to stage and commit. If done through git 
then they directly get added to the staging index. 
    * git rm <file_name>
    * git mv <fil_path_old> <new_file_path>

## Undoing Changes
### Undoing working directory changes
```git 
git checkout <branchName> <fileName> 
<branchName> could be any branch name. 
```
Above command resets changes in the working directory to reflect those present in the branch <branchName>. 
 
### Unstaging files
If unintended files are staged use the reset's mixed mode to reset to a previous commit. ( by default to HEAD)

 
 
 
 
