## GIT COMMAND AND DESCRIPTIONS NOTES

Git is free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

### Advantages

- Tracking Changes
- Managing project code
- Working with multiple members

### Setup

- Download Git from [Git](https://git-scm.com/downloads)
- Create a Github account

### Configurations

- Set the email and username with below commands. Needed for tracking, which commit is by whom. (--global: When you want a default Git configuration across all projects, --local:When you want different Git settings for different projects )

`git config --global/local user.email="example@email.com`

` git config --global/local user.name="user name"`

- To check the configurations

` git config list`

### Lifecycle
![Git Lifecycle](https://miro.medium.com/max/552/1*J1qnVEUXzoDgROobmjjR_Q.png)

[Image source](https://miro.medium.com/max/552/1*J1qnVEUXzoDgROobmjjR_Q.png)


### Commands 
- To initialize a new Git repository in a directory.
A .git directory is created inside your project folder. This directory contains all the metadata required for version control.
` git init `

- Moves changes from the working directory to the staging area.
Is used to stage changes in Git, preparing them for a commit. It tells Git to include specific files or changes in the next commit.
` git add filename`

` git add . `
- Save Staged Changes to Git History
Records staged changes into the repository's history.

` git commit -m "commit message , one liner for changes done" `

` git commit --amend  # modify the last commit message`

- Rename the Current Branch to main
This command renames the current Git branch to main,-M (move) forces the rename, even if a branch named main already exists.
` git branch -M main`

- Link Local Repository to Remote
This command connects your local Git repository to a remote repository.

` git remote add origin link `

` git remote -v # list the remote links` 

` git remote rm origin `

- Push Local Changes to Remote Repository
This command uploads your local branch (main) to the remote repository (origin) and sets it as the default upstream branch.
-u or --set-upstream → Links the local main branch to the remote main branch.
After this, you can simply use git push next time (without specifying origin main).

` git push -u origin branchname`

` git push `

- Check the Current State of Your Repository
The git status command shows the current status of your working directory and staging area. It helps you track:
- Untracked files (new files not yet added to Git)
- Changes staged for commit
- Changes not staged for commit
- The current branch and its relationship with the remote repository

` git status `

- View Commit History
The git log command displays a list of commits in your repository, showing useful details such as:

- Commit hash (unique ID)
- Author
- Date
- Commit message

` git log `

` git log --oneline # one line history log`

-
` git pull `

-

` git restore --staged filename`

-

` git rm --cached filename `

-
` git diff `

-

` git stash `

` git stash pop `

` git stash list `

` git stash clear `

` git stash save 'tag'`

` git stash apply tag`

# Branches

-
` git branch branchname `
-
` git checkout branchname `

-

` git merge branchname `

-

` git branch -d branchname `

-
` git push origin --delete branchname`
-
` git pull origin branchnamr`
-
` git checkout -b branchname `

-
` git branch -v # -v local branches -r remote branches `
-
` git branch list `
-
` git branch --merged `
-
` git branch -D branchname `

# Rebase

-
` git rebase feature `
-
` git rebase --continue `

# Squash
-
` git rebase  -i HEAD ~ 4 `
# Revert 
-
` git revert HEAD ~2 `

# Reset
-
` git reset --soft HEAD ~ index # starts with 0 `
-
` git reset --hard HEAD ~ index `

# Tags & Release

-
` git tag tagname `
-
` git push origin tagname `

# Fork
A fork is a personal copy of someone else's Git repository. It allows you to:

- Experiment with changes without affecting the original repo.
- Contribute to open-source projects by making changes in your fork and submitting a pull request.
- Maintain a separate version of a project with your modifications.

### How to Fork a Repository


1️⃣ Go to the Repository

Visit the GitHub repository you want to fork.

2️⃣ Click the "Fork" Button


This creates a copy of the repository under your GitHub account.


3️⃣ Clone the Forked Repository to Your Local Machine


`sh
git clone https://github.com/your-username/forked-repo.git
cd forked-repo`

4️⃣ Add the Original Repository as a Remote (upstream)

`sh
git remote add upstream https://github.com/original-owner/original-repo.git`
- origin refers to your fork.
- upstream refers to the original repo.
Keeping Your Fork Updated

1️⃣ Fetch Changes from the Original Repo


`sh
git fetch upstream`

2️⃣ Merge Changes into Your Fork

`sh
git checkout main
git merge upstream/main`

3️⃣ Push the Updates to Your GitHub Fork
`
sh
git push origin main`


# How to avoid some file from being tracked by VC
A .gitignore file tells Git which files and directories to ignore (i.e., not track or commit). This is useful for:
- Temporary files (logs, caches)
- Environment-specific files (config, secrets)
- Dependency folders (e.g., node_modules/)
- Compiled files (e.g., .class, .o, .exe)

Create a file named .gitignore in the current directory.
.gitignore file .[Refer these repo for writing .gitignore files for different Framework/Programming Language](https://github.com/github/gitignore) 




