---
title: Git Commands
date: 2020-04-09 07:26:58
tags:
---

git stash

git stash pop

git stash list

git stash apply xxxx

git commit -m "your commit" --no-verify  
> This option bypasses the pre-commit and commit-msg hooks.

git reset --merge
> Resets the index and updates the files in the working tree that are different between <commit> and HEAD, but keeps those which are different between the index and working tree (i.e. which have changes which have not been added).

git log --oneline -10

git show xxxxx

git pull -r

git push --force-with-lease
> --force-with-lease alone, without specifying the details, will protect all remote refs that are going to be updated by requiring their current value to be the same as the remote-tracking branch we have for them.