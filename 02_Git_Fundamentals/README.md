# Git Fundamentals

Git Fundamentals covers the core concepts required to start using Git effectively. It explains the difference between Git and GitHub, how Git manages projects locally, and how repositories are created and maintained.

---

# Git vs GitHub

## Git

Git is a Distributed Version Control System (DVCS) installed on a developer's computer.

Git is responsible for:

- Tracking file changes
- Creating commits
- Managing project history
- Creating and managing branches
- Restoring previous versions
- Working completely offline

Git is the software that performs Version Control.

---

## GitHub

GitHub is a cloud platform that hosts Git repositories.

It allows developers to:

- Store repositories online
- Backup projects
- Collaborate with other developers
- Review code
- Manage Pull Requests
- Track Issues
- Build a professional portfolio

GitHub requires an internet connection for synchronization.

---

## Git vs GitHub

| Git | GitHub |
|------|---------|
| Software | Cloud Platform |
| Installed on local computer | Hosted online |
| Performs Version Control | Hosts Git repositories |
| Works offline | Internet required |
| Creates commits | Stores commits remotely |

---

## Workflow

```text
Write Code
      │
      ▼
VS Code
      │
      ▼
Git
(Local Repository)
      │
      ▼
git push
      │
      ▼
GitHub
(Remote Repository)
```

---

# Repository

A Repository (Repo) is a project managed by Git.

A Git Repository contains:

- Source code
- Project files
- Commit history
- Branches
- Configuration
- Complete version history

Without Git, a project is simply a normal folder.

---

# Local Repository

A Local Repository is a Git repository stored on your own computer.

Examples:

```
C:\Projects\KLYN_OS
```

or

```
D:\AI-AUTOMATION-ENGINEER
```

A Local Repository allows developers to work completely offline.

---

# The .git Folder

When the following command is executed:

```bash
git init
```

Git creates a hidden folder named:

```
.git
```

The `.git` folder is the brain of Git.

It stores:

- Commits
- Branches
- References
- Repository configuration
- Logs
- Complete project history

Without the `.git` folder, Git cannot manage the project.

---

# git init

```bash
git init
```

Purpose:

- Creates the hidden `.git` folder.
- Converts a normal folder into a Git Repository.
- Enables Version Control.

**Important:**

`git init` does **not** upload anything to GitHub.

---

# Repository Lifecycle

```text
Create Project
      │
      ▼
git init
      │
      ▼
Local Repository Created
      │
      ▼
Modify Files
      │
      ▼
git add
      │
      ▼
git commit
      │
      ▼
git push
      │
      ▼
GitHub
```

---

# Key Points

- Git and GitHub are different technologies.
- Git manages project history locally.
- GitHub stores repositories remotely.
- A Repository is a Git-managed project.
- A Local Repository exists on your computer.
- The `.git` folder stores all Git information.
- `git init` creates a Local Repository.
- Nothing is uploaded to GitHub until `git push` is executed.

---

# Summary

Git Fundamentals introduces the basic concepts required to work with Git. It explains the relationship between Git and GitHub, how repositories are created, how Git stores project history, and how local repositories are managed before being synchronized with remote repositories.

---

# My Understanding

Git is the software that manages my project's history on my computer. GitHub is an online service used to store and share Git repositories. A Repository is my project managed by Git, while the hidden `.git` folder stores the complete history and configuration of that project. Running `git init` creates the Local Repository, but nothing is uploaded to GitHub until I explicitly use `git push`.