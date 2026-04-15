# GitHub Foundations (GH-900) - Practice Questions

Test your knowledge with these practice questions designed around the official GH-900 exam domains. Answers and explanations are provided at the end of the document.

---

## Part 1: Understand Git and GitHub Basics

**1. Which of the following best describes the difference between Git and GitHub?**
A) Git is a cloud-based service, while GitHub is a local command-line tool.
B) Git is a distributed version control system, while GitHub is a hosting service for Git repositories.
C) Git is exclusively for open-source development, while GitHub is for enterprise development.
D) There is no difference; they are different names for the same tool.

**2. Which Git command is used to take the changes from one branch and integrate them into your current branch?**
A) `git push`
B) `git clone`
C) `git merge`
D) `git status`

## Part 2: Work with GitHub Repositories

**3. What is the primary purpose of a `CODEOWNERS` file in a repository?**
A) To list all the people who have contributed to the repository.
B) To automatically request reviews from specific users or teams when changes are made to certain files.
C) To restrict who can clone the repository.
D) To declare the open-source license for the repository.

**4. You want to make an exact copy of a repository so that other people can start their own projects with the same directory structure, files, and settings. What is the best way to do this?**
A) Copy all files manually to a new folder and run `git init`.
B) Convert the repository into a template repository.
C) Create a new branch called `template`.
D) Archive the repository.

## Part 3: Collaborate using GitHub

**5. How can you link a Pull Request (PR) to an existing Issue so that the Issue automatically closes when the PR is merged?**
A) By adding the Issue number to the branch name.
B) By using a specific keyword like "Closes #123" in the PR description or commit message.
C) By adding the "linked" label to both the PR and the Issue.
D) Issues must always be closed manually after a PR is merged.

**6. What GitHub feature is best suited for long-form, multi-page documentation about how to use your software project?**
A) GitHub Issues
B) GitHub Discussions
C) GitHub Wikis
D) Commit messages

## Part 4: Apply Modern Development Practices

**7. In a GitHub Actions workflow, what defines the server (e.g., Ubuntu Linux, Windows, macOS) that your jobs will run on?**
A) The `runs-on` keyword.
B) The `on` keyword.
C) The `steps` keyword.
D) The `uses` keyword.

**8. Which GitHub feature spins up a complete, cloud-hosted development environment (container) directly from your repository?**
A) GitHub Copilot
B) GitHub Pages
C) GitHub Actions
D) GitHub Codespaces

## Part 5: Manage Projects with GitHub

**9. In GitHub Projects, you can view your work in several different formats. Which visualization shows project items running chronologically along a timeline?**
A) Board view
B) Table view
C) Roadmap / Timeline view
D) Status view

## Part 6: Understand Privacy, Security, and Administration

**10. You want to ensure that no one can push changes directly to the `main` branch. Instead, they must submit a Pull Request and get at least one approved review. What feature should you configure?**
A) Two-Factor Authentication (2FA)
B) Repository visibility settings
C) Branch protection rules or Rulesets
D) Personal Access Tokens (PATs)

**11. Which GitHub Advanced Security feature scans your repository for accidentally committed passwords, API keys, and tokens?**
A) Dependabot
B) Secret Scanning
C) CodeQL
D) GitHub Copilot

## Part 7: Explore the GitHub Community

**12. You found a bug in an open-source project that you do not have write access to. You want to fix the bug and suggest your changes to the original maintainers. What is your first step?**
A) Clone the repository to your local machine and use `git push` to upload the fix.
B) Ask the maintainers for their password.
C) Create a Fork of the repository.
D) Archive the repository.

---
---

## Answers and Explanations

**1. B**
*Explanation:* Git is the underlying version control software that runs locally, handling the commits, branches, and merges. GitHub is the cloud platform that hosts Git repositories and provides collaboration features.

**2. C**
*Explanation:* `git merge` takes changes from another branch and merges them into the branch you are currently on. `push` sends changes, `clone` copies a remote repo, and `status` checks the current state.

**3. B**
*Explanation:* `CODEOWNERS` automatically defines who is responsible for specific parts of the codebase and automatically adds them as reviewers when a PR modifies those files.

**4. B**
*Explanation:* Marking a repository as a "Template repository" allows others to generate a brand new repository with the same files and directory structure without carrying over the old commit history.

**5. B**
*Explanation:* Using keywords like "Fixes #5", "Closes #10", or "Resolves #22" in the PR description will automatically link and close the corresponding issue when the PR merges.

**6. C**
*Explanation:* While `README.md` is great for an overview, GitHub Wikis are designed for extensive, multi-page project documentation. 

**7. A**
*Explanation:* In GitHub Actions, the `runs-on` keyword determines the type of runner (e.g., `ubuntu-latest`, `windows-latest`) that will execute the job. 

**8. D**
*Explanation:* GitHub Codespaces provides an instant, cloud-based development environment fully configured to run the repository's code.

**9. C**
*Explanation:* The Roadmap (or timeline) view displays items chronologically. Board is a Kanban-style view, and Table is a spreadsheet-style view.

**10. C**
*Explanation:* Branch protection rules (and Rulesets) allow administrators to enforce workflows, such as preventing direct pushes to `main` and requiring PR reviews or status checks.

**11. B**
*Explanation:* Secret Scanning looks for exposed credentials. Dependabot monitors dependency versions, and CodeQL/Code Scanning looks for structural vulnerabilities in the code itself.

**12. C**
*Explanation:* Forking creates a personal copy of another user's repository on your own account. Once you make changes in your fork, you can submit a Pull Request back to the original ("upstream") repository.
