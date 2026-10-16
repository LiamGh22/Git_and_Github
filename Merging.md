Merging:
Branching makes it super easy to work withhin selfcontainde contexts, but often we want to incorporate changes from one branch into another!
we can do this using the command git merge command

the mege command can sometimes be confusing for students early on. remember these two merging concepts:
we merge branches, not specific commits
we always merge to the current HEAD branch

Fast-forward-merge:
to merge follow these basic steps:
1. switch to the branch you want to mege the changes into.
2. Use the git merge command to merge changes from a specific branch into the current branch.

------------------------------
what if we add a commit on master?
this happens all the time! imagine one of your teammates merged in a new feature or change to master while you were working on a branch

if there is no conflict you can merge the branches as same as before
but if we have conflicts:

HEADS UP:
Depending on the soecific changes you are trying to merge, git may not be able to atomaticlly merge.
this resilt in merge conflicts, which you need to manually resolve.

CONFLICT(content): merge confilct in blah.txt automatic merge failed; fix conflict and then commit the result

when you encounter a merge conflict, git warns you in the console that it could not automatically merge.
it also changes the contents of your files to indicate the conflicts that it wants you to resolve.

Conflict markers:
the content from your current HEAD is displayed between the <<<<< HEAD and =======

resonlving the conflicts:
whenever you encounter merge conflicts, follow these sreps to resolve them:
1. open up the file with merge conflict
2. edit the fiel to remove the conflicts. decide which branch's content you want to keep in each conflict. or keep the content feom branch.
3. remove the conflict "markers" in the dokument
4. add your changes and then make a commit

look at the musics-file

