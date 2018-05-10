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
 4.

## Commiting files to git. 
1. Add files to local repo and to the stage
git add . 
2. Commit the staged files.
git commit -m "message"
3. Push to remote repo.
git push origin remote


