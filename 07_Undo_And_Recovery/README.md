# Undo & Recovery in Git

This repository contains my hands-on practice and notes on Git Undo & Recovery commands. The purpose of this module is to understand how to safely undo changes, recover lost work, and restore previous versions of a project.

---

## 📚 Topics Covered

- git restore
- git restore --staged
- git reset
- git reset --soft
- git reset --mixed
- git reset --hard
- git revert
- git reflog
- git stash
- git stash pop
- git stash list
- git stash apply

---

## 🎯 Learning Objectives

After completing this module, I can:

- Restore modified files.
- Remove files from the staging area.
- Undo commits safely.
- Recover deleted commits.
- Temporarily save unfinished work.
- Restore stashed changes.
- Understand the difference between Reset, Restore, Revert, and Reflog.
- Recover work even after accidental mistakes.

---

## 📂 Repository Structure

```
Undo_And_Recovery/
│
├── README.md
├── Practice Files
└── Notes
```

---

## 🔑 Important Git Commands

### Check Repository Status

```bash
git status
```

### Restore File

```bash
git restore filename
```

### Remove File from Staging Area

```bash
git restore --staged filename
```

### Save Temporary Work

```bash
git stash
```

### View Stash List

```bash
git stash list
```

### Restore Stash

```bash
git stash pop
```

### Undo Last Commit (Keep Changes)

```bash
git reset --soft HEAD~1
```

### Undo Last Commit (Unstage Changes)

```bash
git reset HEAD~1
```

### Remove Last Commit Completely

```bash
git reset --hard HEAD~1
```

### Safely Undo a Commit

```bash
git revert <commit-id>
```

### View Git History (Including Lost Commits)

```bash
git reflog
```

---

## 📖 Key Concepts Learned

### git restore

Restores modified files to the last committed version.

### git restore --staged

Removes files from the staging area without deleting changes.

### git stash

Temporarily stores unfinished work.

### git reset

Moves HEAD to a previous commit.

### git revert

Creates a new commit that reverses a previous commit without rewriting history.

### git reflog

Displays every movement of HEAD and helps recover lost commits.

---

## ⚠️ Best Practices

- Always run `git status` before using Undo commands.
- Use `git revert` on shared repositories.
- Use `git reset` carefully.
- Avoid `git reset --hard` unless you are certain.
- Use `git stash` before switching tasks.
- Use `git reflog` to recover lost work.

---

## ❌ Common Mistakes

- Using `git reset --hard` accidentally.
- Forgetting to commit before resetting.
- Confusing `restore` with `reset`.
- Forgetting stashed changes.
- Using `revert` when `restore` is sufficient.

---

## 💡 Real-World Usage

Undo & Recovery commands are commonly used to:

- Fix coding mistakes.
- Recover deleted work.
- Undo incorrect commits.
- Switch between urgent tasks.
- Restore previous project versions.
- Recover lost commits after accidental resets.

---

## 🏆 Module Outcome

After completing this module, I can confidently recover files, undo mistakes, restore previous versions, and safely manage project history using Git.

---

## 📌 Author

**Bhushan**

Learning Journey:
**Python → Git & GitHub → AI Automation Engineer → Freelancer → KLYN OS → Software Company**