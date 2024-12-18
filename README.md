# What is Git?
- ### Git is a distributed version control system or tool that allows you to track, manage, and control changes to your project's files over time.
- ### The real power of Git lies in its ability to save each change (commit) you make to your project's files by keeping a history of changes, allowing you to revert to any previous version if needed.
- ### It enables multiple people to collaborate on a project.
- ### [Git Book](https://git-scm.com/book/en/v2)

## Commands
- Most Git commands starts with git keyword to tell the system that you are using Git.
- First, ensure that Git is installed successfully by running the git --version command.
- Let’s start by configuring Git for global use or for hosting services like GitHub, so let's move on to the first command, git config.

## git config
- Set username and email in Git
- Git requires a username and email to identify the author of each commit.
- Use global configuration if you want to use the same username and email across all your Git repositories.
  - git config --global user.name "Your Name"
  - git config --global user.email "your_email@example.com"
- Use specific repository configuration If you want to use a different username and email for a specific project, navigate to the project directory and run
  - git config user.name "Your Name"
  - git config user.email "your_email@example.com"
- To check that the information was set correctly for global configuration, you can use
  - git config --global user.name
  - git config --global user.email
- Or, to check the configuration in the current repository
  - git config user.name
  - git config user.email

## After username and email configuration
- Navigate to your project directory in the CLI.
- Now I am in a local project; where the Git is? To let Git start working on your project, you have to use the git init command to initialize or create a repository to include the project's files in Git, so let's start with the first command, which is git init.

## git init
- Create an empty Git repository or reinitialize an existing one.
- Hint: After creating the repository, Git will add a hidden .git folder to your project. This folder contains all the files Git needs to track your project’s history and changes.
- Now we have created a repository, we are in need to start adding and tracking project files. Let's move on to the second command, which is git add.

## git add file-name, * or .
- Start tracking specified project files.
- Once you have created a Git repository, your project files will be untracked by the Git. To let Git start tracking project files, use the git add command to let it track files.
- Using * or . instead of file-name will let all project files be tracked.

## git rm --cached file-name
- Removes the specified file from Git's tracking without deleting it from your working directory, effectively making it untracked.
- Then the project files either tracked or untracked so we are in need for command to check the status of project files. Lets move on to the next command, which is git status.

## git status
- Show the status of files, either tracked or untracked.
- Also showing if tracked files are modified or unmodified (at the staging area to be committed).
- Once you have done all the changes, you will need to save or make a checkpoint for changes that have already been made, so we will jamb to the next command, which is git commit.
- Hint: You can add a .gitignore file to your project and list any files or directories you want Git to ignore. To ensure Git ignores a file listed in .gitignore, make sure the file is untracked or remove it from tracking using git rm --cached file-name. If you want to ignore a group of files with the same extension in your .gitignore file, use *.extension.

## git commit -m "leave a message describes what you did in this commit"
- A commit in Git records the latest changes to the repository, saving them in the project’s history.
- Each commit represents a version of your project, saved in the history of changes, allowing you to revert to it if needed.

## git log
- Displays a complete history of all commits made in the project, showing details like commit hashes, author names, dates, and commit messages.

## git checkout commit-hash or branch-name
- Switches to a specific branch or a specific commit.
- When checking out a branch, you switch to the latest commit on that branch.
- When checking out a commit, you enter a "detached HEAD" state, where you can view or work from that point in the project history, but changes won't be associated with any branch unless you create a new branch from it.

## git checkout -b branch-name
- Creates a new branch with the specified name and immediately switches to it.

## git branch
- List, create, rename, or delete branches
- git branch
  - List all branches.
- git branch branch-name
  - create branch with the given name.
- git branch -M new-branch-name
  - Renames the current branch to the new given name.
  - The -M flag forces the rename, even if there’s already a branch with that name.
- git branch -m old-branch-name new-branch-name 
  - Renames the specified branch to the new branch name without needing to switch (checkout) to it first.
- git branch -d branch-name
  - Deletes the specified branch from your local repository. Note that this command only works if the branch has been fully merged; otherwise, Git will prevent the deletion to avoid losing changes.

## git merge branch-name-to-be-merged
- Merges the specified branch into the current branch, combining the changes from both branches.

## git remote add remote-name url-of-remote-repo
- Adds a remote repository with the specified name and URL, allowing you to connect your local project to a remote repository

## git remote -v
- Displays the names and URLs of all remotes associated with the repository, showing whether each URL is used for fetching or pushing.

## git push -u origin main
- Uploads (pushes) changes from the local main branch to the remote main branch on the remote repository named origin. The -u flag sets the upstream branch, so future git push commands can be used without specifying the branch name.

## git pull origin main
- Downloads (pulls) the latest changes from the remote main branch on origin and merges them into your local main branch, keeping your local branch up-to-date with the remote.

## git clone url-of-remote-repo
- Creates a local copy of a remote repository, including all its files, branches, and commit history.
