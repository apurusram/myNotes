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
