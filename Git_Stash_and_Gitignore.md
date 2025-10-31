## 1. Git Stash — Temporary Save for Your Work

- Concept

- The git stash command stores your uncommitted changes (both staged and unstaged) into a temporary area called the stash stack.

- It reverts your working directory to the last committed state, allowing you to safely switch branches or perform clean operations.

- You can later reapply (pop) those stashed changes when you’re ready.

- Think of it as: “Put my messy desk in a drawer for now, I’ll get back to it later.”

## Common git stash Commands

## Save Current Work

```
git stash
```

- Temporarily saves your uncommitted changes and clears your working directory.

🔹 Save with a Custom Message

- git stash push -m "WIP: working on navbar feature"

- Stores changes with a description so you remember what it’s for.

🔹 List All Stashes

```
git stash list
```

- Shows all saved stashes.

🔹 Apply the Most Recent Stash

```
git stash apply
```

- Restores the last stashed changes but keeps the stash in the stack.

🔹 Apply and Remove (Pop)

```
git stash pop
```

- Applies the last stash and removes it from the stash list.

🔹 Apply a Specific Stash

```
git stash apply stash@{2}
```

- Applies a specific stash entry from the list.

🔹 Drop/Delete a Stash

```
git stash drop stash@{1}
```

- Deletes a specific stash.

🔹 Clear All Stashes

```
git stash clear
```

- Removes all stashed entries from the list.

## 2. .gitignore — Ignoring Unwanted Files

- Concept

- .gitignore tells Git to ignore specific files or directories.
- This prevents unnecessary files (like logs, build artifacts, or credentials) from being committed to your repository.
- Typical examples include:
- Compiled files (_.class, _.pyc)
- Log files (\*.log)
- Environment configuration (.env)
- System files (.DS_Store, Thumbs.db)
- Node modules or dependencies (node_modules/)

## How to Use .gitignore

🔹 Create a .gitignore File

```
touch .gitignore
```

🔹 Add Patterns to Ignore

- Example .gitignore content:

## Ignore log files

- \*.log

## Ignore environment files

- .env

## Ignore node modules

- node_modules/

## Ignore system files

- .DS_Store
- Thumbs.db

🔹 Verify Ignored Files

```
git status
```

- You’ll notice the ignored files no longer appear in the untracked list.

- Note: .gitignore only affects files that are not yet tracked by Git.
- If a file is already tracked, you must untrack it using:

```
git rm --cached <file>
```
