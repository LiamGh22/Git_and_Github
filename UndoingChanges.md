git chechout command is like a git swiss army knife.
many developers think it is overloaded, which is what lead to the additional of the git switch and git restore commands.

we can use chechout to create branches, switch to new branches, restore files and undo history!

we can use git checkout <commit-hash>
to view a previous commit.

remember, you can use the git log command to view commit hashes. we just need the first 7 digits of a commit hash.

Detached (losgelöst) HEAD:
you have a cople options:
1. stay in detached head to examine the contents of the old commit. poke around, view the files, etc,.
2. leave and go back to whereever you were before- reattach the HEAD.
3. create a new branch and switch to it. you can now make and save changes, since HEAD is no longer detached.

if you checkout an old commit and decide you want to returen to where you were before just switch back to whtever branch you were on before.
if we do the git checkout <commit hash>:
the HEAD point to that commit und not to the branch adress anymore.

but we can di git checkout <commit hash> and then we can initiolaize a new branch there, so we start working from that commit.
------------------
git checkout supports a slightly add syntax for refrencing previous commits relative to a particular commit.

git checkout HEAD~1


HEAD~1 refer to the commit before HEAD(parent)
HEAD~2 refer to the 2 commits before HEAD(grandparent)

it is not essential :)
---------------------

Discarsing changes :

git checkout HEAD <file>

suppose you've made some changes to a file but don't want to keep them. to revert the file back to whatever it looked like when you LAST COMMITED , you can use:

git checkout HEAD <fielname> to discard any changes in that file, reverting back to the HEAD.

another option 
here is another shorter option revert a file...

rhther than tyoing HEAD, you can subtitute -- followed by file(s) you want to restore

git checkout -- <file>

-------------------
Restore:
git restore is a brand new Git command that helps with undoing operations.

beacuse it is so new, most of the existing git tutorials and books do not mention it, but it is worth knowing!

recall that git checkout does a million different things, which many git users find very confusing. git restore was introdued alongside git switch as alternitives to some of the uses for checkout.

unmodifying files with restore:
suppose you have made some changes to a file since your last commit. you have saved the file but then realize you definitly do not want those changes anymore!
to restore the file to the contents in the HEAD, use git restore <filename>

git restore, restores using HEAD as the default source, but we can change that using the --source option.

for example, git restore --source HEAD~1 home.html will restore the contents of home.html to its state from the commit prior to HEAD. you can also use a particular commit hash as the source.

git restore --source HEAD~1 app.js

--------------------------

unstaging files with restore :
if you have accidentlly added a file to your staging area with git add and you don't wish to include it in the next commit, you can use git restore to remove it from staging.

use the --staged option like this:
git restore --staged app.js

------------------
Git Reset 
suppose you have just mafe a couple of commits on the master branch, but you actually meant to make them on a separate branch instead. to undo thoes commits, you can use git reset.

git reset <commit-hash> will reset the repo back to a specific commit. the commits are gone

it just remove the commits and not the changes

---------
git reset --hard <commit-hash>

if you want to undo both the commits and the actual changes in your files, you can use --hard option.

for example, git reset --hard HEAD~1 will delete the last commit and associated changes

-------------------
git revert:

git revert is similar to git reset in that they both undo changes, but they accomplish it in different ways.
git reset actually moves the branch pointer backwards, eliminating commits.

git revert instead creates a brand new commit which reverser/undos  the changes from a commit. because it results in a new commit, you will be prompted tp enter a commit message.

git revert <commit-hash>
--------------
anyone can clone a repo from github, provided the repo is public. 
-----------
SSH Keys
you need to be authenticated on github to do certain operatios, like pushing uoo code from your local machine. your terminal will prompt you every single time for your github email and password, unless...
you generate and configure an ssh key! Once configured, you can connect to github without having to supply your username and password.
-------------------------------

creating our firts github repo:

option1:
if you already have an existing repo locally that you want to get on github....
create a new repo on github
connect your local repo (add a remote)
push up your changes to github

Option2:
if you havent begun work on your local repo, you can...
crate a brand new repo on Github 
clone it down to youre machine
do some work locally 
push up your changes to github

Remote:::
before we can push anything up to Github, we need to tell Git about our remote repository on github. we need to setup a destination to push up to.

in git we refer to these destinations as remotes. each remote is simply a URL where a hosted repository lives.

to view any existing remotes for your repo, we can run git remote or git remote -v(verbose for more infos)

this just displays a list of remotes. if you have not added any remotes yet you wont see anything

Adding a new remote
a remote is really two things: a URL and a lable. to add a new remote, we need to provide both to Git.
git remote add <name> <url>
a really standard name is origin
okay Git, anytime i use the name origin, i am referring to this particular Github repo URL.

renameing the remote with :
git remote rename <old> <new>
removing a remote with this command:
git remote remove <name>
----------------------------------------
Pushing:

now that we have a remote set up, lets push some work up to github! to do this, we need to use the git push command.

we need to specify the remote name we want to push up to and the specific local branch we want to push up to that remote.

git push <remote> <branch>

check that you are copying the SSH URL and not the https URL.

we can push any branch:
the same commad just use the new branch name
------------------
while we often want to push a local branch up to a remote branch of the same name, we do not have to!
to push our local pancake branch up to a remote branch called waffle we could do :
git push origin pancake:waffle
----------------------------

the -u option
the -u option allows us to set the upstream o the branch we are pushing ypu can think of this as a link connecting our local to a branch on github.

running git push -u origin master sets the upstream of the local master branch so thtat it tracks the master branch on the origin repo.

what this means ....
Once we have set the upstream for a branch, we can use the git push shorthand which will push our current branch to the upstream.

git push -u origin master and next time we can run => git push
------------------------------

Option 2:
start from scratch

we have to make a new repo in github and clone it down to our machine

------------







