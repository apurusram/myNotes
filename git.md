# Working with git branches

# Create a branch called "quickfix" and move to that branch
git checkout -b quickfix

# stage changes
git add *

# Commit changes
git commit -m "msg"

# list branches
git branch

# rename branch
git branch -m <oldname> <newname>

# delete branch
git branch -d <branch>

note: you need to checkout before you delete nad if you have not merged changes, you will get a warning

# force delete
git branch -D <branch>

# MERGING 
- Target: master 
- Source: branch

# merge branch
git checkout <target-branch>
git merge <source-branch>

# compare branch
git diff <branch1> <branch2>

# REBASE 
- clean up local history - focus on end result
- increase accuracy and clarity
- draft vs final copy

Conditions:
* Do not use rebase on a public branch (can cause confusion and lose work)

Scenarios:
- Clean up your local history before sharing a branch
- Pull changes from a branch into your branch without performing a merge

Example:
Squash commits into one commit

Rebase creates a copy of your commits to change the parent

# steps for rebase
# see branch history
git log --oneline
# get the original base of the "ticket1" branch created from master
git merge-base ticket1 master
# start rebase from the commit sha
git rebase -i <commit-sha>
# squash the commits you want to combine into a single commit (git-rebase todo file will be opened)
pick 1285e6c starting f1
squash b714e68 more work in f1
squash 985d1e1 completed f1
# choose the commit message you want to use
..first msg
..second msg
..third msg
# pull in changes from master then replay branch commits after
git rebase master

# rebase log
git reflog





