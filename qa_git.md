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