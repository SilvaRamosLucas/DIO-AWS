# 📘 Git Commands Sheet

## Introduction

Git is a powerful and essential tool for version control, widely used in software development. It allows developers to collaborate efficiently and track changes in the source code over time. Below, you'll find the most important Git commands, accompanied by examples to illustrate their use.

---

<details>

<summary> Topics </summary>

## 📌 Table of Contents

1. [Initializing a Repository](#1-initializing-a-repository)
2. [Cloning a Repository](#2-cloning-a-repository)
3. [Adding Changes](#3-adding-changes)
4. [Committing Changes](#4-committing-changes)
5. [Checking Status](#5-checking-status)
6. [Pushing Changes](#6-pushing-changes)
7. [Pulling Changes](#7-pulling-changes)
8. [Managing Branches](#8-managing-branches)
9. [Switching Branches](#9-switching-branches)
10. [Merging Branches](#10-merging-branches)
11. [Viewing Commit History](#11-viewing-commit-history)
12. [Managing Remote Repositories](#12-managing-remote-repositories)
13. [Stashing Changes](#13-stashing-changes)
14. [Rebasing Branches](#14-rebasing-branches)
15. [Resetting Changes](#15-resetting-changes)
16. [Showing Differences](#16-showing-differences)
17. [Tagging Commits](#17-tagging-commits)
18. [Cherry-Picking Commits](#18-cherry-picking-commits)
19. [Fetching Changes](#19-fetching-changes)
20. [Archiving a Repository](#20-archiving-a-repository)
21. [Managing Submodules](#21-managing-submodules)
22. [Configuring Git](#22-configuring-git)

</details>

---

## ⚙ Commands

### 1. Initializing a Repository

The `git init` command initializes a new Git repository in a directory.

```sh
$ mkdir my_project
$ cd my_project
$ git init
```
### 2. Cloning a Repository

The `git clone` command is used to create a copy of an existing repository.

```sh
$ git clone https://github.com/user/repo.git
```

### 3. Adding Changes

The `git add` command adds changes in the working directory to the staging area.

```sh
#To add all modified files
$ git add file.txt
$ git add .
```

### 4. Committing Changes

The `git commit` command records the changes added to the staging area in a new commit.

```sh
$ git commit -m "Message describing the changes"
```

### 5. Checking Status

The `git status` command shows the current state of the working directory and the staging area.

```sh
$ git status
```

### 6. Pushing Changes

The `git push` command sends commits from the local repository to a remote repository.

```sh
$ git push origin master
```

### 7. Pulling Changes

The `git pull` command fetches and integrates changes from a remote repository.

```sh
$ git pull origin master
```

### 8. Managing Branches

The `git branch` command allows you to manage branches.

```sh
# List branches
$ git branch

# Create a new branch
$ git branch new-feature

# Delete a branch
$ git branch -d old-branch
```

### 9. Switching Branches

The `git checkout` command is used to switch branches or restore files.

```sh
# Switch to another branch
$ git checkout new-feature

# Create a new branch and switch to it
$ git checkout -b new-feature
```

### 10. Merging Branches

The `git merge` command combines changes from different branches.

```sh
$ git checkout master
$ git merge new-feature
```

### 11. Viewing Commit History

The `git log` command displays the commit history of the repository.

```sh
$ git log

# Show history with diff stats
$ git log --stat
```

### 12. Managing Remote Repositories

The `git remote` command allows you to manage connections to remote repositories.

```sh
# List remote repositories
$ git remote -v

# Add a remote repository
$ git remote add origin https://github.com/user/repo.git

# Remove a remote repository
$ git remote remove origin
```

### 13. Stashing Changes

The `git stash` command temporarily saves uncommitted changes.

```sh
# Save uncommitted changes
$ git stash

# List saved stashes
$ git stash list

# Apply the most recent stash
$ git stash apply

# Apply and remove the most recent stash
$ git stash pop
```

### 14. Rebasing Branches

The `git rebase` command reapplies commits from one branch on top of another.

```sh
$ git checkout my-branch
$ git rebase master
```

### 15. Resetting Changes

The `git reset` command moves the current branch pointer and modifies the staging area and/or working directory.

```sh
# Revert commits but keep changes in the working directory
$ git reset --soft HEAD~1

# Revert commits and changes in the staging area, but keep in the working directory
$ git reset --mixed HEAD~1

# Revert commits and all changes
$ git reset --hard HEAD~1
```

### 16. Showing Differences

The `git diff` command shows the differences between commits, branches, and the working directory.

```sh
# Show differences between the working directory and the staging area
$ git diff

# Show differences between the staging area and the last commit
$ git diff --cached

# Show differences between two branches
$ git diff branch1 branch2
```

### 17. Tagging Commits

The `git tag` command marks specific points in the repository's history.

```sh
# Create an annotated tag
$ git tag -a v1.0 -m "Version 1.0"

# Create a lightweight tag
$ git tag v1.1

# List all tags
$ git tag

# Push tags to the remote repository
$ git push origin --tags
```

### 18. Cherry-Picking Commits
The `git cherry-pick` command applies a specific commit from one branch to another.

```sh
$ git checkout master
$ git cherry-pick abc123
```

### 19. Fetching Changes

The `git fetch` command fetches changes from a remote repository without automatically integrating them.

```sh
$ git fetch origin
```

### 20. Archiving a Repository

The `git archive` command creates a tar or zip file of a repository tree.

```sh
# Create a tar file of the master branch
$ git archive --format=tar master | gzip > project.tar.gz
```

### 21. Managing Submodules

The `git submodule` command manages submodules, which are Git repositories inside another Git repository.

```sh
# Add a submodule
$ git submodule add https://github.com/user/subrepo.git path/to/subrepo

# Initialize submodules
$ git submodule init

# Update submodules
$ git submodule update
```

### 22. Configuring Git

The `git config` command configures Git options and behaviors.

```sh
# Configure username
$ git config --global user.name "Your Name"

# Configure email
$ git config --global user.email "youremail@example.com"

# View all configurations
$ git config --list
```

## ☑ Conclusion

#### These commands form the basis of daily Git use, allowing developers to control the version of their code, collaborate efficiently, and maintain a clear and detailed history of changes in the project. Mastering these commands is essential for any developer working in a team or on long-term projects. Happy coding! 🚀

## 📚 Documentation

- [Git](https://git-scm.com/doc)
- [GitHub](https://docs.github.com/en)
- [Markdown](https://www.markdownguide.org/)
