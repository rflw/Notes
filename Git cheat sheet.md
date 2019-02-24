# Git Cheat Sheet

## History review

`git log`  
Lists version history for the current branch

`git log --oneline --graph --all`  
Lists version history for all branches with graph



## Make changes

`git add -A`  
Stage **all** (new, modified, deleted)

`git add .`  
Stage **all** (new, modified, deleted)

`git add -u`  
Stage **modified** and **deleted**

`$ git diff`  
Shows file differences not yet staged

## Group changes

`git checkout -b <branch-name>`  
Create branch **and** checkout, shortcut for `git branch <branch-name>; git checkout <branch-name>`

`git branch <branch-name>`  
Create branch

`git branch`  
List branches

`git checkout <branch-name>`  
Switch to branch

`git branch -d <branch-name>`  
Delete the specified branch

`git merge <branch-name>`  
Merge `<branch-name>`  into current

`git cherry-pick <commit-1> <commit-2> ..`  
Move small code patches across branches

## Reversing changes

`git reset`  
Reverts changes by moving a branch reference backwards in time to an older commit. 
In this sense you can think of it as "rewriting history;" `git reset` will move 
a branch backwards as if the commit had never been made in the first place.  
EXAMPLE: `git reset HEAD~1`

`git revert`  
While resetting works great for local branches on your own machine, its method 
of "rewriting history" doesn't work for remote branches that others are using.  
EXAMPLE: `git revert HEAD~` 