# Branches

Branches are one of Git's most powerful features. They allow developers to work on new features, bug fixes, or experiments without affecting the main project.

---

# What is a Branch?

A branch is an independent line of development within a Git repository.

Instead of modifying the main project directly, developers create a separate branch to work safely.

Every branch contains the complete project history up to the point where it was created.

---

# Why Do We Need Branches?

Without branches, every developer would modify the same codebase.

Problems:

- Bugs could break the application.
- New features could interfere with stable code.
- Multiple developers could overwrite each other's work.

Branches solve these problems by isolating development.

---

# Main Branch

The default branch in most Git repositories is:

```text
main
```

The **main** branch should always contain stable, working code.

New development should normally happen in separate branches.

---

# Branch Workflow

```text
               main
                 │
                 │
        ─────────┼─────────
                 │
        Create Branch
                 │
                 ▼
         feature-login
                 │
          Work & Commit
                 │
                 ▼
             Merge
                 │
                 ▼
               main
```

---

# Creating a Branch

Create a new branch:

```bash
git branch feature-login
```

This creates the branch but does not switch to it.

---

# Viewing Branches

Display all local branches:

```bash
git branch
```

Example:

```text
* main
  feature-login
```

The asterisk (*) indicates the currently active branch.

---

# Switching Branches

Switch to another branch:

```bash
git checkout feature-login
```

or using the newer Git command:

```bash
git switch feature-login
```

The current working directory now reflects the selected branch.

---

# Create and Switch Together

Create a branch and switch to it immediately:

Older syntax:

```bash
git checkout -b feature-login
```

Newer syntax:

```bash
git switch -c feature-login
```

---

# Working on a Branch

After switching to a branch:

- Edit files
- Save changes
- Stage changes
- Commit changes

Example:

```bash
git add .
git commit -m "Add login feature"
```

These commits belong only to the current branch until they are merged.

---

# Listing All Branches

Show local branches:

```bash
git branch
```

Show remote branches:

```bash
git branch -r
```

Show both local and remote branches:

```bash
git branch -a
```

---

# Deleting a Branch

Delete a branch after it has been merged:

```bash
git branch -d feature-login
```

Force delete:

```bash
git branch -D feature-login
```

---

# Real-World Example

Suppose we are developing KLYN OS.

The **main** branch contains the stable application.

```
main
│
├── Billing
├── Customer Management
├── Reports
└── WhatsApp Automation
```

Now we want to develop an AI Billing Assistant.

Instead of changing **main**, we create:

```
feature-ai-billing
```

All development happens safely inside that branch.

Once testing is complete, it is merged back into **main**.

---

# Advantages of Branches

- Safe development
- Easy experimentation
- Parallel development
- Better collaboration
- Isolated bug fixes
- Cleaner project history

---

# Best Practices

- Keep the **main** branch stable.
- Create a separate branch for every new feature.
- Give branches meaningful names.
- Commit frequently.
- Merge only after testing.

---

# Key Commands

Create a branch:

```bash
git branch branch-name
```

Switch branches:

```bash
git switch branch-name
```

or

```bash
git checkout branch-name
```

Create and switch:

```bash
git switch -c branch-name
```

List branches:

```bash
git branch
```

Delete a branch:

```bash
git branch -d branch-name
```

---

# Summary

Branches allow developers to work independently without affecting the main project. They provide isolated development environments, making collaboration, feature development, and bug fixing much safer and more organized.

---

# My Understanding

A branch is like creating a separate copy of my project where I can develop a new feature or fix a bug without affecting the stable version. Once my work is complete and tested, I can merge those changes back into the main branch. Branches make development safer, cleaner, and more efficient, especially when multiple developers work on the same project.