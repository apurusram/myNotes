# You give the command git checkout master. What is HEAD now pointing to?
The branch master

# Where do Git branches point?
To a commit

# What is the difference between git branch -m and git branch -M?
git branch -m will rename a branch and the corresponding reflog, whereas git branch -M will force the renaming of the branch, even if a branch with the new name already exists.

# After writing hooks to enforce policy on the server side of a Git instance, why is it necessary to write and manage client-side hooks that are copies of the same policy enforcements?
To catch any potential violations before you run the server-side hooks, to provide a meaningful warning to the user when performing Git operations

# What is the difference between annotated and non-annotated tags?
Annotated tags can hold extra information about themselves (tag metadata, release notes, security signatures), whereas non-annotated tags serve just as a pointer for a commit. 

# Which best describes the difference between log and diff commands?
log will output the latest commits in a specified format and diff will take two inputs and output their differences.

# Which URL protocols would you use when fetching a Git repository?
Secure Shell (SSH), Git, and HTTP

# Which statement is the best comparison between git log and git blame?
git blame shows only the latest change in the file, whereas git log can show the entire branch history.

# Which command adds a file to the index?
git add

# What is the purpose of the git clean command?
To delete untracked files from the repository's working directory

# You give the command git checkout master. What is HEAD now pointing to?
The branch master

# If you make a hotfix on a release (stable) branch, what actions must you take on other branches, for example, integration or feature?
Replicate the changes by rebasing, cherry-picking, or merging.

# While on branch main, you give the command git merge branch1. Which branch or branches change?
main

# What happens during a Git fast-forward?
Git moves the working branch pointer forward to the latest commit of the merging branch because there is no divergent work to merge together.

# How can you move to another branch while discarding all uncommitted changes?
Use git checkout --force.

# What is the difference between git branch -d and git branch -D? 
git branch -d will delete a branch, given that it has been properly merged, whereas git branch -D will allow the deletion of the branch irrespective of its merged status.

# What is the difference between git checkout and git reset?
git checkout allows you to navigate between branches or to restore working tree files, whereas git reset moves both HEAD and branch pointers to a previous commit.

# You add *.txt to your .gitignore file. You commit the changes to the .gitignore, but Git is still tracking a file named notes.txt. Why?
The *.txt pattern does not apply to previously tracked files.

# What is the difference between using git restore for a single file and the git clean command?
Restoring a file with git restore changes the file in the working directory to its state in the staged area, whereas git clean removes any untracked files from the working directory.

# Which command will you use to move to an existing branch named mybranch?
git switch mybranch

# You create a new branch using the git branch mybranch command, but you do not check it out. What occurs when you next commit?
Git creates a new commit, but mybranch stays on the previous commit.

# Which term defines Git repositories that are included as subdirectories in another repository?
Submodules

# Which kind of files can you use in Git for version control?
Text and binary files