# Advanced Git Commands

## Table of Contents
1. [Introduction](#introduction)
2. [Cherry-picking Commits](#cherry-picking-commits)
3. [Rebasing: When and How to Use It](#rebasing-when-and-how-to-use-it)
4. [Squashing Commits](#squashing-commits)
5. [Using Tags in Git](#using-tags-in-git)
6. [Conclusion](#conclusion)

---

## Introduction
Git is a powerful version control system that provides advanced features for managing commits, branches, and history. Understanding these advanced Git commands can help you maintain a clean repository, collaborate effectively, and streamline your development workflow. In this guide, we will explore cherry-picking commits, rebasing, squashing commits, and using tags in Git.

---

## Cherry-picking Commits
Cherry-picking allows you to apply a specific commit from one branch onto another. This is useful when you need to apply a bug fix from one branch to another without merging the entire branch.

### How to Cherry-pick a Commit:
1. Identify the commit hash using:
   ```sh
   git log --oneline
   ```
2. Switch to the target branch:
   ```sh
   git checkout target-branch
   ```
3. Apply the specific commit:
   ```sh
   git cherry-pick <commit-hash>
   ```
4. If conflicts arise, resolve them manually and continue:
   ```sh
   git cherry-pick --continue
   ```
5. If you need to abort the process:
   ```sh
   git cherry-pick --abort
   ```

---

## Rebasing: When and How to Use It
Rebasing is an alternative to merging that rewrites commit history. It is used to maintain a linear history by applying changes from one branch onto another.

### When to Use Rebasing:
- To clean up commit history before merging into the main branch.
- To update a feature branch with the latest changes from the main branch.

### How to Rebase:
1. Switch to the feature branch:
   ```sh
   git checkout feature-branch
   ```
2. Rebase onto the main branch:
   ```sh
   git rebase main
   ```
3. If conflicts occur, resolve them and continue:
   ```sh
   git rebase --continue
   ```
4. If necessary, abort the rebase:
   ```sh
   git rebase --abort
   ```

### Interactive Rebasing
Interactive rebasing allows you to modify commit history.
```sh
git rebase -i HEAD~3
```
This opens an editor where you can squash, edit, or reorder commits.

---

## Squashing Commits
Squashing commits is useful for cleaning up commit history by combining multiple commits into one.

### How to Squash Commits:
1. Start an interactive rebase for the last N commits:
   ```sh
   git rebase -i HEAD~N
   ```
2. In the editor, change `pick` to `squash` (or `s`) for commits you want to merge.
3. Save and close the editor.
4. Edit the commit message and save.

This results in a single commit containing all the changes.

---

## Using Tags in Git
Tags are used to mark specific points in your Git history, such as version releases.

### Creating a Tag:
```sh
git tag v1.0.0
```

### Listing Tags:
```sh
git tag
```

### Pushing a Tag to Remote Repository:
```sh
git push origin v1.0.0
```

### Deleting a Tag:
```sh
git tag -d v1.0.0
git push origin --delete v1.0.0
```

### Annotated Tags (with Metadata):
```sh
git tag -a v1.0.0 -m "Release version 1.0.0"
```

---

## Conclusion
Mastering advanced Git commands like cherry-picking, rebasing, squashing commits, and using tags can significantly improve your workflow and repository management. These techniques help maintain a clean, structured, and efficient project history, making collaboration and debugging much easier.
