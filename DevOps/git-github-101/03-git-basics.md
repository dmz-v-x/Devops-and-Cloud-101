# Git Basics

## 1. Introduction to Git
Git is a distributed version control system that allows multiple people to collaborate on a project efficiently. It helps track changes, revert to previous versions, and work on different features simultaneously.

---

## 2. Git Terminology
Before diving into commands, let's understand some basic Git terminology:

- **Repository (Repo)**: A directory that contains all files, history, and metadata of a project tracked by Git.
- **Commit**: A snapshot of changes in a repository.
- **Branch**: A parallel version of the repository where changes can be made without affecting the main codebase.
- **Merge**: The process of integrating changes from one branch into another.
- **Clone**: Creating a copy of a remote repository on a local machine.
- **Staging Area**: A temporary storage for files before committing them.
- **Working Directory**: The local folder containing project files where changes are made.
- **Remote Repository**: A repository hosted on platforms like GitHub or GitLab, allowing collaboration.
- **Pull Request (PR)**: A request to merge changes from one branch to another in a remote repository.

---

## 3. Creating a New Git Repository
To create a new Git repository, follow these steps:

### Step 1: Initialize Git
Run the following command inside the project folder:

```sh
mkdir my_project
cd my_project
git init
```

This initializes a new Git repository in the `my_project` folder.

### Step 2: Add Files to the Repository
Create a sample file:

```sh
echo "# My Project" > README.md
```

Then, add the file to the staging area:

```sh
git add README.md
```

### Step 3: Commit the File
Commit the changes with a message:

```sh
git commit -m "Initial commit"
```

---

## 4. Cloning an Existing Repository
To work on an existing project hosted on a remote platform like GitHub:

### Step 1: Clone the Repository

```sh
git clone https://github.com/user/repository.git
```

This downloads the repository into a local folder named `repository`.

### Step 2: Navigate into the Cloned Repo

```sh
cd repository
```

Now you can start working on the project!

---

## 5. Staging and Committing Changes
### Staging Changes
After modifying files, use:

```sh
git add filename.txt  # Stage a specific file
git add .             # Stage all changes
```

### Committing Changes
Once staged, commit the changes:

```sh
git commit -m "Updated filename.txt with new content"
```

To commit without opening an editor, use `-m` to specify a message.

---

## 6. Understanding the `.git` Directory
When you initialize a repository with `git init`, Git creates a hidden `.git` directory that contains:

- **HEAD**: Points to the current branch.
- **config**: Configuration settings for the repository.
- **objects/**: Stores all commits, trees, and other Git objects.
- **refs/**: Contains references to commits (branches, tags, etc.).
- **index**: Tracks the staging area.

To view `.git` contents, run:

```sh
ls -la .git
```

⚠️ **Do not modify `.git` manually unless necessary, as it stores the full repository history!**

---

## 7. Summary
- Git helps track changes and collaborate efficiently.
- A repository is a Git-tracked project folder.
- `git init` creates a new repository.
- `git clone` copies an existing repository.
- `git add` stages changes, and `git commit` saves them.
- `.git` directory contains all the necessary metadata for version control.

This guide provides a fundamental understanding of Git basics. Stay tuned for more Git topics! 🚀
