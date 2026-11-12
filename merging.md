# Git Merging

## 1. What is Merging?

Merging is the process of combining changes from two different branches into one branch.

In Git, developers can work on separate branches without affecting each other's work. After finishing their tasks, they can merge their changes into the main branch.

## 2. Why Do We Use Merge?

Merging helps developers to:
- Combine different features.
- Work on the same project independently.
- Keep the main branch organized.
- Integrate changes made by team members.

## 3. Types of Merge

There are two common types of merging:

**Fast-Forward Merge:**

This happens when the main branch has no new commits since the feature branch was created. Git simply moves the branch pointer forward.

**Three-Way Merge:**

This happens when both branches have new commits. Git combines the changes using their common ancestor.

## 4. How to Merge Branches

Follow these steps:

**Step 1: Switch to the main branch**

```bash
git checkout main
```

**Step 2: Get the latest changes**

```bash
git pull origin main
```

**Step 3: Merge the feature branch**

```bash
git merge feature/login
```

**Step 4: Push the changes**

```bash
git push origin main
```

## 5. Practical Example

Imagine two developers are working on a website.

- Developer 1 creates a branch called `feature/login`.
- Developer 2 works on another branch called `feature/register`.

After finishing their tasks, both branches can be merged into the main branch.

```bash
git checkout main
git merge feature/login
git merge feature/register
```

Now both features are included in the main branch.

## 6. Merge Conflicts

A merge conflict happens when Git cannot automatically combine changes from different branches.

For example, two developers change the same line in a file.

Git shows conflict markers like this:

```text
<<<<<<< HEAD
Hello from Main
=======
Hello from Feature
>>>>>>> feature/login
```

To solve the conflict:

1. Open the conflicted file.
2. Choose the correct changes or combine them.
3. Remove the conflict markers.
4. Save the file.
5. Complete the merge.

```bash
git add .
git commit -m "Resolve merge conflict"
```

## 7. Useful Git Commands

| Command | Description |
|---|---|
| `git branch` | Shows all branches |
| `git checkout main` | Switches to main |
| `git merge branch-name` | Merges a branch |
| `git merge --abort` | Cancels a merge |
| `git status` | Shows repository status |
| `git log --oneline` | Shows commit history |

## Conclusion

Merging is an important part of teamwork in Git. It allows developers to combine their work and build a complete project together.