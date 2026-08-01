# Merge Conflicts

A Merge Conflict occurs when Git is unable to automatically merge changes from two different branches because the same part of a file has been modified differently.

Git stops the merge and asks the developer to manually decide which changes should be kept.

---

# What is a Merge Conflict?

A Merge Conflict happens when two branches modify the same file, same line, or same section differently.

Git cannot determine which version is correct.

Instead of guessing, Git pauses the merge and requests manual resolution.

---

# Why Do Merge Conflicts Occur?

Merge conflicts commonly occur when:

- Two developers edit the same line of code.
- Two developers rename the same file differently.
- One branch deletes a file while another branch modifies it.
- The same configuration file is changed differently in multiple branches.

---

# Real-World Example

Suppose Developer A and Developer B are working on KLYN OS.

Developer A

```
feature-ai-chatbot
```

Changes:

```
Button Text

"Start Chat"
```

Developer B

```
feature-ui-update
```

Changes:

```
Button Text

"Start AI Assistant"
```

Both developers modified the same line.

When Git tries to merge:

```
feature-ai-chatbot
        │
        ▼
      Merge
        │
        ▼
feature-ui-update
```

Git cannot decide which button text is correct.

A Merge Conflict occurs.

---

# How Git Responds

Git stops the merge.

Example:

```text
CONFLICT (content): Merge conflict in chatbot.py

Automatic merge failed; fix conflicts and then commit the result.
```

Git never guesses.

The developer must resolve the conflict manually.

---

# Conflict Markers

Git marks conflicting sections like this:

```text
<<<<<<< HEAD

Start Chat

=======

Start AI Assistant

>>>>>>> feature-ai-chatbot
```

Meaning:

```
<<<<<<< HEAD
```

Current branch.

```
=======
```

Separator.

```
>>>>>>> feature-ai-chatbot
```

Incoming branch.

The developer chooses one version or combines both.

---

# Resolving a Merge Conflict

Step 1

Open the conflicted file.

Step 2

Review both versions.

Step 3

Edit the file manually.

Example:

```
Start AI Chat
```

Step 4

Save the file.

Step 5

Stage the resolved file.

```bash
git add chatbot.py
```

Step 6

Complete the merge.

```bash
git commit
```

Git creates the merge commit.

---

# Merge Conflict Workflow

```
Branch A
      │
      ▼
Modify File

Branch B
      │
      ▼
Modify Same File

        │
        ▼
      Merge

        │
        ▼
Merge Conflict

        │
        ▼
Resolve Conflict

        │
        ▼
Commit Merge
```

---

# Best Practices to Avoid Merge Conflicts

- Pull the latest changes before starting work.
- Create small feature branches.
- Commit changes frequently.
- Merge branches regularly.
- Communicate with team members.
- Avoid editing the same files simultaneously when possible.

---

# Key Commands

Check repository status:

```bash
git status
```

Stage resolved files:

```bash
git add .
```

Complete merge:

```bash
git commit
```

Abort an unfinished merge:

```bash
git merge --abort
```

---

# Summary

A Merge Conflict occurs when Git cannot automatically combine changes from different branches because both branches modify the same part of the project. Git pauses the merge, marks the conflicting sections, and allows the developer to manually resolve the conflict before completing the merge.

---

# My Understanding

A Merge Conflict is Git's safety mechanism. Instead of automatically choosing one developer's changes and potentially losing the other developer's work, Git stops the merge and asks the developer to resolve the conflict manually. After reviewing and fixing the conflicting code, the changes are committed, completing the merge safely.