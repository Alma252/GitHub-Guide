# GitHub Collaboration

## 1. What is Collaboration?

Collaboration means working together with other developers on the same software project.

GitHub provides useful tools that allow team members to share code, review changes, and manage tasks.

## 2. What is a Collaborator?

A Collaborator is a person who has permission to contribute to a repository.

The repository owner can invite other developers as collaborators.

After accepting the invitation, collaborators can work on the project according to their permissions.

## 3. What is an Issue?

An Issue is used to report problems, suggest new features, or assign tasks to team members.

For example, a team can create an Issue called:

`Create Login Page`

Then assign it to a developer.

## 4. What is a Pull Request?

A Pull Request (PR) is a request to merge changes from one branch into another branch.

Developers use Pull Requests to show their changes and ask other team members to review them.

## 5. How to Create a Pull Request

Follow these steps:

**Step 1: Create a new branch**

```bash
git checkout -b feature/login
```

**Step 2: Make changes to your files.**

**Step 3: Save changes with a commit**

```bash
git add .
git commit -m "Add login feature"
```

**Step 4: Push the branch to GitHub**

```bash
git push -u origin feature/login
```

**Step 5: Open GitHub and create a Pull Request.**

Select the source branch and the target branch, then click Create Pull Request.

## 6. What is Code Review?

Code Review is the process of checking another developer's code before merging it.

Team members can:
- Check the code for errors.
- Suggest improvements.
- Ask questions.
- Approve the changes.

Reviewing code helps improve project quality.

## 7. Practical Example

Imagine three developers are working on a website:

- Developer 1 creates the login page.
- Developer 2 creates the registration page.
- Developer 3 reviews their Pull Requests.

Each developer works on a separate branch and submits a Pull Request.

After reviewing and approving the changes, the team can merge them into the main branch.

## 8. Useful GitHub Features

| Feature | Description |
|---|---|
| Repository | Stores project files |
| Collaborator | A team member with repository access |
| Issue | Used to manage tasks and problems |
| Branch | An independent version of the project |
| Pull Request | Requests merging changes |
| Review | Checks changes made by developers |
| Actions | Automates workflows |

## Conclusion

GitHub makes teamwork easier by providing tools for task management, code sharing, and reviewing changes. Collaboration helps developers work together more effectively.