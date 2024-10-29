# What is Git?
- ### Git is a distributed version control system or tool that allows you to track, manage, and control changes to your project's files over time.
- ### The real power of Git lies in its ability to save each change (commit) you make to your project's files by keeping a history of changes, allowing you to revert to any previous version if needed.
- ### It enables multiple people to collaborate on a project.
- ### [Git Book](https://git-scm.com/book/en/v2)

## Commands
- Most Git commands starts with git keyword to tell the system that you are using Git.
- Firstly navigate to your project directory in the CLI.
- Now I am in a local project; where the Git is? To let Git start working on your project, you have to use the git init command to initialize or create a repository to include the project's files in Git, so let's start with the first command, which is git init.

## git init
- Create an empty Git repository or reinitialize an existing one.
- Hint: After creating the repository, Git will add a hidden .git folder to your project. This folder contains all the files Git needs to track your project’s history and changes.
- Now we have created a repository, we are in need to start adding and tracking project files. Let's move on to the second command, which is git add.

## git add file-name, <*> or <.>
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

## git branch
- List, create, or delete branches
- git branch
  - List all branches.
- git branch branch-name
  - create branch with the given name.
- git branch -M new-branch-name
  - Renames the current branch to new given name.
  - The -M flag forces the rename, even if there’s already a branch with that name.
- git branch -M new-branch-name

## git remote add remote-name url-of-remote-repo
- Adds a remote repository with the specified name and URL, allowing you to connect your local project to a remote repository

## git remote -v
- Displays the names and URLs of all remotes associated with the repository, showing whether each URL is used for fetching or pushing.

## git push -u origin main

## git pull origin main

## git config
- To set your username and email in Git
- Global Configuration (Applies to all repositories on your system) This is useful if you want to use the same username and email across all your Git repositories.
  - git config --global user.name "Your Name"
  - git config --global user.email "your_email@example.com"
- Repository-Specific Configuration (Applies only to the current repository) If you want to use a different username and email for a specific project, navigate to the project directory and run
  - git config user.name "Your Name"
  - git config user.email "your_email@example.com"
- Verifying Configuration To verify that the information was set correctly, you can use
  - git config --global user.name
  - git config --global user.email
- Or, to check the configuration in the current repository:
  - git config user.name
  - git config user.email

  
