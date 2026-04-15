# GitHub Foundations (GH-900) Study Notes

This document provides a comprehensive overview of the topics covered in the GitHub Foundations (GH-900) certification exam.

## 1. Git and GitHub Basics (25-30%)

### What is Version Control?
Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later. It allows multiple people to work on a project simultaneously without overwriting each other's changes.
- **Benefits:** History tracking, collaboration, branch management, traceability, and backup.

### Git vs. GitHub
- **Git:** A free, open-source distributed version control system (VCS) created by Linus Torvalds. It runs locally on your machine and tracks changes to files.
- **GitHub:** A cloud-based hosting service that lets you manage Git repositories. It provides a web interface and additional features like issue tracking, continuous integration (CI), and collaboration tools.

### Core Git Concepts
- **Repository (Repo):** A folder where your project files and their revision history are stored. It contains a `.git` directory.
- **Commit:** A snapshot of your repository at a specific point in time. Every commit has a unique hash (SHA-1). 
- **Branch:** A parallel version of a repository. It allows you to work freely without affecting the "main" or "master" branch.
- **Merge:** The process of taking changes from one branch and integrating them into another.
- **Clone:** A local copy of a remote repository.
- **Push:** Sending your local committed changes to a remote repository (like GitHub).
- **Pull:** Fetching changes from a remote repository and merging them into your local branch.

## 2. Working with GitHub Repositories (10-15%)

### Repository Structure & Key Files
- **`README.md`:** The instruction manual for your project. Usually the first file people see.
- **`LICENSE`:** Defines how others can use, modify, and distribute your code. 
- **`CONTRIBUTING.md`:** Guidelines for how other developers can contribute to your project.
- **`CODEOWNERS`:** Defines which individuals or teams own specific parts of the code and automatically requests their review on pull requests touching those files.
- **`SECURITY.md`:** Instructions on how to report security vulnerabilities responsibly.
- **`.gitignore`:** Specifies intentionally untracked files that Git should ignore (e.g., build artifacts, sensitive keys).

### Managing Repositories
- **Repository Visibility:** Public (anyone can see), Private (only you and chosen collaborators), Internal (only available to enterprise members).
- **Templates:** You can mark a repo as a "template" so others can generate new repositories with the exact same directory structure and files.
- **Archiving:** Making a repository read-only.
- **Insights & Metrics:** GitHub provides data on traffic, commits over time, and dependency graphs to help maintainers see how their repo is being used.

## 3. Collaborate using GitHub (10-15%)

### Issues
Use issues to track ideas, enhancements, tasks, or bugs. They can be organized using:
- **Labels:** Categorize issues (e.g., `bug`, `enhancement`, `good first issue`).
- **Milestones:** Group issues and pull requests by a specific target or date.
- **Assignees:** Assign tasks to specific collaborators.
- **Issue Templates:** Standardized forms for users to fill out when opening a new issue.

### Pull Requests (PRs)
A proposal to merge a set of changes from one branch into another.
- **Code Review:** Collaborators can comment on specific lines of code, approve changes, or request modifications.
- **Linking:** You can link a PR to an issue (e.g., typing "Closes #42" in the PR description will automatically close issue #42 when the PR is merged).
- **Draft PRs:** Indicate that a PR is a work in progress and not ready for review.

### Other Collaboration Tools
- **Discussions:** A forum-like feature for community conversations, Q&A, and announcements.
- **GitHub Wikis:** A place to host extensive documentation for your project.
- **GitHub Pages:** A static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository and publishes a website.
- **Gists:** A simple way to share snippets of code or text.

## 4. Modern Development Practices (10-15%)

### GitHub Copilot
An AI pair programmer that offers autocomplete-style suggestions as you code. It is powered by OpenAI models and trained on public repositories.

### GitHub Codespaces
A complete, configurable development environment in the cloud hosted on GitHub. It spins up a container (Linux) with your code, extensions, and tools already configured, directly accessible via a browser or VS Code.

### GitHub Actions
A continuous integration and continuous delivery (CI/CD) platform that allows you to automate your build, test, and deployment pipeline.
- **Workflows:** Defined in YAML files in the `.github/workflows` directory.
- **Events:** Triggers that start a workflow (e.g., `push`, `pull_request`, `schedule`).
- **Jobs:** A set of steps that execute on the same runner.
- **Runners:** The server (Ubuntu, Windows, macOS) that runs your workflows.

## 5. Manage Projects with GitHub (5-10%)

### GitHub Projects (ProjectsV2)
A customizable, spreadsheet-like tool that integrates directly with your issues and PRs to help track and plan work.
- **Views:** Board (Kanban), Table, Timeline.
- **Custom Fields:** Add custom metadata (text, number, date, single select) to your items.
- **Automation:** Built-in workflows to automate moving cards when a PR is opened or closed.

## 6. Privacy, Security, and Administration (10-15%)

### Authentication & Access
- **2FA (Two-Factor Authentication):** Requires a second form of verification (SMS, Authenticator app, Passkeys) when logging in.
- **Roles & Permissions:** Define what users can do in a repository (Read, Triage, Write, Maintain, Admin).
- **Personal Access Tokens (PATs):** Used as an alternative to passwords for Git over HTTPS.

### Repository Protections
- **Branch Protection Rules:** Enforce specific workflows before a branch can be merged (e.g., require pull request reviews, require status checks to pass, prevent forceful pushing).
- **Rulesets:** A newer, more flexible way to define branch and tag protections at the repository or organization level.

### Advanced Security
- **Dependabot:** Alerts you when a repository uses a vulnerable dependency and can automatically create PRs to update them.
- **Secret Scanning:** Scans repositories for exposed secrets (tokens, private keys) and alerts the specific provider or repo owner.
- **Code Scanning (CodeQL):** Analyzes code to find security vulnerabilities and errors.

## 7. Explore the GitHub Community (5-10%)

### Open Source Ecosystem
- **Forks:** A personal copy of someone else's project. Used to propose changes to someone else's project or start your own version.
- **InnerSource:** Applying open-source practices and principles internally within a company.
- **GitHub Sponsors:** A way to financially support the developers who build the open-source projects you use.
- **GitHub Marketplace:** A place to discover and purchase tools (GitHub Actions, Apps) that extend your GitHub workflow.

---

## Exam Tips
- **Passing Score:** 700 / 1000.
- **Focus:** Understand the *purpose* behind features rather than just memorizing definitions. Know *when* to use what (e.g., when to use a Fork vs. a Branch).
- **Hands-on:** The best way to study is to create a free GitHub account, initialize a repository, create issues, open a pull request, and configure a simple GitHub Actions workflow.
