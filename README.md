# react-course
# project 1
# created a first-react-app with CRA mehtod
# command : $npx create create-react-app [project-name]
# execute : $npm start
## project 2
# created a vite-react with vite build tool
# command : $npm install vite@latest [project-name]
# command : $cd [project-name]
# command : $npm install
# execute : $npm run dev

# git commands
# I already have set of react projects want to push to github into a single repository
# step 1 : created a empty reposiory in github and copy cloning link for remote connection
# step 2 : go to cmd of parent directory since it is already exist so initialise it
# $git init
# step 3 : add all projects to staging area with git add .
# $git git add .
# issue : error: 'first-react-project/' does not have a commit checked out
# fatal: adding files failed
# problem : The error message error: 'first-react-project/' does not have a commit checked out typically occurs when you are trying to add a subdirectory that is already a Git repository to another repository. Git does not allow nested repositories by default because it can cause conflicts and ambiguity.
# how to resolve
# Option 1: Remove Git History from Nested Repositories
#  1. Navigate to Each React Project Folder For example:
#  cd /path/to/react-projects/first-react-project
#  Remove the .git Folder Remove the Git history from the nested repository:
#  2. rm -rf .git
#  Repeat for All Subfolders Repeat this process for all React projects (e.g., first-react-project, second-react-project, etc.).

#  Add and Commit Files to the Parent Repository Navigate back to the parent directory (react-projects) and run:
#   git add .
#   git commit -m "Add all React projects"
#   git push -u origin main
# Option 2: Use Git Submodules (If You Want to Keep Individual Repos)
# If you want to preserve the separate Git histories for each React project, you can use Git submodules.

# Add Each React Project as a Submodule From the parent directory (react-projects), add each project as a submodule:
# $ git submodule add <URL_of_first_project_repo> first-react-project
# $ git submodule add <URL_of_second_project_repo> second-react-project

# The rm command is commonly used in Unix-based systems (e.g., Linux or macOS). If you're on Windows and the command rm is not recognized, you can use the following alternatives:

# Use PowerShell
# Open PowerShell.
# Navigate to your project directory:
# powershell
#  $ cd "C:\path\to\react-projects\first-react-project"
# Remove the .git folder: $ Remove-Item -Recurse -Force .git


# git branch commands -
# List branches
#   1. git branch - List all local branches
#   2. git branch -a : List all local and remote branches
# Create a new branch:
  # git branch <branch_name>
  # Switch to the new branch immediately after creating it: create and switch if we use -b flag
  # git checkout -b <branch_name>
  # git checkout <branch_name> switch if already branch exist
  # (Modern Git versions prefer git switch):
  # git switch -c <branch_name>
# 3. Switch Between Branches
  # Switch to another branch:
  # git checkout <branch_name>
  # (Preferred alternative):
  # git switch <branch_name>
# 4. Rename a Branch
  # Rename the current branch:
  # git branch -m <new_branch_name>
  # Rename a specific branch:
  # git branch -m <old_branch_name> <new_branch_name>
# 5. Delete a Branch
  # Delete a local branch:
  # git branch -d <branch_name>
  # (Use -D to force delete if the branch is not fully merged):
  # git branch -D <branch_name>
6. Push a Branch to a Remote Repository
Push a new branch to a remote repository:
git push -u origin <branch_name>
The -u option sets the remote branch as the default upstream for the local branch.
7. Delete a Remote Branch
Delete a branch on the remote repository:

git push origin --delete <branch_name>
8. Merge a Branch
Merge another branch into the current branch:
git merge <branch_name>
9. Track a Remote Branch Locally
Create a local branch that tracks a remote branch:
git checkout -b <branch_name> origin/<branch_name>
(Preferred alternative):
git switch -t origin/<branch_name>
10. View the Current Branch
Show the branch you’re currently on:

git branch --show-current
11. Compare Branches
Compare the current branch with another branch:

git diff <branch_name>

12. View a Branch’s Commit History
Show commit history for a specific branch:
git log <branch_name>
Common Workflows:
Create and switch to a branch:
git checkout -b feature-branch
Merge feature-branch into main:

git checkout main
git merge feature-branch
Push feature-branch to remote:
git push -u origin feature-branch