[Home](../README.md) | [Git](git.md) | [Cline](cline.md)

# Git Guide

This guide provides a concise overview of a Git workflow, branching strategy, and common operations.

## Branching Strategy

- **main** or **master** branch: The stable branch, containing the most up-to-date, production-ready code.
- **Feature branches:** Create a new branch for each feature or bug fix (e.g., `feature/add-login`, `bugfix/resolve-navigation`).
- **Never commit directly to main!**

## Basic Workflow

1.  **Clone the repository:**

    - `git clone <repository_url>`

2.  **Create a feature branch:**

    - `git checkout -b <your-feature-branch>`

3.  **Work on your feature:**

    - Write code, test, etc.

4.  **Stage changes:**

    - `git add .` (stages all changes) or `git add <file>` (stages specific files)

5.  **Commit changes:**

    - `git commit -m "Meaningful commit message"`

6.  **Push your branch:**

    - `git push origin <your-feature-branch>`

7.  **Create a Pull Request (PR):**

    - On GitHub, create a PR from your feature branch to `main`.

8.  **Code Review:**

    - Other team members review the code, provide feedback, and suggest changes.

9.  **Address Feedback (if necessary):**

    - Make changes based on feedback and push updates to your branch.

10. **Merge the PR:**

    - Once approved, merge your feature branch into `main`.

11. **Update local main:**
    - `git checkout main`
    - `git pull origin main`

## Common Scenarios

### Integrating Changes from a Merged Feature Branch

**Scenario:** You're working on `feature/incomplete` and want to integrate changes from a merged `feature/completed` branch (which is now part of `main`).

1.  **Switch to your branch:**
    - `git checkout feature/incomplete`
2.  **Fetch latest changes (optional, but good practice):**
    - `git fetch origin main`
3.  **Merge `main` into your branch:**
    - `git merge origin/main`
    - Resolve any merge conflicts that arise.

### Notifying Team of Completed Feature

**Scenario:** You've finished work on `feature/completed` and want others to review it.

1.  **Push your branch:**
    - `git push origin feature/completed`
2.  **Create a Pull Request:**
    - Create a PR from `feature/completed` to `main` on GitHub.
3.  **Inform the Team:**
    - Notify your team through your communication channel (e.g., Slack, email) about the new PR.
