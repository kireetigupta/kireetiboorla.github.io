---
layout: post
title: Git commands, tips & tricks.
category: tutorials
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
-n <0> --> number of commit messages needs to be returned
--since=<date> --> return commits only after certain date
--until=<date>
--author=<name>
--grep="search terms" --> greps commit messages.


 ## Git tree strucutres
 Git architecture has three stages:
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
```git
git reset HEAD file_name
```
### Amending commits
If needed to add some changes to the previous commit use --amend
```git
git commit --amend -m "message"
```
### Reverting to old commits.
To revert to any commit using the sha has :
```git
git revert <commit_id>
```

### Reseting to undo commits.
There are three types of reset.
1. Soft : reverts head repo to specified commit and doesn't impact staging index and working dir.
2. mixed: this is the default option. Copies changes to repo and staging index.
3. hard: copies changes to repo,staging index and the working directory.
```git
git reset --mode <commit_id>
```
### Removing untracked files.
To untrack files that are not important use the clean option. '-n' is just to show what would be cleaned. '-f' forces the clean operation to be impacted.
```git
git clean -f/-n
```

## Ignoring Files
.gitignore will have rules to specify which files to ignore.
* Basic regex can be used to specify the rules.
 * ? [a-z] [0-9]
 * ! -> to negate the exp
 * assets/videos/ --> tells to ignore files in this dir.

You can find standard gitignore files online.
We can set a global gitignore and set it using the config commands.
If there are files already comitted to untrack them, delet it from git's cache.
git rm --cached <fileName>

 ## Commit Tree
 tree-ish
 we can use the below to identify commits.
 * full SHA-1 hash
 * HEAD pointer
 * branch reference, tag reference
 * ancestry by using the above first. (HEAD^,acf8793^) or (HEAD~1)

We can use any of the above to refer to a branch and use commands related to commits.

To view files in a commit: git ls-tree <tree-ish>

To compare two commits:  
git diff <tree-ish1> <tree-ish2>
Many other options such as ignoring white space etc are present.


## Branches
### Creating a branch
git branch <branch_name>
### Switching branch
use checkout to switch between branches.
```git
git checkout <branch_name>
```
###
