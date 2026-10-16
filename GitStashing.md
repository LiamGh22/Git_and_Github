Stashing=lagern

git provides an easy way of stashing these uncommited chhanges so that we can return to the m later, without having to make any unnecessary commits.

git stash is super useful command that helos you save changes that you are not yet ready to commit. you cna stash chabges and then come back to them later.

running git stash will take all uncommited changes and stash them, reverting the changed in your working copy.

using git stash pop to remove the most recently stashed changes in your stash and re-apply them to your working copy.

stash apply:

you can use git stash apply to apply whatever is stashed away, without removing it from the stash. this can be useful of you want to apply stashed changes to multiple branches.

----------
stashing multiple times:
you can add multiple stashes onto the stack of stashes. they will be stashed in order you added them.

you can see what is in your stash with 
git stash list

git assumes you want to apply the most recent stash when you run git stash apply, but you can also specify a particular stash like git stash apply stash@{2}
-----------------------
Dropping and clearing stashes:
to delete a paticular stash, you can use git 
stash drop <stash-id>


to clear out all stashes, run:

git stash clear
