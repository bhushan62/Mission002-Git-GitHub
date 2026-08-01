# Merging

Merging is the process of combining changes from one Git branch into another. It is used after a feature has been developed, tested, and committed in a separate branch.

---

# What is Merging?

A merge brings the completed work from one branch into another branch.

Most commonly:

```
feature branch
        │
        ▼
      Merge
        │
        ▼
       main
```

After merging, the changes become part of the main project.

---

# Why Do We Need Merging?

Without merging, every completed feature would remain isolated inside its own branch.

Example:

```
main
```

```
feature-login
```

```
feature-payment
```

```
feature-ai-chatbot
```

None of these features become part of the actual application until they are merged into `main`.

---

# Real-World Example

Suppose we are building KLYN OS.

```
main
│
├── Billing
├── Customers
└── Reports
```

We create a new branch:

```
feature-ai-chatbot
```

Inside this branch we develop:

```
AI Chatbot
```

After testing:

```
feature-ai-chatbot
        │
        ▼
      Merge
        │
        ▼
       main
```

Now the project becomes:

```
main

Billing
Customers
Reports
AI Chatbot
```

---

# Merge Workflow

```
Create Branch
        │
        ▼
Develop Feature
        │
        ▼
Commit Changes
        │
        ▼
Switch to main
        │
        ▼
Merge Branch
        │
        ▼
Delete Branch (optional)
```

---

# Fast-Forward Merge

A Fast-Forward Merge happens when the main branch has not changed since the feature branch was created.

Example:

```
A ----- B (main)

         \
          \
           C (feature)
```

After merge:

```
A ----- B ----- C

              ▲
              │
             main
```

Git simply moves the `main` pointer forward.

No extra merge commit is created.

---

# Deleting a Merged Branch

After successfully merging a completed feature, the feature branch is usually deleted.

This keeps the repository clean.

Deleting a merged branch does **not** remove the work because the commits already exist inside `main`.

---

# Key Commands

## Merge a branch

```bash
git switch main
git merge feature-branch
```

---

## Delete merged branch

```bash
git branch -d feature-branch
```

---

## View branches

```bash
git branch
```

---

# Best Practices

- Never develop directly on `main`.
- Create one branch for one feature.
- Commit frequently.
- Test the feature before merging.
- Merge only completed work.
- Delete old branches after successful merges.

---

# Summary

Merging combines the work from one branch into another. Developers usually create feature branches, complete the work independently, commit the changes, merge them into `main`, and finally remove the feature branch. This workflow keeps projects organized, safe, and easy to manage.

---

# My Understanding

A merge is the process of bringing completed work from a feature branch into the main project. Instead of developing directly on `main`, each feature is built in its own branch. After testing and committing the feature, it is merged into `main`, making it part of the application. Once merged successfully, the feature branch can be deleted because its work is already stored in `main`.