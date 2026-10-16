Git Diff:
we can use the git diff command to view changes between commits, branches, files ,our working directory and more!

we often use git diff alongside commands like git status and git log to get a better picture of a repository and how it has changed over time.

git diff 
without any additional options, git diff lists all the changes in our working direltory that are not staged in the next commit.

git diff HEAD:
list all changes in the working  tree since last commit.
if you di the add command git diff doesn't work anymore.
-----------------------------

git diff --staged 
or
git diff --cached

changes between the staging area and our last commit
"show me what will be included in my commit if i run git commit right now"

diffing specifc files:

git diff HEAD [filename]
git diff -- staged [filename]

we can view the changes within a specific file by providing git diff with a filename.

comparing Branches:

git diff branch1  branch 2
will list all the changes between the tips of branch1 and branch2


comparing commits:
git diff commit1 commit2
use the git log --oneline to get the commit number
git diff c8ff6b5 6a8bf25


to compare two commits, and see what has been changed between thoes two commits.



