# Git
- ### This repo is a beginner guide for learning mostly used Git commands.

# Commands
- ### Most Git commands starts with git keyword to tell the system that you are using Git.

- ## git init
  - Create an empty Git repository or reinitialize an existing one.
  - Now that we have created a repository, we are in need to start adding and tracking project files. Let's move on to the second command, which is git add.

- ## git add file-name, * or .
  - Add file contents to the index
  - Once you have created a Git repository, your project files will be untracked by the Git. To let Git start tracking project files, use the git add command to let it track files.
  - Using * or . instead of file-name will let all project files be tracked.
  - Then the project files either tracked or untracked so we are in need for command to check the status of project files. Lets move on to the next command, which is git status.

- ## git status
  - Show the working tree status this means showing the status of untracked files if it is modified or unmodified (at staging area to be commited).
  - Once I have done all the changes, I will need to save or make a checkpoint for changes that have already been made, so we will jamb to the next command, which is git commit.

- ## git commit -m "leave a message describes what you did in this commit"
  - commit in Git is recording the latest changes to the repository that have been done.

- ## git branch
  - List, create, or delete branches
  - git branch
    - List all branches.
  - git branch branch-name
    - create branch with the given name.
