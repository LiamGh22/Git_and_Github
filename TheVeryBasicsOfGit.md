A git repository is a workspace which tracks and manages files within a folder.

anytime we want to use git with a project, app, etc we need to create a new git repository. we can have as many repositories on our machine as needed. all with seperated histories and contents.
------------
our first git command:

git status gives information on the current status of a git repository and its contents.

creating a repositoriy:
Use git init(initiolize) to create a new git repo. before we can do anything git-related, we must initialize a repo first.

this is something we do once per project.
initiolize the repo in the top-level folder containig your project.

it crates a hidden file .git , which stores erverthing of our repo.
----------------
Warning: do not init a repo inside of a repo.
before running git init, use git status to verity that you are not currently inside of a repo.

--------------
commiting:
making checkpoints.
the process looks like this:
work on stuff -> add changes -> commit


--------------------
we use the git add command to stage changes to be commited.

it is a way of telling git please inculde this changes in our next commit.

working directory ->(git add)-> staging area ->(git commit)-> repository
