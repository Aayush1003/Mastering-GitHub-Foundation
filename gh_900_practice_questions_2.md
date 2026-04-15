# GitHub Foundations (GH-900) - Practice Test 2 (Scenario-Based Questions)

This second set of questions focuses a bit more on scenarios and specific feature nuances to ensure you are fully prepared for the exam. Answers and explanations are at the bottom.

---

## Part 1: More on Git and GitHub

**1. You are working on a new feature and realize your commit message contained a typo. You haven't pushed the commit to GitHub yet. Which of the following is the best way to fix the commit message locally?**
A) Run `git revert` and make a new commit.
B) Run `git commit --amend` to rewrite the last commit message.
C) Run `git push --force` to send the correct message.
D) Delete the repository and clone it again.

**2. Which authentication method uses a pair of cryptographic keys (one public, one private) so you can push and pull from a repository without typing your GitHub username and password every time?**
A) SSL Authentication
B) SSH (Secure Shell) Keys
C) HTTPS standard passwords
D) Advanced Security Tokens

## Part 2: Repository Features

**3. You want to share a single file with some code output logs quickly but don't want to create a full repository. Which GitHub feature is designed specifically for sharing code snippets or single files?**
A) GitHub Gist
B) GitHub Pages
C) GitHub Packages
D) GitHub Repositories

**4. Your organization wants to encourage developers across different teams (who don't normally work together) to openly contribute code to each other's proprietary, internally-hosted projects using open-source workflows (like Forks and PRs). What is this practice called?**
A) Open Source
B) InnerSource
C) Crowdsourcing
D) Closed Source

## Part 3: Collaboration & PRs

**5. You created a Pull Request but you know the code is not finished and isn't ready for a formal review. What is the best way to signal to your team that they should wait to review it?**
A) Turn on branch protection.
B) Add a `WIP` label and hope they notice.
C) Convert the Pull Request to a "Draft Pull Request".
D) Delete the PR and open it later.

**6. A maintainer wants to track the overall progress of an upcoming release called "v2.0" and group several issues and pull requests together under this single target. What feature should they use?**
A) GitHub Discussions
B) Milestones
C) GitHub Wikis
D) CODEOWNERS

## Part 4: GitHub Actions & Codespaces

**7. In a GitHub Actions workflow, you need a job to only trigger when a push is made specifically to the `main` branch. How do you configure this?**
A) Inside the `on: push` block, use the `branches: [main]` filter.
B) Use the `only-main: true` keyword.
C) Set a branch protection rule to trigger the action.
D) Actions can only trigger on all branches automatically.

**8. You are working in a GitHub Codespace. How do you ensure that any custom VS Code extensions or settings you need are automatically installed for anyone else who starts a Codespace in your repository?**
A) Commit a `.vscode/settings.json` and a `devcontainer.json` file.
B) Instruct developers to manually install them in the `README.md`.
C) Use GitHub Actions to install the extensions.
D) Configure it in the repository Settings page under the Secrets tab.

## Part 5: Projects & Tracking

**9. In a GitHub Project (ProjectsV2), what is the purpose of a "Custom Field"?**
A) To change the CSS styling of the project board.
B) To add specific metadata to issues (like 'Priority', 'T-Shirt Size', or 'Target Date') that isn't native to standard GitHub Issues.
C) To allow non-GitHub users to comment on issues.
D) To rename issues automatically.

## Part 6: Security

**10. A developer accidentally pushed a file containing a plaintext AWS API Key to a public GitHub repository. What will happen if Secret Scanning is enabled?**
A) GitHub will automatically delete the repository to prevent a data leak.
B) GitHub relies on Dependabot to inform the developer.
C) GitHub will silently notify AWS, who may automatically revoke the key to protect the account, and the repository admins will be alerted.
D) GitHub will prevent the `git push` command from completing entirely if it's the free tier.

**11. What is the role of GitHub Dependabot?**
A) It automatically writes code for you based on comments.
B) It monitors your repository's dependencies for known security vulnerabilities and can automatically open PRs to update them.
C) It prevents unauthorized users from cloning your code.
D) It tracks your developer metrics and productivity.

---
---

## Answers and Explanations

**1. B**
*Explanation:* `git commit --amend` allows you to modify the most recent commit. Since it hasn't been pushed yet, this is the safest and cleanest way to fix a typo in the message.

**2. B**
*Explanation:* SSH uses a public/private key pair to securely authenticate your machine with GitHub without requiring your account password for each operation.

**3. A**
*Explanation:* GitHub Gists are designed to instantly share code snippets, notes, or single files. They can be secret or public. Pages is for web hosting, and Packages is for hosting software packages (like npm or Docker images).

**4. B**
*Explanation:* InnerSource is the practice of applying open-source methodologies (like open collaboration, issues, forks, and PRs) to proprietary software development within the boundaries of a single organization.

**5. C**
*Explanation:* Draft Pull Requests clearly indicate that the code is still in progress. They cannot be merged until they are marked as "Ready for Review," explicitly preventing accidental merges.

**6. B**
*Explanation:* Milestones allow you to group related issues and pull requests, and assign a due date. This makes them perfect for tracking progress toward a specific release version.

**7. A**
*Explanation:* The `on` keyword defines the trigger. To limit it, you provide a filter under the event: `on: push: branches: - main`.

**8. A**
*Explanation:* A Development Container (`devcontainer.json`) allows you to define the exact environment variables, extensions, and setup scripts needed for a Codespace, ensuring a consistent environment for all developers.

**9. B**
*Explanation:* Custom Fields let you track repository-agnostic data (like Priority levels, estimates, or custom dates) directly within your Project views, customizing how you track work.

**10. C**
*Explanation:* Secret Scanning partners with many service providers (like AWS, Azure, Google Cloud). When a secret is detected in a public repo, GitHub alerts the provider, who often automatically revokes it to prevent abuse.

**11. B**
*Explanation:* Dependabot helps secure your software supply chain by finding outdated or vulnerable dependencies and raising Pull Requests to bump them to secure versions.
