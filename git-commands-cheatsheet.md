# 🧠 Git Command Cheat Sheet

## 🔧 Setup & Config
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
````

## 📁 Initialize & Clone

```bash
git init                    # Initialize a new repo
git clone <repo-url>        # Clone a repository
```

## 📌 Basic Workflow

```bash
git status                  # Check status
git add <file>              # Stage a file
git add .                   # Stage all changes
git commit -m "message"     # Commit staged changes
git log                     # View commit history
```

## 🌿 Branching

```bash
git branch                  # List branches
git branch <branch-name>    # Create new branch
git checkout <branch>       # Switch branch
git checkout -b <branch>    # Create & switch branch
git merge <branch>          # Merge branch into current
git branch -d <branch>      # Delete branch
```

## 🔄 Remote Repos

```bash
git remote -v                       # Show remotes
git remote add origin <url>        # Add remote
git push -u origin main            # Push to remote (first time)
git push                           # Push changes
git pull                           # Fetch & merge changes
git fetch                          # Fetch without merging
```

## 🔀 Undo Changes

```bash
git restore <file>         # Discard changes in working dir
git reset <file>           # Unstage file
git reset --hard           # Reset everything (⚠️ destructive)
git revert <commit>        # Undo commit safely
```

## 🕵️‍♂️ Inspecting

```bash
git diff                   # Show changes
git diff --staged          # Show staged changes
git show <commit>          # Show commit details
```

## 📦 Stashing

```bash
git stash                  # Save changes temporarily
git stash pop              # Apply and remove stash
git stash list             # List stashes
```

## 🏷️ Tags

```bash
git tag                    # List tags
git tag <tag-name>         # Create tag
git push origin <tag>      # Push tag
```

## ⚡ Useful Shortcuts

```bash
git commit -am "message"   # Add & commit tracked files
git checkout -- <file>     # Discard file changes (old syntax)
```

---

