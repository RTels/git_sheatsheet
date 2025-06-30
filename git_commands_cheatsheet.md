# Git Commands Cheat Sheet (Sorted by Frequency of Use)

> This Markdown file lists **Git commands** in approximate **order of real-world frequency of use**, starting with daily essentials and ending with niche/advanced commands.

---

## 🔁 Everyday Essentials

```bash
git status           # Show the working tree status
git add <file>       # Stage a file
git add .            # Stage all changes
git commit -m "msg"  # Commit staged changes with message
git push             # Push changes to remote repository
git pull             # Fetch and merge from origin
git clone <url>      # Clone a remote repo
```

---

## 🌿 Branching & Navigation

```bash
git branch                  # List local branches
git branch -r              # List remote branches
git branch -a              # List all branches
git branch <name>          # Create a new branch
git switch <name>          # Switch to branch (modern)
git checkout <name>        # Switch to branch (legacy)
git switch -c <name>       # Create and switch to new branch
git checkout -b <name>     # Same as above
```

---

## 🔀 Merging & Rebasing

```bash
git merge <branch>                 # Merge branch into current
git merge --no-ff <branch>         # Preserve merge history
git rebase <branch>                # Reapply commits on top of another base
git rebase -i HEAD~n               # Interactive rebase
```

---

## 🌎 Remote Repos

```bash
git remote -v                    # List remotes
git remote add origin <url>     # Add remote

# Push/Pull remote branches
git push origin <branch>        # Push specific branch
git push -u origin <branch>     # Push and set upstream
git fetch                       # Fetch updates
git pull origin <branch>        # Pull specific branch
```

---

## 👀 Viewing Changes

```bash
git diff                        # Unstaged changes
git diff --staged              # Staged changes
git diff <branch1> <branch2>   # Compare branches
git log                        # View commit history
git log --oneline --graph      # Concise graph view
```

---

## 🧹 Undo & Clean

```bash
git restore <file>             # Undo changes to file
git restore --staged <file>    # Unstage file
git reset <file>               # Unstage file (old syntax)
git reset --hard               # Discard all changes (DANGER!)
git clean -fd                  # Delete untracked files/dirs (DANGER!)
```

---

## 🗑️ Deleting Branches

```bash
git branch -d <name>           # Delete local branch (safe)
git branch -D <name>           # Force delete local branch
git push origin --delete <name> # Delete remote branch
```

---

## 🔍 Searching & Blame

```bash
git grep "text"                # Search in repo

git blame <file>               # Show who changed what line
```

---

## 🧪 Tags & Releases

```bash
git tag                        # List tags
git tag <name>                 # Create tag
git tag -a <name> -m "msg"     # Annotated tag
git push origin <tagname>      # Push tag
```

---

## 🔄 Stashing

```bash
git stash                      # Save current work

git stash apply                # Reapply latest stash
git stash pop                  # Apply and delete stash
```

---

## 🧠 Advanced & Plumbing

```bash
git reflog                     # View all HEAD changes
git cherry-pick <commit>       # Apply specific commit

git bisect start               # Start binary search for bug
git submodule update --init    # Init/update submodules

git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

## 🧪 Low-Level / Rare

```bash
git archive                    # Create archive from repo
git gc                         # Garbage collection
git fsck                       # Check repo integrity
git filter-branch              # Rewrite history (legacy)
git worktree add <dir> <branch> # Create linked working tree
```

---

## 📌 Notes

- `switch` and `restore` are modern replacements for older `checkout`/`reset` patterns.
- `rebase` can rewrite history—use with care on shared branches.
- `reset --hard` and `clean` are destructive—double check before running.

---

✅ **Pro Tip:** Always `git status` before and after making changes!

---

