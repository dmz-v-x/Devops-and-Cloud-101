# Undoing Changes in Git

## Table of Contents
- [Undoing Changes in Git](#undoing-changes-in-git)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Undoing Last Commit](#undoing-last-commit)
    - [Using `git reset`](#using-git-reset)
      - [Example:](#example)
    - [Using `git revert`](#using-git-revert)
      - [Example:](#example-1)
  - [Discarding Unstaged Changes](#discarding-unstaged-changes)
    - [Using `git checkout`](#using-git-checkout)
    - [Using `git restore`](#using-git-restore)
  - [Recovering Deleted Files](#recovering-deleted-files)
  - [Git Stash: Saving and Restoring Work in Progress](#git-stash-saving-and-restoring-work-in-progress)
    - [Saving Work](#saving-work)
    - [Restoring Work](#restoring-work)
    - [Listing Stashed Changes](#listing-stashed-changes)
  - [Real-World Use Case Scenario](#real-world-use-case-scenario)
  - [Summary](#summary)

---

## Introduction
Imagine you're writing an important school assignment on your computer, and suddenly, you realize you made a big mistake. Wouldn't it be great if you had a magic "undo" button to go back? Git provides such features to help developers correct mistakes efficiently without losing important work.

---

## Undoing Last Commit
There are two main ways to undo the last commit: `git reset` and `git revert`.

### Using `git reset`
`git reset` allows you to undo a commit and move the HEAD pointer back to an earlier state.

#### Example:
```sh
git reset --soft HEAD~1  # Undo the last commit but keep the changes staged
git reset --mixed HEAD~1 # Undo the last commit and unstage the changes
git reset --hard HEAD~1  # Undo the last commit and discard changes permanently
```

> **Warning:** `git reset --hard` is irreversible. Use with caution!

### Using `git revert`
Unlike `git reset`, `git revert` creates a new commit that undoes the changes from a previous commit.

#### Example:
```sh
git revert HEAD  # Create a new commit that undoes the last commit
```

Use `git revert` if you've already shared the commit with others.

---

## Discarding Unstaged Changes
If you've modified files but haven't staged them yet, you can discard those changes using:

### Using `git checkout`
```sh
git checkout -- filename  # Revert changes in a specific file
```

### Using `git restore`
```sh
git restore filename  # Revert changes in a specific file
```

> **Note:** In Git version 2.23 and later, `git restore` is recommended over `git checkout`.

---

## Recovering Deleted Files
If you've accidentally deleted a file and haven't committed the deletion, you can recover it:

```sh
git checkout -- filename  # Restore deleted file
```

If you've already committed the deletion, use:
```sh
git checkout HEAD^ -- filename
```

---

## Git Stash: Saving and Restoring Work in Progress
Sometimes, you need to switch tasks but don’t want to commit unfinished work. Use Git Stash:

### Saving Work
```sh
git stash  # Stash current changes
```

### Restoring Work
```sh
git stash pop  # Apply the last stash and remove it
git stash apply stash@{0}  # Apply a specific stash
```

### Listing Stashed Changes
```sh
git stash list  # View saved stashes
```

---

## Real-World Use Case Scenario
Imagine you’re working on a new feature, but your manager asks you to fix an urgent bug. Instead of committing half-done work, you stash your changes, switch to the bug-fix branch, complete the fix, and then restore your stashed work seamlessly.

---

## Summary
- `git reset` and `git revert` help undo commits in different ways.
- `git checkout` and `git restore` discard unstaged changes.
- Deleted files can be recovered using `git checkout`.
- `git stash` allows you to save and restore uncommitted work.
- Understanding these commands prevents accidental data loss and improves productivity.

Now you’re equipped to handle mistakes like a pro! 🚀
