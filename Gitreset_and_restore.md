## 1. git reset — Moving the Commit Pointer

- git reset is used to move the current branch’s HEAD to a previous commit.
- It changes the state of your repository in terms of:

## Commits

- Staging area

- Working directory

- Depending on the mode you use (soft, mixed, or hard), it controls how much gets changed.

## 🔹 a) Soft Reset

- The commit pointer (HEAD) moves back to a chosen commit.

- The staging area and working directory remain unchanged.

- It’s like undoing a commit while keeping your changes staged — ready to recommit again if needed.
-
- Commonly used when you realize you forgot to add something to the last commit and want to re-commit properly.

- Think of it as: “Undo the commit, but keep my changes intact.”

## 🔹 b) Mixed Reset (Default)

- The commit pointer moves back.

- The staging area is cleared, but your working directory remains unchanged.

- Files that were part of the undone commit now appear as unstaged changes.

- This is helpful when you want to re-stage specific files differently.

- Think of it as: “Undo the commit and unstage my files, but don’t touch what’s inside them.”

## 🔹 c) Hard Reset

- The commit pointer moves back.

- Both the staging area and working directory are reset to match the target commit.

- All uncommitted work is permanently deleted from your local environment.

- Used when you want to completely discard unwanted changes and restore your project to an earlier snapshot.

- Think of it as: “Completely go back in time — erase all uncommitted work.”

## 2. git restore — Reverting File Changes

- git restore is designed for restoring individual files either from:

  - the staging area, or
  - a specific commit.

- It’s much safer than reset, as it focuses only on file-level changes instead of rewriting history.

- You use it when:

  - You made accidental edits to a file and want to return to its last committed version.

  - You staged a file but changed your mind and want to unstage it.

  - Think of it as: “Undo changes in my files, not in my commit history.”
