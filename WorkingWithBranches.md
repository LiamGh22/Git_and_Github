Branches 
think of branching as alternative timelines for a project.
they enable us to create seperate context where we can try new things or even work on multiple ideas parallel.
if we make changes on one branche they do not impact the other branches(unless we merge the changes).
merge = verschmelzen, vereinigen
----------------------------------
master Brache:
In Git we are always working on a branch the default brache name is master.

it does not do anything soecial or have fancy powers. it is just like any other branch.

many people designate the master branch as their source of truth or the officail branch for their codebase, but that is left to you to decide.
from git's prespective, the master branch is just like any other branch. it does not have to hold the master copy of your project.

in 2020 github renamed the default branch from master to main. the default git branche is still master, though the git team is exploring a potential change.

--------------------------
HEAD -> master

HEAD:
we will often come across the term HEAD in Git.
HEAD is simply a pointer that refers to current location in your repository. it points to a particular branch refrence.

so far, HEAD always points to the latest commit you made on the master branch, but soon we will see that we can move around and HEAD will change!

------------------------------

Viewing branches:
use git branch to vieew your existing branche.
the default branch in every git repo is master, though you can configure this.

look for the * which indecates the branch you are currently on.
-------------
creating and switching branches: 
use git branch <branche name> to make a new branche based upon the current HEAD.

this just crates the branch. it does not switch you to that branch(the HEAD stays the same)

Swichting branches:
once you have created a new branch, use git switch <branch-name> to switch to it.

more practice with branching:
it is really important where you make a branch.
based upon the current HEAD, you will have different branches.
----------------------------------------------
Another way of switching??
Historiclly we used git checkout <branch-name> to switch branches. this still works.

the checkout command dies a million additional things, so the decition was made to add a standalone switch cammand which is much simpler.

you will see older tutorials and docs using checkout rather than switch. both  now work.

git checkout <branch-name>

Creating and switching at the same time:
use git switch with the -c flag to crate a new branch and switch to it all in one go.
-c stands for create


git switch -c <branch-name>

-----------------------------------------------
switching branches with unstaged changes?
if you make changes in branch and wants to switch to onother branch you have to add and commit it.
otherweis you will get an error.
sometimes it is ok and changes will be follow you everywhere.

--------------------------------------------------
Deleting and renaming branches:

git branch -d <branch-name>
-d = --delete
-D = --delete --force
(You can not delete from the branch)

for renaming:
git branch -m <branch-name>
-m = --move 
(you have to be on the branch to rename it)
------------------------------------------------


