# git-basics

## What is Git?

Git is a version control system. It is designed to make it easier for teams to collaborate by tracking a project's history of changes.

Each addition to a project is made by a collaborator in a unit of change called a **commit**. These commits are linked together to represent the history of changes made to a project. 

A collection of these commits that tracks the change history for a project is called a **repository**. Below is a diagram representing a repository with three commits.

![repository with three commits](/images/diagram-1.png)

Each commit tracks:
* What changes were made
* When the changes were made
* Who made the changes
* Why the changes were made

## Git vs. GitHub

*GitHub* hosts *git* repositories remotely on the cloud. 

Each contributer to a project has a local copy of the project's repository. The contributor commits changes to their local repository, and then **pushes** those changes to the remote repository on GitHub. Then, other contributors can **pull** these changes into their local repository. 

By using this system of pushing and pulling, all collaborators are able to stay up to date with each others' work.

## A Basic Git Workflow

### Cloning a repository

A contributer makes their local copy of the project's repository by **cloning** it. To clone a repository, navigate to the directory in which you'd like to store the project's directory, and then run:

`git clone https://github.com/username/repo-name.git`

You can find the actual URI by clicking on the green "Clone or Download" button in on the top right corner of the repository's page on GitHub, under the "Code" tab.

After running this line, you should see a new directory containing the repository that you just cloned.

The diagram below shows the local and remote repositories that exist after the clone.

![local and remote repositories](/images/diagram-2.png)

### Making changes locally

Now the contributor is ready to make changes. They can simply begin by editing the files they wish to edit. Once they've made the desired changes, it is time to add those changes to their local repository as a commit.

1. `git status` - Shows the status of the repo (what changes need to be committed, what files are untracked, etc).

2. `git add [files]` - **Stages** changes for commit. This step allows the contributor a chance to review the changes they are about to commit.

3. `git status` (again) - Now, files staged for commit should show up in green. The contributor double checks what they are about to commit.

4. `git commit -m "commit message"` - Commits the changes. The commit message should describe in present tense the changes that were made (eg. "add specific functionality", or "fix specific bug")

The diagram below shows our local and remote repositories after the contributor has made their commit locally. The new commit is in red.

![local commit](/images/diagram-3.png)

### Pushing changes to remote

The contributor has made their change locally, but for this change to be accessable to other contributors, it must be **pushed**. The contributor can push their changes with:

5. `git push`

Now, the repositories look like this.

![repos after push](/images/diagram-4.png)

Once the changes are pushed to the remote repository, other contributors can **pull** the new changes.
