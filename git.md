# Git Commands Reference Guide

## Basic Git Commands

### Repository Initialization and Cloning
- **`git init`**: Creates a new local repository in the current directory
- **`git clone`**: Copies an existing remote repository to your local machine

### Branch Creation and Navigation
- **`git branch`**: List local branches
- **`git checkout mi-rama`**: Switches your working directory to a different branch or commit, discarding any uncommitted changes
- **`git checkout -b firstname-lastname/rb`**: Creates and switches to a new branch

#### Remote Repository Management
- **`git checkout main`**: First move to the local main branch!
- **`git fetch origin`**: Only retrieves information from the remote repository
- **`git pull origin main`**: Performs fetch + merge (may cause errors) remote to main
Other commands:
- **`git remote -v`**: Shows the remote repositories configured for your local repository

### Working with your Brach and Main Local Branch
- **`git switch mi-rama`**: First move to the your branch!
Discard your work
- **`git reset --hard main`**: Leave your branch as main local one
Merge your work
Option 1
- **`git merge main`**: does a merge commit 
Option 2
- **`git stash push -m "WWIP" --include-untracked`**: 
- **`git rebase main`**: alignment mi-rama to main
- **`git stash pop`**: take back your changes

### Working with your Changes and your BNranch
- **`git checkout mi-rama`**: First move to the your branch!
- **`git status`**: Shows the state of your working directory and staging area
- **`git add`**: Adds changes in your working directory to the staging area, which is a temporary area where you can prepare your next commit
- **`git commit -m "message"`**: Records the changes in the staging area as a new snapshot in the local repository, along with a message describing the changes
- **`git commit --allow-empty -m "Ready to sync"`**: Creates an empty commit with a message

### Branching and Navigation
- **`git checkout`**: Switches your working directory to a different branch or commit, discarding any uncommitted changes
- **`git checkout -b firstname-lastname/rb`**: Creates and switches to a new branch
- **`git branch`**: Lists, creates, or deletes branches
- **`git merge`**: Combines the changes from one branch into another branch, creating a new commit if there are no conflicts

### Viewing Information
- **`git diff`**: Shows the differences between two commits, branches, files, or the working directory and the staging area
- **`git log`**: Shows the history of commits in the current branch, along with their messages, authors, and dates
- **`git log -1 --oneline`**: Shows the last commit in a single line format
- **`git log --oneline --all`**: Shows all commits in a condensed format

### Remote Repository Management
- **`git push -u origin main`**: Pushes the main branch to the origin remote and sets up tracking

## Advanced Operations

### Undoing Local Commits
```bash
git reset --soft HEAD~2
```
This command undoes the last 2 commits while keeping the changes in the staging area.

## Manual Git Fork Process

Follow these steps to manually fork a repository:

### 1. Create a New Empty Repository on GitHub
- Create a new repository on GitHub
- **Important**: Do not check options like including a README, .gitignore, or license

### 2. Clone the Original Repository Locally
Clone the original repository to your local machine.

### 3. Configure Upstream in the Local Repository
Instead of using origin, configure upstream:

**Rename the origin remote (which points to the original repository) as upstream:**
```bash
git remote rename origin upstream
```

**Verify the change was made correctly:**
```bash
git remote -v
```

### 4. Add Another Remote Repository (origin) to the Local Repository
```bash
git remote add origin https://github.com/<your-username>/t5-numpy-mnist-firstname-lastname.git
```

**Verify the remotes again:**
```bash
git remote -v
```

### 5. Upload Content to the New Repository (origin)
```bash
git push -u origin master
```
This command establishes the master branch as the default branch for future pushes.

### 6. Future: Pull Changes from the Original Repository (upstream)
```bash
git pull upstream master
```

## Quick Reference Summary

| Command | Purpose |
|---------|---------|
| `git init` | Initialize new repository |
| `git clone` | Copy remote repository |
| `git status` | Check working directory status |
| `git add` | Stage changes |
| `git commit` | Save staged changes |
| `git push` | Upload changes to remote |
| `git pull` | Download and merge changes |
| `git fetch` | Download changes only |
| `git branch` | Manage branches |
| `git checkout` | Switch branches/commits |
| `git merge` | Combine branches |
| `git log` | View commit history |
| `git diff` | Show differences |
