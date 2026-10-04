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
we use the git add command to stage changes to be commited.

it is a way of telling git please inculde this changes in our next commit.

working directory ->(git add)-> staging area ->(git commit)-> repository


--------------
commiting:
making checkpoints.
the process looks like this:
work on stuff -> add changes -> commit

we use git commit command to actually commit changes from the staging area.
git commit -m "your massage"

when making a commit we need to provide a commit that summarizes the changes and work snapshonted in the commit
--------------------
git log command:
it just a command like git status.

--------------------------

with the command git add . to stage all changes at once.

--------------------
an Example of the difference between git add and git commit:

groseriy shopping:
with git add you can add good to your basket or remove them from it.
but with git commit your bisket is ready to final pay.

-------------------------
## Git Workflow Example: `git add` vs `git commit`

Imagine you are developing a system for an autonomous vehicle and you have modified **10 files** at the same time:
*   **5 files** are for LiDAR sensor integration (e.g., `lidar_read.py`, `config.yaml`).
*   **5 files** are for YOLO object detection (e.g., `yolo_detect.py`, `network_config.json`).

Instead of saving everything together, you want to keep your project history organized. Here is how you do it:

### 1. Stage the LiDAR changes
First, you only select the 5 files related to the LiDAR sensor and move them to the Staging Area. 
```bash
git add lidar_read.py config.yaml

2. Commit the LiDAR changes

Now, you save those staged files permanently to the repository history.

git commit -m "Add LiDAR sensor integration"

3. Stage the YOLO changes

Next, you prepare the remaining 5 files for the object detection feature.

git add yolo_detect.py network_config.json
4. Commit the YOLO changes

Finally, you save the YOLO files as a separate snapshot.

git commit -m "Implement YOLO object detection"