Atomic commits:
when possible a commit should encompass a single feature chanfe or fix. in other works, try to keep each commit focused a single thing.

this make it easier to undo or rollback changes later on. it also makes your code or project easier to review.

do commiting smart. that is everything. :) .

from the Git Docs:
describe your changes in imperative mood, e.g. "make xyzzy do frotz" insted of i changed....

-----------------
running git commit will commit all staged changes. it also pens up a text editor and promots you for a commit massage.
this can be overwhelming when you are starting out, si instead you can use.

if you type git commit it will show up an editor like nano 
in the website below from git doc you can change your editor:
https://git-scm.com/book/en/v2/Appendix-C%3A-Git-Commands-Setup-and-Config

if you want to change your editor to vs code ust type this line in your terminal:
	
git config --global core.editor "code --wait"
-------------------------------------
A closer look to git log command:

git log --oneline

this is a shorthand for "--pretty=oneline --abbrev-commit" used together.
--------------------
commiting with GUI.
is really easy.
--------------------

Amending commits
suppose you just made a commit and then realized you forgot to include a file! Or, maybe you made a typo in the commit message that you want to correct.
rather than making a brand new seperate commit, you can "redo" the previous commit using the --amend option
it just work if you made a mistake just one commit ago.

--------------------
Ignoring files:
we can tell Git which files and directories to ignore in a given repositoey, using a .gitignore file.
this is useful for files you know you never wantto commit, includeing:
secrets, API keys, credintials, etc.
Operating system files
Log files.
Deonedicies and packages

.gitignore:
crate a file called .gitignore in the root of a repository. iside the file, we can write patterns to tell Git which files and folders to ignore:
DS_STORE will ignore files named .DS_Store
*.log will ignore any files with the .log extention
foldername/ will ignore an entire directory



