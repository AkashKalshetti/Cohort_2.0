# Cohort_2.0

# Git & GitHub Cheat Sheet
## 🔧 Configuration
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list

## 📁 Repository Setup
git init                    # Initialize a new repo
git clone <repo-url>        # Clone an existing repo

## 📄 Checking Status & History
git status                  # Check working tree status
git log                     # Commit history
git log --oneline --graph   # Compact visual history

## ➕ Staging & Committing
git add <file>              # Stage a file
git add .                   # Stage all changes
git commit -m "message"     # Commit staged changes
git commit -am "message"    # Add & commit tracked files

## 🌿 Branching
git branch                  # List branches
git branch <name>           # Create new branch
git checkout <name>         # Switch branch
git checkout -b <name>      # Create & switch branch
git branch -d <name>        # Delete branch

## 🔀 Merging & Rebasing
git merge <branch>          # Merge branch into current
git rebase <branch>         # Rebase current branch

## 🌍 Remote (GitHub)
git remote -v               # View remotes
git remote add origin <url> # Add remote repo
git push origin <branch>    # Push to remote
git pull origin <branch>    # Pull from remote

## 🔄 Syncing Changes
git fetch                   # Fetch without merging
git pull                    # Fetch + merge
git push                    # Push local commits

## ♻️ Undo & Fix
git restore <file>          # Discard file changes
git restore --staged <file> # Unstage file
git reset --soft HEAD~1     # Undo last commit (keep changes)
git reset --hard HEAD~1     # Undo last commit (discard changes)

## 🧹 Clean Up
git clean -n                # Preview files to delete
git clean -f                # Delete untracked files

## 🏷️ Tags
git tag                     # List tags
git tag <tag-name>          # Create tag
git push origin <tag-name>  # Push tag

## 🚀 Common Workflow
git checkout -b feature-x
git add .
git commit -m "Add feature X"
git push origin feature-x

## 🧠 Helpful Tips
* Commit often with **clear messages**
* Pull before pushing to avoid conflicts
* Use branches for features & fixes
* Never commit secrets 🔒