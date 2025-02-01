# Working with Branches in Git

## Table of Contents
- [Working with Branches in Git](#working-with-branches-in-git)
  - [Table of Contents](#table-of-contents)
  - [What are Branches in Git?](#what-are-branches-in-git)
  - [Creating and Switching Branches](#creating-and-switching-branches)
    - [Creating a New Branch](#creating-a-new-branch)
    - [Switching Branches](#switching-branches)
  - [Merging Branches](#merging-branches)
    - [Understanding Merging](#understanding-merging)
    - [Performing a Merge](#performing-a-merge)
    - [Fast-Forward vs. Three-Way Merge](#fast-forward-vs-three-way-merge)
  - [Deleting Branches](#deleting-branches)
    - [Deleting a Local Branch](#deleting-a-local-branch)
    - [Deleting a Remote Branch](#deleting-a-remote-branch)
  - [Resolving Merge Conflicts](#resolving-merge-conflicts)
    - [Why Do Conflicts Happen?](#why-do-conflicts-happen)
    - [Identifying Conflicts](#identifying-conflicts)
    - [Resolving Conflicts](#resolving-conflicts)
    - [Using a Merge Tool](#using-a-merge-tool)
  - [Summary](#summary)


## What are Branches in Git?
A branch in Git represents an independent line of development. It allows multiple developers to work on different features or bug fixes simultaneously without interfering with each other’s code.

Key benefits of using branches:
- Enables parallel development.
- Keeps the main codebase stable.
- Facilitates experimentation without affecting production.
- Supports collaborative workflows.

By default, Git initializes a repository with a branch called `main` (previously `master`).

---

## Creating and Switching Branches

### Creating a New Branch
To create a new branch, use:

```sh
git branch feature-branch
```

This creates a branch named `feature-branch` but does not switch to it.

### Switching Branches
To switch (checkout) to the new branch:

```sh
git checkout feature-branch
```

Alternatively, create and switch in one command:

```sh
git checkout -b feature-branch
```

To list all branches:

```sh
git branch
```

The current active branch is marked with an asterisk (`*`).

---

## Merging Branches

### Understanding Merging
Merging integrates changes from one branch into another, typically into `main` or `develop`.

### Performing a Merge
First, switch to the branch you want to merge into:

```sh
git checkout main
```

Merge the `feature-branch` into `main`:

```sh
git merge feature-branch
```

Git will attempt to merge automatically. If there are conflicts, they must be resolved manually.

### Fast-Forward vs. Three-Way Merge
- **Fast-Forward Merge**: Happens when there are no new commits on the target branch.
- **Three-Way Merge**: Occurs when both branches have diverged, requiring Git to create a new merge commit.

To force a merge commit (even when fast-forward is possible):

```sh
git merge --no-ff feature-branch
```

---

## Deleting Branches

### Deleting a Local Branch
After merging, delete a branch locally with:

```sh
git branch -d feature-branch
```

If the branch is not merged and you want to force deletion:

```sh
git branch -D feature-branch
```

### Deleting a Remote Branch
Push a delete request to the remote repository:

```sh
git push origin --delete feature-branch
```

To ensure remote-tracking branches are updated:

```sh
git fetch --prune
```

---

## Resolving Merge Conflicts

### Why Do Conflicts Happen?
Conflicts occur when two branches modify the same line in a file differently.

### Identifying Conflicts
Git marks conflicts in files like this:

```diff
<<<<<<< HEAD
This is the main branch's version.
=======
This is the feature branch's version.
>>>>>>> feature-branch
```

### Resolving Conflicts
Manually edit the file to keep the desired changes, then mark it as resolved:

```sh
git add conflicted-file.txt
git commit -m "Resolved merge conflict in conflicted-file.txt"
```

### Using a Merge Tool
To use Git’s built-in merge tool:

```sh
git mergetool
```

Abort a merge if needed:

```sh
git merge --abort
```

---

## Summary
- Git branches enable isolated development.
- Creating (`git branch`), switching (`git checkout`), and merging (`git merge`) are essential operations.
- Merging can be fast-forward or three-way, and sometimes conflicts need resolution.
- Deleting branches (`git branch -d` or `git push origin --delete`) helps keep repositories clean.

By mastering branches, you can collaborate efficiently and manage project versions effectively! 🚀
