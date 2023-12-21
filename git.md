# 3 stages
Committed
Modified
Staged

# 3 states:
working directory
staging area (index)
.git directory (repo)

# print working directory
pwd

# change working directoR
cd

# list files
dir

# create new directory
mkdir

# git config
git config --global user.name ""
git config --global user.email ""
git config --global user.password ""

# check config settings
git config --list

# initialize a git repo
cd to project directory
git init

# pull code and setup local branch
git clone <url>

# default name for remote server
origin

# provide name for remote server
git remote add <name> <remote-url>

# list remotes and URLs
git remote -v

# fetch and compare
git fetch

# fetch and merge
git pull

# push changes (resolve conflict first)
git push

# track changes of branch
git checkout --track origin/branch_name

# changed and not staged for commit
git diff 

# changed and staged for commit (git commit)
git diff --cached

# changed since last commit (git commit -a)
git diff HEAD

# specific commit and current
git diff <commit>

# specific commit and staged
git diff --cached <commit>

# difference between two commits
git diff <commit> <commit>

# difference tips of branches
git diff feature master

# changed in master since featue was started off of it
git diff feature...master

# difference in file.txt on 2 branches 
git diff feature master file.txt

Example:
diff --git a/example.txt b/example.txt

- label a and b for files being compared
- index 747e2b3..8ef0a69 10044 (git hash of a ..b files permission)

# see file
git show <hash>

file markers:
-- a/example.txt
+++ b/example.txt

a file marker: ---
b file marker: +++

@@ -3,6 +3,7 @@

@@: markers for chunk header
-3,6: 6 lines of file a starting at line 3
+3,7: 7 lines of file b starting at line 3
Lines with no file marker are the same in both and b







# WORKING WITH GIT BRANCHES

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

# cherry-pick commits
# find the commit you want
git log --oneline
git log <branchname> --oneline
# where do you want to commit? Checkout to that branch
git checkout <branchname>
# perform the cherry-pick to append the commit to HEAD
git cherry-pick <commit>





