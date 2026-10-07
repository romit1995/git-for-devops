# Git Commands Cheat Sheet

## 1. Directory Commands

### Create a directory

```bash
mkdir git_for_devops
```

### Navigate into a directory

```bash
cd git_for_devops/
```

---

## 2. File Commands

### Create an empty file

```bash
touch nibba.txt
```

### Edit a file

```bash
vim nibba.txt
```

### Display file contents

```bash
cat nibba.txt
```

---

## 3. Initialize a Git Repository

### Initialize Git

```bash
git init
```

Creates a new Git repository in the current directory.

### Check repository status

```bash
git status
```

Shows the current branch and the state of files in the working directory and staging area.

---

## 4. Git Staging

### Add a specific file

```bash
git add nibba.txt
```

Stages a specific file for the next commit.

### Add all changes

```bash
git add .
```

Stages all new, modified, and deleted files.

### Remove a file from staging

```bash
git rm --cached nibba.txt
```

Removes the file from the staging area without deleting the actual file.

---

## 5. Git Commit

### Create a commit

```bash
git commit -m "adding nibba nibbi"
```

Creates a commit using the changes currently in the staging area.

### Basic Git workflow

```text
Working Directory
       ↓
   git add
       ↓
Staging Area
       ↓
  git commit
       ↓
Git Repository
```

---

## 6. Git Configuration

### Set Git username

```bash
git config --global user.name "romit1995"
```

### Set Git email

```bash
git config --global user.email "rjn121210@gmail.com"
```

### View Git configuration

```bash
git config --list
```

---

## 7. Git Branches

### List branches

```bash
git branch
```

Shows all local branches.

Example:

```text
  dev
* master
```

The `*` indicates the branch you are currently on.

### Create a branch

```bash
git branch dev
```

Creates a new branch called `dev`.

### Create and switch to a branch

```bash
git checkout -b dev
```

Creates the `dev` branch and switches to it.

### Switch to an existing branch

```bash
git checkout master
```

Switches to the `master` branch.

### Switch branches using modern Git syntax

```bash
git switch dev
```

Switches to the `dev` branch.

---

## 8. Git Commit History

### View detailed history

```bash
git log
```

Displays detailed information about commits.

### View compact history

```bash
git log --oneline
```

Displays each commit in a single line.

### View history as a graph

```bash
git log --oneline --all --graph
```

Useful for visualizing branches and commits.

---

## 9. Working With Branches

Create and switch to a development branch:

```bash
git checkout -b dev
```

Create a file:

```bash
vim nibbu.txt
```

Stage the file:

```bash
git add .
```

Commit the changes:

```bash
git commit -m "nibbu added"
```

Switch back to `master`:

```bash
git checkout master
```

The commit containing `nibbu.txt` belongs to the `dev` branch.

Example:

```text
master
  │
  ● Initial commit
  │
  └──── dev
          │
          ● nibbu added
```

---

## 10. Complete Basic Git Workflow

```text
Create/Edit Files
       ↓
   git status
       ↓
    git add
       ↓
   git status
       ↓
   git commit
       ↓
   git log
```

Typical commands:

```bash
git status
git add .
git commit -m "Added new files"
git log --oneline
```

---

## 11. Quick Reference

| Topic                 | Command                                  | Purpose                  |
| --------------------- | ---------------------------------------- | ------------------------ |
| Initialize repository | `git init`                               | Create Git repository    |
| Check status          | `git status`                             | Check repository status  |
| Add file              | `git add file`                           | Stage a specific file    |
| Add all               | `git add .`                              | Stage all changes        |
| Unstage file          | `git rm --cached file`                   | Remove file from staging |
| Commit                | `git commit -m "message"`                | Create a commit          |
| List branches         | `git branch`                             | Show local branches      |
| Create branch         | `git branch dev`                         | Create a branch          |
| Create + switch       | `git checkout -b dev`                    | Create and switch branch |
| Switch branch         | `git checkout dev`                       | Switch branches          |
| Modern switch         | `git switch dev`                         | Switch branches          |
| View history          | `git log`                                | Detailed commit history  |
| Compact history       | `git log --oneline`                      | Short commit history     |
| Graph history         | `git log --oneline --all --graph`        | Visualize branch history |
| Set username          | `git config --global user.name "name"`   | Configure Git username   |
| Set email             | `git config --global user.email "email"` | Configure Git email      |

---

## 12. Important Git Concepts

```text
Working Directory
       │
       │ git add
       ▼
Staging Area
       │
       │ git commit
       ▼
Local Repository
       │
       │ git push
       ▼
Remote Repository
```

### Topics to Learn Next

* `git diff`
* `git reset`
* `git restore`
* `git merge`
* `git rebase`
* `git remote`
* `git push`
* `git pull`
* `git clone`
* Merge conflicts
* `.gitignore`
* GitHub/GitLab workflow
