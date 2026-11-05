Here is your revised file content, renamed to **`GIT_COMMANDS.md`**, with the most frequently used commands moved straight to the top and organized with clear sub-headings.

You can copy and paste this text directly into your repository file:

# 🛠️ Git Commands Cheat Sheet

A comprehensive reference guide for essential Git commands, prioritized by everyday usage.

---

## ⚡ 1. Daily & Frequently Used Commands

These are the core commands you will use 90% of the time during daily development.

### Working with Changes (Staging & Committing)

```bash
# Check status of modified, untracked, or staged files
git status

# Stage all modified and new files for commit
git add .

# Stage a specific file only
git add filename.txt

# Commit staged changes with a descriptive message
git commit -m "Add feature description"

# View unstaged changes in your working directory
git diff

```

### Syncing with GitHub (Push & Pull)

```bash
# Upload your local commits to the remote GitHub repository
git push origin main

# Download and merge the latest remote changes into your active branch
git pull origin main

# Push a new local branch to GitHub and set tracking upstream
git push -u origin feature-branch

```

---

## 🌿 2. Branching & Merging

Isolate feature development, manage parallel work, and combine changes.

### Managing Branches

```bash
# List all local branches (active branch marked with *)
git branch

# Create a new branch
git branch feature/login-page

# Switch to an existing branch
git switch feature/login-page
# (Alternative syntax: git checkout feature/login-page)

# Create and switch to a new branch immediately
git switch -c feature/login-page
# (Alternative syntax: git checkout -b feature/login-page)

```

### Combining & Cleaning Up

```bash
# Merge another branch into your current active branch
git merge feature/login-page

# Safely delete a branch after merging
git branch -d feature/login-page

# Force delete an unmerged branch (DESTRUCTIVE)
git branch -D feature/login-page

```

---

## 🚀 3. Repository Setup & Remote Connections

Commands for starting a project or linking to GitHub.

```bash
# Clone an existing remote repository to your local machine
git clone https://github.com/username/repository-name.git

# Initialize a brand-new Git repository in the current folder
git init

# View connected remote repository URLs
git remote -v

# Link your local repository to a GitHub remote server
git remote add origin https://github.com/username/repository-name.git

# Fetch updates from remote without merging them into working files
git fetch origin

```

---

## ⏪ 4. Undoing Changes & Fixing Mistakes

Commands to unstage files, edit recent commits, or roll back history safely.

```bash
# Discard uncommitted changes in a specific file
git restore filename.txt

# Unstage a file while keeping your local changes intact
git restore --staged filename.txt

# Amend the last commit (fix typo in message or include forgotten files)
git commit --amend -m "Updated commit message"

# Create a new commit that safely reverses a previous commit's changes
git revert <commit-hash>

# Reset working directory and staging area to match a past commit (DESTRUCTIVE)
git reset --hard <commit-hash>

```

---

## 🔍 5. Inspection, History & Configuration

Review repository history, inspect author tracking, or configure user settings.

### Commit Log & Line History

```bash
# View detailed commit history log
git log

# Display compact history with a visual graph representation
git log --oneline --graph --all

# View line-by-line modification history and authorship for a file
git blame filename.txt

```

### Git Configuration

```bash
# Set your global author name for commits
git config --global user.name "Your Name"

# Set your global email address for commits
git config --global user.email "email@example.com"

# View all active Git settings
git config --list

```
