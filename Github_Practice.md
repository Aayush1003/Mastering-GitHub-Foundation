# GitHub Foundation (GH-900) - MCQ Practice Question Paper

**Exam Code:** GH-900  
**Total Questions:** 112  
**Recommended Time:** 120-150 minutes  
**Passing Score:** ~70% (varies by exam)  
**Difficulty Mix:** 30% Easy • 50% Medium • 20% Hard

---

## Instructions

- This practice paper contains **112 multiple-choice questions** covering all domains of the GitHub Foundation certification
- Each question has **4 options (A-D)** with a single correct answer
- **Difficulty indicators:** ⭐ (Easy) • ⭐⭐ (Medium) • ⭐⭐⭐ (Hard)
- Answers and detailed explanations are provided inline
- Recommended approach: Complete untimed first, then retake timed (1-1.5 min per question)
- Use the **Answer Key Summary** at the end for quick reference

---

## Section 1: Introduction to GitHub & Git Fundamentals (10 Questions)

**Q1.** What is the primary difference between Git and GitHub? ⭐
- A) Git is a cloud platform; GitHub is a version control system
- B) Git is a version control system; GitHub is a cloud-based hosting platform for Git repositories
- C) Git is only for individual developers; GitHub is for teams only
- D) There is no practical difference; they are the same thing

**Answer:** B  
**Explanation:** Git is a distributed version control system that runs locally on your machine, while GitHub is a cloud-based platform that hosts Git repositories and provides collaboration tools. Git is the underlying technology; GitHub is the service that provides hosted Git repositories and additional features like pull requests, issues, and discussions.

---

**Q2.** You're setting up version control for a project. What is the correct sequence of Git operations to start tracking changes? ⭐
- A) git commit → git add → git push → git init
- B) git init → git add → git commit → git push
- C) git add → git commit → git init → git push
- D) git push → git init → git add → git commit

**Answer:** B  
**Explanation:** The correct workflow is: (1) `git init` initializes a new repository, (2) `git add` stages your changes, (3) `git commit` creates a snapshot, (4) `git push` sends commits to the remote. The other options have incorrect ordering.

---

**Q3.** What does a commit message should ideally contain? ⭐⭐
- A) Long, detailed descriptions of everything that changed
- B) A clear, concise description of what changed and why
- C) Technical implementation details and code snippets
- D) References to all files modified

**Answer:** B  
**Explanation:** Good commit messages should be clear and concise, explaining what changed and why—this helps with code review and future understanding. They should be descriptive enough to understand intent but not so verbose that they're difficult to scan. Very long messages or just technical details make history harder to navigate.

---

**Q4.** What is a branch in Git? ⭐
- A) A backup copy of your entire repository
- B) An independent line of development that allows parallel work without affecting other branches
- C) A tag that marks a specific commit
- D) A temporary file storage area

**Answer:** B  
**Explanation:** A branch is an independent line of development. You can work on branches without affecting other branches, making them essential for feature development. The default branch is usually "main," and you create feature branches for specific work. Branches are lightweight and allow parallel development.

---

**Q5.** When should you use `git clone` instead of `git init`? ⭐⭐
- A) `git clone` is only for copying, `git init` is for starting new projects
- B) Use `git clone` to download an existing remote repository; use `git init` to create a new repository locally
- C) They are interchangeable; use whichever you prefer
- D) `git clone` is deprecated; always use `git init`

**Answer:** B  
**Explanation:** `git clone` downloads an existing repository (with full history) from a remote location like GitHub. `git init` creates a brand new, empty repository locally. Use `init` for new projects; use `clone` to work with existing remote projects.

---

**Q6.** You accidentally added a file to staging area but haven't committed yet. How do you unstage it? ⭐⭐
- A) `git remove <file>`
- B) `git undo`
- C) `git reset <file>`
- D) `git revert <file>`

**Answer:** C  
**Explanation:** `git reset <file>` removes a file from the staging area without losing your changes. The file remains modified in your working directory but is no longer staged. `git revert` creates a new commit undoing changes; `git remove` is not a valid command. This is one of the most common staging undo operations.

---

**Q7.** What is the purpose of the `.gitignore` file? ⭐
- A) It specifies which users are ignored in the project
- B) It lists files and patterns that Git should ignore when tracking changes
- C) It prevents certain users from pushing code
- D) It marks files as read-only

**Answer:** B  
**Explanation:** `.gitignore` tells Git which files or directories to ignore (not track). This is useful for excluding dependency folders (node_modules), environment files (.env), OS files, and compiled output. Files matching patterns in `.gitignore` won't be staged or committed.

---

**Q8.** What is the difference between `git fetch` and `git pull`? ⭐⭐
- A) `git fetch` is faster; `git pull` is slower
- B) `git fetch` downloads changes without merging; `git pull` downloads and automatically merges
- C) `git fetch` is for branches; `git pull` is for tags
- D) They are identical; use whichever you prefer

**Answer:** B  
**Explanation:** `git fetch` retrieves remote changes and updates your remote-tracking branches (origin/main) without modifying your local working branch. `git pull` combines `git fetch` + `git merge`, automatically merging remote changes. Fetch is safer for review; pull is faster when you want immediate updates.

---

**Q9.** What information does a Git commit contain? ⭐⭐
- A) Only the changed lines of code
- B) Author, timestamp, commit hash, commit message, and reference to parent commit(s)
- C) Only usernames of people who edited the files
- D) Only the commit message

**Answer:** B  
**Explanation:** Each commit is an immutable snapshot containing: a unique hash (ID), author name and email, timestamp, commit message, and reference(s) to parent commit(s). This metadata creates the complete history and enables Git's powerful tools like blame and bisect.

---

**Q10.** You're reviewing a repository's history and want to see all commits with one-line summaries. What command would you use? ⭐⭐
- A) `git log --oneline`
- B) `git history --brief`
- C) `git commits --summary`
- D) `git show --all`

**Answer:** A  
**Explanation:** `git log --oneline` displays commit history with one-line summaries showing commit hash and message. This is the most efficient way to scan commit history. `git log` alone shows detailed information; `--oneline` makes it scannable. Other options aren't valid Git commands for this purpose.

---

## Section 2: Working with GitHub Repositories (10 Questions)

**Q11.** You're starting a new team project on GitHub. What are the essential files you should include in the repository root? ⭐⭐
- A) Only the source code files
- B) README.md and .gitignore at minimum; LICENSE and CONTRIBUTING.md recommended
- C) .git folder and config files
- D) Nothing; start with an empty repository

**Answer:** B  
**Explanation:** Best practices include: README (project description and setup), .gitignore (exclude unneeded files), LICENSE (usage rights), and CONTRIBUTING.md (contribution guidelines). These files are essential for a professional project. The .git folder is created automatically; it shouldn't be manually added.

---

**Q12.** What is the primary purpose of a README file in a GitHub repository? ⭐
- A) To store configuration settings
- B) To provide an overview of the project, setup instructions, and usage guidelines
- C) To track bug reports
- D) To store secret tokens

**Answer:** B  
**Explanation:** A README is the first file visitors see. It should explain what the project does, how to install it, usage examples, contributing guidelines, and license. It's critical for attracting contributors and helping new users understand the project quickly.

---

**Q13.** You've just created a private repository on GitHub for your company's internal tool. Later, you need to allow an external contractor to work on it. What is the best approach? ⭐⭐
- A) Change the repository to public
- B) Make the contractor an organization member
- C) Add the contractor as an outside collaborator with appropriate permissions
- D) Have them fork the repository

**Answer:** C  
**Explanation:** Adding an outside collaborator gives specific permissions to an external person without making the repo public or making them a full org member. You control exactly what they can access and modify. Making it public exposes everything; forking is for contributions, not team collaboration.

---

**Q14.** What happens when you fork a repository on GitHub? ⭐
- A) You create a backup copy that syncs automatically with the original
- B) You create an independent copy under your account that you fully control
- C) The original repository is archived
- D) You become a direct collaborator on the original repository

**Answer:** B  
**Explanation:** Forking creates a complete, independent copy of the repository under your GitHub account. You own it outright; changes to the original don't affect your fork. This is the standard workflow for open-source contributions: fork → clone → make changes → pull request to original.

---

**Q15.** Your repository is public, but you realize it contains sensitive API keys. What's the immediate action you should take? ⭐⭐⭐
- A) Delete the entire repository
- B) Change the repository to private immediately and rotate the credentials (never use the exposed ones again)
- C) Just remove the keys from the current code; the commits don't matter
- D) Hope nobody saw it; the history isn't important

**Answer:** B  
**Explanation:** Exposed secrets in a public repo are a serious security issue, even if deleted from current code, because they exist in Git history. Immediate action: (1) Change to private, (2) Rotate/invalidate the exposed credentials, (3) Use a tool like git-filter-branch or BFG to remove from history. GitHub has secret scanning that alerts you automatically.

---

**Q16.** What is the difference between cloning and forking a repository? ⭐⭐
- A) Cloning downloads to your local machine; forking creates a GitHub copy you own
- B) They are identical operations
- C) Forking is for private repos; cloning is for public
- D) Cloning creates a backup; forking creates a branch

**Answer:** A  
**Explanation:** Clone = download a repo locally to your machine (read-only or if you have access). Fork = create an independent GitHub copy under your account. You fork when you want to work independently (open source contributions); you clone after to work locally.

---

**Q17.** You want to change your repository from public to private. Where would you find this setting? ⭐
- A) Repository branch settings
- B) Repository Settings → Danger Zone → Change visibility
- C) Team settings
- D) GitHub billing settings

**Answer:** B  
**Explanation:** Repository visibility (public/private/internal) is in Settings → General or Settings → Danger Zone → Change visibility, depending on GitHub's current UI. You need admin access to change repository visibility. Changing to private is irreversible from web UI for some versions.

---

**Q18.** What is a repository template in GitHub? ⭐⭐
- A) A branch containing boilerplate code
- B) A special repository marked as a template that others can use to create new repositories pre-populated with its structure
- C) A document describing the repo structure
- D) A GitHub Actions workflow

**Answer:** B  
**Explanation:** Repository templates let you mark a repo as a template. Others can then click "Use this template" to create new repos based on it, with the same directory structure, files, and initial code. This is cleaner than forking when you want fresh history. Great for creating project starters.

---

**Q19.** You notice GitHub shows a security warning about a vulnerable dependency in your repository. What should you do? ⭐⭐
- A) Ignore it; it's likely a false positive
- B) Review the alert details and update the vulnerable package to a patched version
- C) Make the repository private to hide the warning
- D) Immediately delete all code

**Answer:** B  
**Explanation:** Dependabot alerts (by GitHub's security scanner) are usually accurate. When you see a vulnerability: (1) Review the alert, (2) Understand what's vulnerable and the risk, (3) Update the package to a patched version, (4) Test thoroughly, (5) Commit and deploy. Ignoring security alerts is risky.

---

**Q20.** What permission levels can you assign to a collaborator on a private GitHub repository? ⭐⭐
- A) Only "admin" or "no access"
- B) Pull (read), Push (write), and Admin
- C) Across several levels including Read, Write, Admin, Maintain, and Triage
- D) Only one level: "collaborator"

**Answer:** C  
**Explanation:** GitHub offers granular permissions: Read (pull only), Triage (manage issues/PRs), Write (can push), Maintain (manage repo but not delete), Admin (full control). This allows principle of least privilege. Exact role names vary (the above are common in 2024+).

---

## Section 3: Git Fundamentals & Workflows (10 Questions)

**Q21.** What is a merge conflict in Git? ⭐
- A) A conflict between two repositories
- B) When Git cannot automatically combine changes from different branches because the same lines were modified differently
- C) A permission error
- D) When you try to push without having latest changes

**Answer:** B  
**Explanation:** Merge conflicts occur when two commits modify the same lines differently. Git can't automatically determine which version is correct. You must manually resolve conflicts by choosing which changes to keep, then complete the merge. Conflicts are common in collaborative development.

---

**Q22.** You're working on a feature branch and want to incorporate the latest changes from main without creating a merge commit. What Git operation should you use? ⭐⭐
- A) `git merge main`
- B) `git rebase main`
- C) `git pull main`
- D) `git cherry-pick main`

**Answer:** B  
**Explanation:** `git rebase main` replays your commits on top of main, creating a linear history without a merge commit. `git merge main` creates a merge commit (preserves history). Rebase creates cleaner history but rewrites commits, so avoid on shared branches. Perfect for feature branches before PR.

---

**Q23.** What is the purpose of creating a feature branch instead of working directly on main? ⭐⭐
- A) Feature branches are faster
- B) Feature branches allow isolated development, regular testing, and clean commit history before merging to main
- C) Main branch can't be worked on
- D) It doesn't matter; main and feature branches are identical

**Answer:** B  
**Explanation:** Feature branches isolate work, allowing you to experiment without affecting main. Benefits: (1) Main stays stable, (2) Code review via PR, (3) Easy rollback if needed, (4) Multiple features develop in parallel. This is the standard professional workflow.

---

**Q24.** If you want to undo the last commit but keep the changes in your working directory, which command should you use? ⭐⭐
- A) `git revert HEAD`
- B) `git reset --soft HEAD~1`
- C) `git reset --hard HEAD~1`
- D) `git remove HEAD`

**Answer:** B  
**Explanation:** `git reset --soft HEAD~1` moves HEAD back one commit but keeps your changes staged and in the working directory. `--hard` would discard changes (destructive). `--soft` keeps changes for re-committing. `revert` creates a new undo commit instead of removing the original.

---

**Q25.** What is the difference between `git reset --soft`, `git reset --mixed`, and `git reset --hard`? ⭐⭐⭐
- A) They are identical; the flags don't matter
- B) --soft keeps changes staged; --mixed keeps changes unstaged; --hard discards changes
- C) --hard is the only real command; others are shortcuts
- D) They differ only in speed

**Answer:** B  
**Explanation:** `git reset --soft HEAD~1`: undo commit, keep changes staged. `--mixed` (default): undo commit, keep changes unstaged in working dir. `--hard`: undo commit, discard changes completely. Choose based on what you want to keep. Hard is destructive and should be used carefully.

---

**Q26.** You realize a commit introduced a bug and you want to create a new commit that undoes it, keeping all history visible. What command should you use? ⭐⭐
- A) `git reset <commit>`
- B) `git revert <commit>`
- C) `git undo <commit>`
- D) `git remove <commit>`

**Answer:** B  
**Explanation:** `git revert <commit>` creates a new commit that undoes the changes from the specified commit. It preserves all history—you can see both the original commit and the revert commit. This is safer than reset when the commit has been pushed to shared repos.

---

**Q27.** In a Git workflow, what does "squashing commits" mean? ⭐⭐
- A) Deleting old commits
- B) Combining multiple commits into a single commit
- C) Merging two branches
- D) Stashing work in progress

**Answer:** B  
**Explanation:** Squashing combines multiple commits into one. Useful for cleaning up messy development history before merging (e.g., 10 "work in progress" commits → 1 clean feature commit). GitHub's "Squash and merge" option does this automatically. Keeps main history clean.

---

**Q28.** What is a GitHub Flow workflow? ⭐
- A) A complex branching strategy for enterprise projects
- B) A simple workflow: main always deployable, create feature branches, PR for review, merge and deploy
- C) A way to manage Git conflicts
- D) A type of merge strategy

**Answer:** B  
**Explanation:** GitHub Flow is simple: (1) main is always stable/deployable, (2) create descriptive feature branches, (3) work on branch and commit regularly, (4) open PR for review, (5) merge after approval, (6) deploy. Great for continuous deployment. Simpler than Git Flow for most teams.

---

**Q29.** When working with multiple remote repositories, what does "origin" typically refer to? ⭐
- A) The first repository ever created
- B) The primary remote repository (usually your GitHub repo)
- C) Your local repository
- D) The repository owner

**Answer:** B  
**Explanation:** "origin" is the default remote name for the primary repository URL. When you clone, origin is automatically set to the clone source. You can add other remotes (e.g., "upstream" for original repo). Use `git remote -v` to see all configured remotes.

---

**Q30.** What does it mean when Git says "your branch is ahead by 3 commits"? ⭐
- A) Your local commits haven't been pushed to the remote yet
- B) Your remote repo has newer code than local
- C) There are conflicts between branches
- D) Three collaborators made commits

**Answer:** A  
**Explanation:** This message means your local branch has 3 commits not yet pushed to the remote. Fix by pushing: `git push origin <branch>`. Opposite message "behind 3 commits" means remote has changes not pulled locally. Understanding the relationship between local and remote is crucial for collaboration.

---

## Section 4: Collaboration Features (10 Questions)

**Q31.** What is the primary purpose of a Pull Request (PR) on GitHub? ⭐
- A) To request permission to access the repository
- B) To propose code changes and request review before merging into main
- C) To notify collaborators of a commit
- D) To create a backup of the code

**Answer:** B  
**Explanation:** A PR is a proposal to merge changes from one branch into another (usually feature branch → main). It enables code review, discussion, and ensures code quality. PRs are central to collaborative development, allowing teams to maintain standards and catch issues before merging.

---

**Q32.** You've created a pull request but reviewers have requested changes. What's the correct workflow? ⭐⭐
- A) Close the PR and create a new one with corrected code
- B) Make the requested changes, commit, and push to the same feature branch; the PR updates automatically
- C) Rebase and force-push
- D) Create a new PR with a note about the changes

**Answer:** B  
**Explanation:** When reviewers request changes, you make updates on the same feature branch and push. GitHub automatically updates the PR showing the new commits. Force-pushing (A) works but is not ideal on shared branches. Creating a new PR (D) is unnecessarily complicated. Just push to your branch.

---

**Q33.** What should an effective PR description include? ⭐⭐
- A) A detailed list of every line of code changed
- B) What changed, why it changed, any relevant issue numbers, testing notes, and screenshots (if applicable)
- C) Nothing; let the code speak for itself
- D) Only the commit message

**Answer:** B  
**Explanation:** Good PR descriptions explain context: what problem it solves, why this approach was chosen, links to related issues (fixes #123), testing approach, and visual evidence (screenshots/demos) if relevant. This helps reviewers understand intent and catch architectural issues, not just syntax.

---

**Q34.** As a code reviewer, you notice a potential issue in a PR. How should you communicate it? ⭐⭐
- A) Approve anyway; it's not critical
- B) Immediately request changes without explanation
- C) Leave a comment on the specific line explaining the issue, asking questions constructively, or suggesting improvements
- D) Message the author privately

**Answer:** C  
**Explanation:** Good code review etiquette: (1) Comment on specific code lines, (2) Ask clarifying questions, (3) Suggest improvements constructively, (4) Acknowledge what's good. Avoid approval-anyway or aggressive tone. GitHub's "Suggest changes" feature lets reviewers propose edits the author can apply with one click.

---

**Q35.** What does "required status checks" mean in a pull request? ⭐
- A) You must receive feedback from at least one person
- B) Automated tests/CI must pass before the PR can be merged
- C) The PR must exist for a minimum time period
- D) All comments must be resolved

**Answer:** B  
**Explanation:** Required status checks enforce that CI/CD pipelines (tests, linters, builds) must succeed before merging. Protects main from broken code. Configured via branch protection rules. A PR with failing status checks shows a ⚠️ and can't be merged until tests pass.

---

**Q36.** You want to link a GitHub Issue to a PR to automatically close the issue when the PR merges. What's the correct syntax? ⭐⭐
- A) "See issue 123"
- B) "fixes #123" or "closes #123" in the PR description
- C) "link to issue 123"
- D) Use the "Link" button in the UI only

**Answer:** B  
**Explanation:** Keywords like "fixes #123", "closes #123", "resolves #123" in a PR description automatically close the linked issue when the PR merges. GitHub recognizes these special keywords. Mentioning "#123" alone just links but doesn't auto-close. Very useful for workflow automation.

---

**Q37.** What is a GitHub Discussion? ⭐
- A) A type of bug report
- B) A conversational thread for Q&A, ideas, and announcements (different from issues which are task-focused)
- C) A pull request review conversation
- D) A commit message thread

**Answer:** B  
**Explanation:** Discussions are for open-ended conversations: questions, ideas, polls, announcements. Issues are for tracked tasks/bugs. Discussions feel more like a forum; issues feel like a task tracker. You can mark discussion answers, search, and filter by category. Great for community engagement.

---

**Q38.** You have multiple branches with active PRs. How do you manage notifications to avoid being overwhelmed? ⭐⭐
- A) Turn off all notifications
- B) Configure notification preferences: watch specific repos, customize email frequency, mute conversations when caught up
- C) Check GitHub manually several times daily
- D) Ask others not to notify you

**Answer:** B  
**Explanation:** GitHub settings → Notifications let you customize: (1) Which repos you watch, (2) Email vs. web notifications, (3) Include/exclude comments on unassigned items, (4) Digest frequency. Mute conversations with "Mute" button. Proper configuration keeps you informed without overwhelm.

---

**Q39.** When reviewing a PR, you notice it touches a critical system but wasn't assigned to you. What action should you take? ⭐⭐
- A) Approve quickly so the PR isn't delayed
- B) Change your review status to "Requesting changes" without reading the code
- C) Review carefully, leave feedback, and potentially request a domain expert review
- D) Ignore it; that's someone else's responsibility

**Answer:** C  
**Explanation:** Reviewing critical code is everyone's responsibility. Even if not assigned, if you notice critical changes: (1) Review thoroughly, (2) Provide detailed feedback, (3) Suggest involving domain experts, (4) Don't rubber-stamp. This maintains code quality and knowledge sharing. No one person should be sole reviewer of critical code.

---

**Q40.** What's the purpose of mentioning someone with @username in a GitHub conversation? ⭐
- A) To create a direct message
- B) To notify them and draw their attention to the conversation
- C) To share the conversation with everyone
- D) To give them administrative access

**Answer:** B  
**Explanation:** @mentioning notifies the specific person and adds them to the conversation. They receive notifications and the mention appears highlighted. Used to get specific expertise, answer questions, or request review. Essential for collaboration and ensuring important people see relevant conversations.

---

## Section 5: GitHub Products & Ecosystem (8 Questions)

**Q41.** What is GitHub Desktop used for? ⭐
- A) Hosting repositories in the cloud
- B) Managing issues and projects only
- C) A graphical Git client for those preferring GUI over command line for Git operations
- D) Backing up repositories automatically

**Answer:** C  
**Explanation:** GitHub Desktop is a GUI application that simplifies Git workflows for those uncomfortable with the command line. Allows committing, branching, merging, pulling, and pushing through a visual interface. Useful for beginners but power users typically prefer CLI for efficiency.

---

**Q42.** When should you use GitHub CLI (gh command) over the GitHub web interface? ⭐⭐
- A) GitHub CLI is no longer supported
- B) For automation, scripting, and workflows you want to run from the terminal without web browser
- C) Only on Fridays
- D) Never; web interface is always better

**Answer:** B  
**Explanation:** GitHub CLI is powerful for automation and scripting. Commands like `gh pr create`, `gh issue list`, `gh repo clone` run from terminal. Great for CI/CD, automation workflows, and power users who live in the terminal. Example: `gh pr create --title "My PR" --body "Description"` creates a PR from CLI.

---

**Q43.** You want to approve a pull request while on your mobile phone. What GitHub feature or app enables this? ⭐
- A) GitHub Desktop (available on phone)
- B) GitHub Mobile app (iOS/Android)
- C) Web browser only
- D) Not possible on mobile

**Answer:** B  
**Explanation:** GitHub Mobile app (iOS and Android) lets you review PRs, manage issues, view code, and leave comments on the go. It doesn't support full code editing but great for reviews and management. Modern development requires review capability anywhere.

---

**Q44.** What are webhooks in the context of GitHub? ⭐⭐
- A) A type of branch protection rule
- B) Automated notifications that trigger external actions when GitHub events occur (push, PR, issue)
- C) A method to backup repositories
- D) A type of commit hook

**Answer:** B  
**Explanation:** Webhooks send HTTP POST payloads to a specified URL when events occur (push, PR opened, issue created, etc.). Used to integrate GitHub with external systems: deployment tools, Slack notifications, CI/CD platforms, jira, etc. Powerful for automation and integration.

---

**Q45.** You want to add your GitHub repository to your Slack team so members get notifications about pushes and PRs. This is an example of what? ⭐
- A) A branch protection rule
- B) A GitHub Action
- C) A GitHub integration/webhook with Slack
- D) A repository secret

**Answer:** C  
**Explanation:** Installing GitHub app in Slack (or using webhooks) creates an integration that sends GitHub notifications to Slack channels. This is an example of GitHub ecosystem integration. Every time someone pushes, opens PR, or creates issue, Slack gets notified. Keeps team informed without leaving Slack.

---

**Q46.** What's the difference between GitHub Apps and OAuth applications? ⭐⭐
- A) They are identical
- B) GitHub Apps are newer, more secure (granular permissions, no personal token), can act independently; OAuth apps are older, less secure
- C) GitHub Apps are for GitHub only; OAuth apps work everywhere
- D) OAuth is better

**Answer:** B  
**Explanation:** GitHub Apps (newer) > OAuth apps (older) for security and features. Apps have: (1) Granular permissions per repository, (2) More secure (no shared personal token), (3) Can take actions independently, (4) Server account separate from user. For new integrations, prefer GitHub Apps.

---

**Q47.** Describe what GitHub Marketplace is and what you can find there. ⭐
- A) Where you buy GitHub subscriptions
- B) Where you download GitHub
- C) A platform where developers publish and discover GitHub Apps, Actions, and integrations for workflows
- D) Where teams hire developers

**Answer:** C  
**Explanation:** GitHub Marketplace lists verified Apps and Actions that extend GitHub functionality. Browse by category (CI/CD, project management, code quality, deployment, etc.), read reviews, install directly to your account/org. Great way to discover community tools and solutions. First place to check before building custom integration.

---

**Q48.** You want to automate running tests every time code is pushed. Which GitHub feature would you use? ⭐⭐
- A) Webhooks only
- B) GitHub Actions (workflow automation platform) to create CI/CD pipelines
- C) Branch protection rules
- D) Repository secrets

**Answer:** B  
**Explanation:** GitHub Actions is the native workflow automation platform. Create `.github/workflows/test.yml` to run tests on push. More powerful than webhooks for CI/CD. Can run linting, tests, builds, deployments, notifications—all defined as code. Excellent and free for public repos, has limits on private.

---

## Section 6: Project Management (10 Questions)

**Q49.** What are labels in GitHub Issues used for? ⭐
- A) Blocking other contributors
- B) To categorize and organize issues (bug, feature, help wanted, good first issue, documentation, etc.)
- C) To force closure of issues
- D) To encrypt issue contents

**Answer:** B  
**Explanation:** Labels are tags for organizing issues. Common labels: "bug" (problems), "feature" (requests), "help wanted" (need assistance), "good first issue" (for newcomers), "documentation", "critical". You can create custom labels. Labels enable filtering and quick understanding of issue type and priority. Essential for managing large projects.

---

**Q50.** What is a milestone in GitHub? ⭐
- A) A label for bugs
- B) A target version/release or deadline that groups related issues and PRs for planning
- C) A type of branch
- D) A commit message

**Answer:** B  
**Explanation:** Milestones group issues/PRs by release version or deadline (v1.0.0, Sprint 3, Q1 Release). Helps plan and track progress toward goals. Set due dates. See progress bar showing completion percentage. Useful for release management and sprint planning. Each issue/PR can belong to one milestone.

---

**Q51.** You want to prevent accidental merge of a PR into main before a specific task is completed. How would you manage this? ⭐⭐
- A) Have everyone agree verbally not to merge
- B) Create an issue and link it, but you can't technically prevent merge
- C) Create a "Draft" PR (marked as not ready) or use auto-linking (fixes #456 blocks merge until #456 is closed)
- D) Delete the main branch

**Answer:** C  
**Explanation:** Mark PR as "Draft" (top-right toggle) to show it's not ready for review/merge. For blocking until another issue is done: create that issue, link it with "fixes/closes #456" in PR. PR will show as blocked until linked issue is closed. Or use branch protection with required reviewers who enforce this discipline.

---

**Q52.** What is the purpose of GitHub Projects? ⭐⭐
- A) To back up code
- B) To create visual task boards/roadmaps for managing issues and PRs (Kanban or table view)
- C) To store project files only
- D) To host the main branch

**Answer:** B  
**Explanation:** GitHub Projects provides project management tools: Kanban boards (To Do → In Progress → Done) or table views (like spreadsheets). Link issues/PRs to projects. Automation: new issues auto-add, movement rules auto-update status. Replaces external tools like Jira/Trello if you want GitHub-native project management.

---

**Q53.** How can you automate moving issues across project columns? ⭐⭐
- A) Manually drag each issue
- B) Use project automation rules (e.g., auto-move to "In Progress" when PR created, auto-move to "Done" when issue closed)
- C) Create custom GitHub Actions
- D) Not possible; must be manual

**Answer:** B  
**Explanation:** GitHub Projects has built-in automation: "When issues are opened, add to project", "When PR opened, move to In Progress", "When issue closed, move to Done". These reduce manual overhead. You configure automation rules in project settings. Combines with issues/PRs linking for streamlined workflow.

---

**Q54.** What are semantic version numbers, and how do they work? ⭐⭐
- A) Version numbers with no pattern
- B) MAJOR.MINOR.PATCH (e.g., 1.2.3): MAJOR = incompatible changes, MINOR = backward-compatible features, PATCH = backward-compatible fixes
- C) Date-based version numbers
- D) Random numbers assigned by GitHub

**Answer:** B  
**Explanation:** Semantic Versioning: Given a version MAJOR.MINOR.PATCH, increment: MAJOR for incompatible API changes (1.0.0 → 2.0.0), MINOR for new features backward-compatible (1.2.0 → 1.3.0), PATCH for bug fixes (1.2.0 → 1.2.1). Users understand impact at a glance. Industry standard practice.

---

**Q55.** How do you create a release in GitHub? ⭐
- A) Automatically created when you push to main
- B) Create a Git tag and publish it as a GitHub Release with notes and optional assets/binaries
- C) Special button in organizations only
- D) Requires GitHub Actions webhook

**Answer:** B  
**Explanation:** Create a release: (1) Create a Git tag (`git tag v1.0.0`), (2) Push tag (`git push origin v1.0.0`), or use GitHub UI: Go to Releases → "Create a new release", select tag, add release notes, optionally attach binaries/artifacts. Releases are searchable, notable milestones tracked in project history.

---

**Q56.** What should be included in release notes? ⭐
- A) Technical implementation details and code snippets
- B) Summary of changes (new features, bug fixes, breaking changes), upgrade instructions, known issues, contributors
- C) Nothing; let the commits speak
- D) Jokes and irrelevant content

**Answer:** B  
**Explanation:** Good release notes: (1) Summarize what's new/fixed/changed, (2) Highlight breaking changes prominently, (3) Provide upgrade instructions, (4) Acknowledge contributors, (5) List known issues if any. Users shouldn't have to read commit history to understand what changed. Clear release notes build trust.

---

**Q57.** You're managing a large project with many contributors. What's the best practice for tracking who's working on what? ⭐⭐
- A) Rely on commit messages alone
- B) Assign issues/PRs to specific team members, use labels (assignee, priority), link related work, maintain a README of responsibilities
- C) Assume contributors will communicate
- D) Hire a project manager outside GitHub

**Answer:** B  
**Explanation:** Best practices: (1) Assign each issue to a responsible party, (2) Use labels for priority/type, (3) Link related work, (4) Use project boards for overview, (5) Maintain CONTRIBUTING guidelines. Clear ownership reduces confusion, duplicate work, and communication gaps. GitHub provides all these tools.

---

**Q58.** How do you efficiently filter issues in a GitHub repository? ⭐
- A) Read all issues one by one
- B) Use filters: `is:issue is:open label:bug assignee:username`, create saved searches
- C) Export to spreadsheet
- D) Not possible; GitHub has no filtering

**Answer:** B  
**Explanation:** GitHub has powerful search/filter syntax: `is:open is:issue label:bug assignee:me`. Filters work on issues, PRs, discussions. You can save filter URLs for quick access. Combine multiple filters: `sort:created-desc is:open label:"good first issue"`. Saves time when managing dozens/hundreds of issues.

---

## Section 7: Authentication & Security (10 Questions)

**Q59.** What is a Personal Access Token (PAT) and when should you use it? ⭐⭐
- A) A temporary password for web login
- B) A secret token with scoped permissions for CLI, Git, API access instead of using your password
- C) A public identifier for your account
- D) Required only for GitHub Enterprise

**Answer:** B  
**Explanation:** PAT is a secret token with specific permissions ("scopes"). Use for: (1) CLI/API authentication instead of passwords (more secure), (2) Deploy scripts, (3) GitHub Actions (secrets). Never commit PATs to code. Treat like passwords. Has expiration date. Create in Settings → Developer settings → Personal access tokens. Better than passwords for programmatic access.

---

**Q60.** How do you set up SSH authentication for GitHub? ⭐⭐
- A) Use your password; SSH is optional
- B) Generate SSH key pair (`ssh-keygen -t ed25519`), add public key to GitHub account, configure Git to use SSH URL
- C) SSH requires special setup and is only for advanced users
- D) SSH is deprecated

**Answer:** B  
**Explanation:** SSH setup: (1) `ssh-keygen -t ed25519` (generates id_ed25519 + id_ed25519.pub), (2) Add public key to GitHub (Settings → SSH keys), (3) Use `git@github.com:user/repo.git` URLs instead of HTTPS, (4) Test: `ssh -T git@github.com`. No password needed for Git ops. Very secure and convenient for frequent commits.

---

**Q61.** What is Two-Factor Authentication (2FA) and why is it important? ⭐
- A) Two passwords for double security
- B) A second verification step (authenticator app or SMS) required after password entry to access account; protects against password compromise
- C) Only necessary for administrators
- D) Optional security feature with no real benefit

**Answer:** B  
**Explanation:** 2FA requires something you know (password) + something you have (authenticator app like Google Authenticator, Authy, or SMS code). Prevents account takeover even if password leaked. If someone has your password, they still can't access without your device. Highly recommended for all accounts, mandatory for critical accounts.

---

**Q62.** Where do you store secrets (passwords, API keys, tokens) in a GitHub Actions workflow? ⭐⭐
- A) Hardcoded in the workflow file
- B) In GitHub Secrets (Settings → Secrets and variables → Repository secrets); referenced as `${{ secrets.SECRET_NAME }}`
- C) In .env files committed to repo
- D) In workflow file comments

**Answer:** B  
**Explanation:** GitHub Secrets safely store sensitive data. Create in Settings → Secrets, reference in workflows as `${{ secrets.DATABASE_PASSWORD }}`. Secrets are masked in logs. Best practice: create environment-specific secrets (dev, staging, prod). Never hardcode secrets in code or config files.

---

**Q63.** You accidentally committed a sensitive API key to a public repository. What's the immediate action? ⭐⭐⭐
- A) Just delete the file in the next commit
- B) Immediately: (1) Change repo to private, (2) Rotate/invalidate the exposed API key, (3) Remove from Git history using `git-filter-branch` or BFG, (4) Force push
- C) Commit a "fix" removing the key
- D) Ignore it; nobody will find it

**Answer:** B  
**Explanation:** Exposed secrets are critical even if deleted from current code because they're in history. Action plan: (1) Rotate credentials immediately (the exposed ones are compromised), (2) Make repo private, (3) Use tools to remove from history, (4) Force push. GitHub automatically alerts you if it detects secrets in public repos. Old commits' files are still accessible via history!

---

**Q64.** What is the difference between HTTPS and SSH for Git authentication? ⭐⭐
- A) HTTPS is more secure
- B) HTTPS uses password/PAT; SSH uses cryptographic keys. SSH more convenient (no repeated auth), HTTPS more flexible (works everywhere). Both secure if keys/tokens kept safe
- C) SSH is only for Linux
- D) They're identical

**Answer:** B  
**Explanation:** HTTPS: Use password or PAT with `https://github.com/user/repo.git`. SSH: Use key pair with `git@github.com:user/repo.git`. Trade-offs: HTTPS easier setup/ubiquitous (proxy-friendly), SSH more convenient (no password each push), both secure. Most developers prefer SSH for local development.

---

**Q65.** What is the difference between a public SSH key and a private SSH key? ⭐
- A) They are the same thing
- B) Public key goes on GitHub; private key stays on your computer. Others use public to verify your identity; you prove it with private
- C) Private key is for GitHub; public is for your computer
- D) Both go on GitHub

**Answer:** B  
**Explanation:** SSH uses Public Key Cryptography: Public key (shareable) goes on GitHub; Private key (secret) stays on your machine. When you push, Git uses private key to prove you're authorized. Server verifies using public key. Never share private key. Permissions: `chmod 600 ~/.ssh/id_ed25519`.

---

**Q66.** When should you rotate your Personal Access Tokens and SSH keys? ⭐⭐
- A) Never; they're permanent
- B) Regularly (every 90 days recommended), immediately after exposure, or when team members leave
- C) Only when you forget them
- D) GitHub requires rotation every 10 days

**Answer:** B  
**Explanation:** Security best practice: rotate credentials regularly (quarterly) and immediately if compromised or when access should be revoked (departing team member). Most security standards recommend 90-day rotation. GitHub allows token expiration configuration. Balance convenience vs. security.

---

**Q67.** What's the purpose of the GitHub Security audit log (for organizations)? ⭐⭐
- A) Only logs code changes
- B) Records all administrative actions (user added, settings changed, repos transferred) for compliance and security monitoring
- C) Only for GitHub Enterprise
- D) Logs commit messages

**Answer:** B  
**Explanation:** Audit Log (Settings → Audit log) provides immutable record of: who accessed what, when members were added/removed, permission changes, secret access. Essential for security monitoring, compliance (SOC 2, HIPAA), incident investigation. Shows complete admin action history. GitHub Enterprise has more comprehensive audit logging.

---

## Section 8: Privacy & Permissions (10 Questions)

**Q68.** What are the three main visibility levels for GitHub repositories? ⭐
- A) Draft, Public, Private
- B) Public (visible to all), Private (restricted), Internal (org members only)
- C) Open, Closed, Hidden
- D) Only Public and Private

**Answer:** B  
**Explanation:** Public: Anyone can see and clone. Private: Only invited users can access. Internal (Enterprise): Only organization members can access. Choose visibility based on content sensitivity. Most open-source is public; commercial/proprietary is private. Some enterprises use internal for cross-team sharing.

---

**Q69.** You need to grant a contractor access to specific repositories for 3 months, then revoke automatically. What's the best approach? ⭐⭐
- A) Make them a full organization member
- B) Add them as an outside collaborator with specific repo access and a reminder to revoke when contract ends (or Enterprise: use time-based access rules)
- C) Create a shared account (bad practice)
- D) Give them your password

**Answer:** B  
**Explanation:** Use outside collaborator (Settings → Collaborators → Add collaborator) with specific repo access and clearly documented end date. Better yet (Enterprise): use SAML/OIDC with automatic provisioning/deprovisioning. Never share accounts or give permanent access. Document access grants and review quarterly.

---

**Q70.** What permission levels are available for repository collaborators, and what can each do? ⭐⭐
- A) Only "write" and "read"
- B) Read (pull only), Triage (manage issues), Write (push), Maintain (admin except delete), Admin (full control). Each role is a superset of lower
- C) Permissions are binary: on/off
- D) All collaborators get the same permissions

**Answer:** B  
**Explanation:** GitHub permission hierarchy (least to most): Read → Triage → Write → Maintain → Admin. Each level includes previous permissions plus more. Example: Triage can manage issues/PRs but not push code. Maintain can merge but not delete/transfer repo. Admin can do everything. Use principle of least privilege: grant minimum needed.

---

**Q71.** What is a branch protection rule and why would you use one? ⭐⭐
- A) A rule preventing certain users from using branches
- B) Rules that enforce code quality gates before merging (require reviews, status checks, up-to-date branches, etc.) to protect important branches like main
- C) A way to hide branches
- D) Automatically deletes branches over a certain age

**Answer:** B  
**Explanation:** Branch protection on "main": (1) Require PR reviews before merge, (2) Require status checks (tests) to pass, (3) Require updated branch before merge, (4) Dismiss stale reviews on new commits, (5) Require admin review, (6) Allow force push only by admins. Prevents accidental/bad code landing on main. Essential in team environments.

---

**Q72.** How do organization members get access to repositories in an organization? ⭐⭐
- A) Automatically when added to org
- B) Default permissions set at org level + repo-specific overrides. Org owner/admins manage both org-level permissions and per-repo access
- C) Only through personal invitations
- D) Adding one person grants everyone access

**Answer:** B  
**Explanation:** Org structure: Organization has base permission level for all repos (e.g., "read" by default). Then per-repo, you can override with more/less access. Example: New member added to org at "read" level, but elevated to "write" on specific repos. Settings > Member privileges > Base permissions controls default.

---

**Q73.** What are GitHub Secrets for organization and environment? ⭐⭐
- A) Passwords for secret channels
- B) Secure storage for sensitive data (API keys, credentials) scoped to org/environment, used in workflows and available only where scoped
- C) Private comments you make
- D) Broken feature, don't use

**Answer:** B  
**Explanation:** Organization secrets (visible to all org workflows in chosen repos) vs. environment secrets (scoped to specific environments like staging/production). Use in workflows: `${{ secrets.API_KEY }}`. Secrets are masked in logs, encrypted at rest. Best practice: minimize secret exposure; use environment-specific secrets.

---

**Q74.** A contractor left your company. What access should you immediately revoke? ⭐⭐
- A) Don't revoke anything; they signed a contract
- B) Remove from all organizations, revoke SSH keys access, remove outside collaborator status, rotate any shared credentials
- C) Just hope they forget their password
- D) Let admins handle it eventually

**Answer:** B  
**Explanation:** Immediate actions when someone leaves: (1) Remove from org/teams, (2) Remove from repos, (3) Revoke SSH keys (Settings → SSH keys → delete their key), (4) Rotate credentials (API keys, DB passwords), (5) Deactivate any personal access tokens they created, (6) Review audit log for suspicious activity. Don't delay.

---

**Q75.** What is the principle of least privilege, and why does it matter in GitHub? ⭐
- A) Give everyone maximum permissions "just in case"
- B) Grant only the minimum permissions needed for the job; regularly audit and remove unnecessary access
- C) Everyone should have same permissions
- D) Permissions are unimportant

**Answer:** B  
**Explanation:** Least privilege: New team member → Read role initially → "Write" role once trusted/trained → Only keep what's necessary. Reduces risk of accidental/malicious damage. Example: contractor only needs write access to 1 repo, not 10. Reduces blast radius if an account is compromised. Security best practice.

---

**Q76.** What happens when you make a GitHub repository private after it was public? ⭐⭐
- A) Nothing; people can still access
- B) People already accessing can no longer see it; forks remain but are now unreadable to others; existing clones on local machines still work but can't push/pull to remote
- C) Everything is deleted
- D) People retain their forked copies but can't pull updates

**Answer:** B  
**Explanation:** Making repo private immediately restricts access: Public viewers lose access. Existing forked copies remain but lose connection to original (origin becomes unreadable). Local clones still work if you have SSH access, but can't push/pull without credentials. People can see they forked it but not the content.

---

## Section 9: GitHub Administration (8 Questions)

**Q77.** What is a GitHub Organization and when should you create one? ⭐
- A) A collection of repositories for a single project
- B) A shared account with multiple members, centralized billing, and permission management; use for teams/companies with multiple projects/repos
- C) A type of GitHub Actions workflow
- D) Only for open-source projects

**Answer:** B  
**Explanation:** Organization = shared workspace for team/company managing multiple projects. Benefits: Centralized permissions, team management, single billing, auditing, branding. Create for: (1) Teams with multiple repos, (2) Companies needing shared workspace, (3) Open-source projects with multiple maintainers. Personal account for solo developers.

---

**Q78.** What are GitHub Teams within an organization, and how are they useful? ⭐⭐
- A) Different from users
- B) Groups of org members with specific permissions; useful for managing access at scale (Marketing team → access product repo, Backend team → infrastructure), roles, @mentions
- C) Always required
- D) Only for large organizations

**Answer:** B  
**Explanation:** Teams group members to simplify permission management. Examples: "Backend" team with write access to backend repos, "DevOps" with full infrastructure access, "Interns" with read-only access. Benefits: Assign permissions to team vs. individual >> add/remove team members to dynamically manage access. @mention team for PR reviews.

---

**Q79.** What is billing and which plan would you recommend for a small startup with 3 developers? ⭐⭐
- A) GitHub is always free
- B) Free: Public repos, basic features. Pro: Unlimited private repos, advanced features, $4/user/month. Team: $21/user/month. Choose based on: private repos needed, advanced security, collaboration features. Small startup: Pro or Team plan usually
- C) Only Enterprise for businesses
- D) Billing is for GitHub employees only

**Answer:** B  
**Explanation:** GitHub pricing tiers: Free (public repos only), Pro ($4/user/month), Team ($21/user/month), Enterprise (custom). Small startup with private repos → Pro or Team. Team adds better collaboration (protection rules, multiple org admins). Billing = Org → Settings → Billing. Good value for feature set vs. cost.

---

**Q80.** What does it mean to transfer a repository to another team member or organization? ⭐⭐
- A) Copy the repository
- B) Change ownership of repo; new owner/org becomes admin; original can lose access if not invited back; all issues, PRs, history preserved
- C) Delete and recreate
- D) Can't be done

**Answer:** B  
**Explanation:** Transfer repo: Settings → Danger zone → Transfer repository. Requires confirmation. New owner becomes admin; you lose admin unless invited in new org. All data (history, issues, PRs, notifications) transfers. Useful when handing projects to another team or moving to company org. Irreversible if you lose access!

---

**Q81.** How do you enforce organizational policies on GitHub? ⭐⭐⭐
- A) Hope people follow the rules
- B) Document in CONTRIBUTING.md, enforce via branch protection rules (require reviews, status checks), enable organization policies (required settings), require SAML (Enterprise)
- C) Can't enforce; trust only
- D) Hire enforcement staff

**Answer:** B  
**Explanation:** Enforcement mechanisms: (1) Documentation (CONTRIBUTING.md, CLA), (2) Technical enforcement (branch protection rules, required status checks, dismissible/required reviews), (3) Org-level policies (default permissions, disallow forking, require 2FA), (4) Enterprise: Managed users, data location, audit logging. Combination is most effective.

---

**Q82.** What is the GitHub Enterprise account and who needs it? ⭐
- A) Only for giant companies
- B) For organizations needing: advanced security, audit logging, managed users, SSO, dedicated support, on-premises option (GitHub Enterprise Server). Large orgs with compliance/security requirements
- C) Required for any organization
- D) Obsolete; GitHub one plan

**Answer:** B  
**Explanation:** Enterprise tier adds: Advanced Security (secret scanning, code scanning, dependency management), audit logs, SAML/OIDC/SCIM, IP allowlisting, managed users, dedicated support. Worth cost for: strict compliance needs, 500+ employees, regulated industries (healthcare, finance). Small teams don't need but may grow into it.

---

**Q83.** You notice suspicious activity in your organization's audit log (unauthorized access attempts). What action should you take? ⭐⭐
- A) Ignore it; probably nothing
- B) (1) Review audit log for scope, (2) Check forced password changes, (3) Review API access/tokens, (4) Rotate credentials of affected users, (5) Consider requiring 2FA, (6) Allow compromised users to rotate passwords, (7) Communication plan
- C) Delete the org
- D) Blame someone

**Answer:** B  
**Explanation:** When security incident detected: (1) Investigate scope (what was accessed?), (2) Force affected users to rotate passwords, (3) Revoke active sessions, (4) Rotate API keys/PATs, (5) Enable 2FA (if not already), (6) Review audit log further, (7) Communicate with affected parties, (8) Consider incident postmortem. Speed is critical to limit damage.

---

**Q84.** What is GitHub Dependabot and why is it important? ⭐
- A) A human team member's helper
- B) Automated dependency update tool. Opens PRs to update vulnerable/outdated dependencies; helps maintain security and compatibility
- C) Only for enterprise
- D) A deprecated feature

**Answer:** B  
**Explanation:** Dependabot: (1) Dependency scanning detects vulnerable packages, (2) Opens PRs with updates, (3) Can auto-merge safe updates, (4) Reports frequency (daily/weekly). Essential for supply chain security. Integrated into GitHub; enable in Settings → Code security & analysis → Dependabot. Catches security vulnerabilities early when they matter.

---

## Section 10: Modern Development Practices (8 Questions)

**Q85.** What is Continuous Integration (CI) and how does it benefit a team? ⭐
- A) Frequent drinking of coffee during development
- B) Automatically testing code changes as they're submitted; catches bugs early, maintains code quality, enables confident deployments
- C) A type of branch strategy
- D) Only for large projects

**Answer:** B  
**Explanation:** CI = automated testing on every commit/PR. Benefits: (1) Bugs caught immediately, (2) Reduced manual testing, (3) Confidence in deployments, (4) Faster development cycle, (5) Early quality issues = easier fixes. Implemented via GitHub Actions, Jenkins, CircleCI, etc. Run tests, linters, security scans automatically.

---

**Q86.** What is a GitHub Actions workflow and where do you define it? ⭐⭐
- A) A type of PR
- B) YAML file in `.github/workflows/` directory defining automated tasks triggered by events (push, PR, schedule, webhook). Specifies jobs, steps, runners
- C) Only available in Enterprise
- D) A commit message

**Answer:** B  
**Explanation:** Workflow example: `.github/workflows/test.yml` Contains: `on: [push, pull_request]` (trigger), `jobs: [test-suite]` (jobs to run), `steps: [checkout, install, test]` (sequential steps). Runs on GitHub runners or self-hosted. Executes in parallel if multiple jobs. Extremely flexible for any automation.

---

**Q87.** If a test suite fails in your CI pipeline, what should happen with the pull request? ⭐
- A) Automatically merge it anyway
- B) The PR shows as blocked/cannot merge; status check fails; reviewers see failure; author must fix and re-push
- C) Only the author sees the failure
- D) Tests are ignored

**Answer:** B  
**Explanation:** Branch protection with required status checks means: If tests fail → PR shows ❌ → cannot merge until fixed. This prevents broken code entering main. Author makes fixes, pushes, pipeline re-runs, eventually shows ✅ and PR can merge. Protects code quality and prevents regressions.

---

**Q88.** What are common code quality practices enforced in modern development? ⭐⭐
- A) Just write whatever you want
- B) Linting (style consistency), type checking, code reviews, automated tests, code coverage reporting, security scanning. Enforce via CI and branch protection
- C) Only for academics
- D) Optional and never enforced

**Answer:** B  
**Explanation:** Quality gates (CI): (1) Linters check style (Prettier, ESLint), (2) Type checkers (TypeScript, mypy), (3) Tests must pass + minimum coverage %, (4) Security scans flag vulnerabilities, (5) Code reviews catch logic issues. Multiple layers prevent low-quality code. Saves debugging time and maintenance burden long-term.

---

**Q89.** What is a deployment pipeline in the context of GitHub Actions? ⭐
- A) A water treatment system
- B) Sequence of automated stages: build → test → staging → production. Code automatically progresses through stages if all checks pass. Enables continuous deployment (CD)
- C) Manual process
- D) Only for enterprise

**Answer:** B  
**Explanation:** Deployment pipeline (CD): On PR merge → (1) Build artifacts, (2) Run tests, (3) Deploy to staging, (4) Automated tests on staging, (5) Manual approval or automatic deploy to production. GitHub Actions can orchestrate entire pipeline. Risk reduction through automated, repeatable process.

---

**Q90.** What is the purpose of a pre-commit hook in Git? ⭐
- A) To prevent commits
- B) Scripts that run locally before committing to catch issues early (formatting, linting, tests); prevent committing violating code to history
- C) To modify commit history
- D) Not useful

**Answer:** B  
**Explanation:** Pre-commit hook runs client-side before `git commit`. Common use: Format code (prettier), run lint (eslint), run unit tests. If hook fails, commit is blocked. Prevents committing code that violates project standards. Catches issues before they reach CI/remote. Configured in `.git/hooks/pre-commit` or tools like Husky.

---

**Q91.** Describe the difference between unit tests, integration tests, and end-to-end tests. ⭐⭐
- A) There's no difference
- B) Unit tests: test individual functions in isolation. Integration tests: test multiple components together. End-to-end tests: test entire user workflows. All run in CI
- C) Only unit tests matter
- D) Tests are unnecessary

**Answer:** B  
**Explanation:** Test pyramid: (1) Unit tests = fast, many (80%), test single function, (2) Integration tests = medium speed/count, test component interactions, (3) E2E tests = slow, few (5%), test user workflows. All automated in CI. Coverage = combination of all three. Each catches different issues.

---

**Q92.** What does "monitoring" mean in the context of deployed applications? ⭐
- A) Watching code commits
- B) Tracking application health in production: error rates, response times, user behavior, resource usage. Alerting on anomalies. Enables incident response
- C) Only for banks
- D) Not important

**Answer:** B  
**Explanation:** Production monitoring: (1) Application Performance Monitoring (APM) tracks response times, errors, (2) Observability = logs, metrics, traces, (3) Alerting = notification when thresholds exceeded, (4) Dashboards = real-time visibility. Tools: DataDog, New Relic, Prometheus. Enables rapid incident response and continuous improvement.

---

## Section 11: GitHub Community & Ecosystem (8 Questions)

**Q93.** What is the open source community contribution workflow? ⭐
- A) Directly push to projects you don't own
- B) (1) Find issue or identify feature, (2) Fork repo, (3) Clone fork, (4) Create feature branch, (5) Make changes + commit, (6) Push to fork, (7) Create PR to original repo, (8) Respond to feedback, (9) Merged by maintainers
- C) Only employees can contribute
- D) Contributions aren't welcomed

**Answer:** B  
**Explanation:** Open source workflow: Fork because you don't have write access → Clone your fork → Create branch → Edit → Commit → Push → PR. In PR, maintainers review. You might need to make changes, rebase, update. After approval, maintainer merges. Standard for all open source contributions. Cultural norm: enthusiastic collaboration.

---

**Q94.** What does "Good First Issue" label mean and who should tackle it? ⭐
- A) Issues only for new employees
- B) Issues identified as suitable for new contributors to the project; lower complexity, good for onboarding. Perfect for first-time open source contributors
- C) Bad issues
- D) Irrelevant label

**Answer:** B  
**Explanation:** "Good first issue" label = maintainers' way of welcoming newcomers. Characteristics: lower complexity, well-documented, mentorship offered. Perfect for: (1) Learning how to contribute, (2) Understanding project structure, (3) Building confidence. After a few good first issues, tackle harder problems. Many projects use this label intentionally for community building.

---

**Q95.** What is a Contributor License Agreement (CLA) and why do projects require them? ⭐
- A) A contract preventing contributions
- B) Agreement you sign confirming you have rights to your code and grant project license rights. Protects projects from IP lawsuits, clarifies rights. Many open source projects require before accepting PR
- C) Only for enterprise
- D) Outdated practice

**Answer:** B  
**Explanation:** CLA = contributor asserts ownership of code + grants project license to use it. Why: Protects against someone claiming you used their code without permission. Must sign once per contributor. Automated via bots (e.g., CLAssistant). Common in large projects (Linux, GitHub, Kubernetes). Small projects often skip.

---

**Q96.** What is GitHub Sponsors and how can it help open source maintainers? ⭐
- A) GitHub giving away free money
- B) Platform where users can financially support maintainers they rely on monthly or one-time. Maintainers set up profiles/tiers. Enables sustainable open source
- C) Only for celebrities
- D) Requires thousands of downloads

**Answer:** B  
**Explanation:** GitHub Sponsors: (1) Maintainers create sponsor profile in their repo, (2) Users sponsor monthly (like Patreon), (3) GitHub matches 100% for first year, (4) Transparent sponsor recognition. Helps fund maintenance, bug fixes, documentation. Growing model for open source sustainability. Users feel good supporting tools they use.

---

**Q97.** What resources does GitHub provide for learning about Git and GitHub? ⭐
- A) None; self-teaching only
- B) GitHub Skills (interactive courses), GitHub Docs, GitHub Learning Lab (legacy), community forums, GitHub Blog. Free, comprehensive resources
- C) Only paid courses
- D) Outdated documentation

**Answer:** B  
**Explanation:** GitHub Skills = interactive, hands-on learning (https://skills.github.com/) covering topics from intro to advanced workflows. GitHub Docs = comprehensive reference. GitHub Blog = feature announcements, best practices. Community Forum = ask questions. All free. Perfect starting point for beginners and experienced developers.

---

**Q98.** What does "GitHub Trending" show and how might you use it? ⭐
- A) Most starred repositories all-time
- B) Repositories gaining rapid attention/activity in recent days/weeks by language/topic. Useful for discovering new projects, staying current with ecosystem trends
- C) Only personal repositories
- D) Not useful

**Answer:** B  
**Explanation:** GitHub Trending (github.com/trending): Shows repos spiking in activity. Filter by language (Python, JavaScript, etc.) and time (daily, weekly, monthly). Great for: (1) Discovering new tools, (2) Understanding what's popular in your language, (3) Learning from successful projects, (4) Finding communities. Trends change rapidly; useful for staying current.

---

**Q99.** What is a GitHub Discussion and how does it differ from Issues? ⭐
- A) Identical to issues
- B) Discussions = conversational (Q&A, ideas, announcements). Issues = task-focused (bugs, feature requests). Discussions feel like forum; Issues like project tasks. You can convert discussion to issue if actionable
- C) Discussions are old; use issues instead
- D) Issues are better than discussions always

**Answer:** B  
**Explanation:** Discussions and Issues serve different purposes: Discussions for open-ended conversation, brainstorming, Q&A, announcements. Issues for tracked work items, bugs, features. Discussions can be marked as answered and converted to issues (e.g., good idea discussed → becomes feature request). Many projects use both strategically.

---

**Q100.** What is GitHub Gists and when would you use it? ⭐
- A) GitHub's only feature
- B) Lightweight way to share code snippets, config files, notes. Public or secret (not discoverable). No full repo, just files. Great for sharing quick examples, troubleshooting
- C) Deprecated
- D) Only for small files

**Answer:** B  
**Explanation:** Gists (gist.github.com): Create public snippets you can share via URL or secret ones (unlisted). Useful for: (1) Share debugging scripts, (2) Config templates, (3) Code examples, (4) Quick notes with versioning. Less overhead than full repos. Can embed in blogs, create forks. Lightweight but version-controlled.

---

## Section 12: Common Exam Scenarios & Complex Questions (12 Questions)

**Q101.** You're leading a team starting an open source project. Walk through your Git and GitHub setup from scratch. ⭐⭐⭐
- A) Just create a repo and start coding
- B) (1) Create GitHub org for team, (2) Create public repo with meaningful name, (3) Add README explaining project, (4) Add LICENSE file (MIT/Apache), (5) Add CONTRIBUTING.md, (6) Set up branch protection on main, (7) Configure with Code of Conduct, (8) Outline issue templates, (9) Tag first release, (10) Announce
- C) Copy an existing project
- D) Professional setup not needed for open source

**Answer:** B  
**Explanation:** Professional open source setup includes: (1) Org for collaborative governance, (2) Documentation (README, CONTRIBUTING guides expectations), (3) Clear LICENSE (defines usage rights), (4) Code of Conduct (community safety), (5) Issue/PR templates (consistency), (6) Branch protection (quality gates), (7) Release strategy (semantic versioning), (8) Announcement (visibility). Takes effort upfront but attracts contributors.

---

**Q102.** During code review, you notice a PR modifies database schema without a migration script. The PR has 50 commits. How do you handle this? ⭐⭐⭐
- A) Approve it; too late now
- B) (1) Request changes with clear explanation, (2) Ask author to add migration script, (3) Explain why it's necessary (data integrity, rollback capability), (4) Suggest squashing commits to clean history if messy, (5) Don't merge until fixed. Communication is key
- C) Approve anyway
- D) Reject without explanation

**Answer:** B  
**Explanation:** Code review responsibility: Catch architectural issues (like missing migrations) before merge. Request changes constructively: explain why migrations matter (irreversible DB changes, rollback safety, team reproducibility). Number of commits doesn't matter if code is good, but suggest squashing for cleaner history. Be helpful; author is learning too.

---

**Q103.** Your project has reached v2.0.0 and it's a breaking change (API incompatible with v1.x). How do you communicate this to users? ⭐⭐
- A) Don't mention it; let users figure it out
- B) (1) Detailed release notes explaining breaking changes, (2) Migration guide (v1 → v2), (3) Link to documentation, (4) Deprecation period beforehand (if possible), (5) Bump MAJOR version (semantic versioning), (6) Announce via blog/alerts
- C) Keep it quiet
- D) Blame users for not updating

**Answer:** B  
**Explanation:** Breaking changes require clear communication: (1) Lead with "⚠️ BREAKING CHANGES" in release notes, (2) Explain what broke and why, (3) Provide migration guide (before/after examples), (4) Link to updated docs, (5) Increase MAJOR version per semver. Users appreciate transparency; lack of it breeds distrust. Plan deprecation periods for large breaking changes.

---

**Q104.** A security vulnerability is discovered in a dependency your project uses. It's critical but requires an update that might break compatibility. What do you do? ⭐⭐⭐
- A) Ignore it; users' problem
- B) (1) Assess risk (exploitability, exposure), (2) Emergency patch with updated dependency even if breaking, (3) Release as hotfix version, (4) Communication: explain vulnerability + recommend immediate update, (5) Provide migration guide if breaking, (6) Consider extended support for previous version if major projects affected
- C) Don't tell anyone
- D) Update slowly over months

**Answer:** B  
**Explanation:** Security vulnerabilities are severe and time-sensitive. Action: 1) Urgent fix, prioritize over roadmap, 2) Release immediately as hotfix (usually patch or minor version), 3) Transparency: explain vulnerability extent, 4) Provide migration guide if breaking, 5) Deploy monitoring for usage on vulnerable versions, 6) Community communication critical. Speed matters; users understand emergency releases.

---

**Q105.** You're onboarding a new team member on your GitHub-based project. What explicit steps would you take to get them productive quickly? ⭐⭐
- A) Send them the GitHub repo link; they'll figure it out
- B) (1) Add to org/teams with appropriate permissions, (2) Set up local: Git install, SSH keys, clone repo, (3) Install dependencies per README, (4) Create first branch for tiny task (README fix), (5) Walk through PR process (commit → push → PR → review → merge), (6) Pair program on first real task, (7) Provide CONTRIBUTING.md, (8) Document development environment setup, (9) Invite to Slack/communication, (10) Assign "good first issue"
- C) Have them read all documentation
- D) Onboarding is unnecessary

**Answer:** B  
**Explanation:** Effective onboarding is investment in team productivity: (1) Permissions/access setup, (2) Local environment working (common pain point), (3) First contribution small and guided, (4) Process walkthrough (how do we work here?), (5) Pair programming builds confidence, (6) Documentation helps future team members. New hires productive faster = better retention and fewer mistakes.

---

**Q106.** You discover that someone accidentally pushed 500 MB of video files to your private repo. They've been committing for the past month. How do you fix this? ⭐⭐⭐
- A) Delete the files; problem solved
- B) (1) Immediate investigation: who, what, why?, (2) Remove files from current code, (3) Use BFG Repo-Cleaner or git-filter-branch to remove from all history, (4) Force push to rewrite history (risky; coordinate with team), (5) Configure .gitignore to prevent recurrence, (6) Educate team about large file handling (use Git LFS if necessary), (7) Warning: force push requires everyone to re-clone
- C) Leave it; too late now
- D) Archive the repo

**Answer:** B  
**Explanation:** Large files in Git history bloat repo forever; fetches slow down. Action: (1) Identify what to remove, (2) Use BFG/filter-branch to strip from history, (3) Force push (⚠️ requires team coordination), (4) Everyone re-clones. Prevention: .gitignore prohibits large files, Git LFS for media, pre-commit hooks reject large commits. Educational moment for team on best practices.

---

**Q107.** Your organization is growing and you need to structure GitHub with multiple teams and repositories. Outline your access model. ⭐⭐
- A) Everyone gets admin access
- B) (1) Define teams by function (Frontend, Backend, DevOps, QA), (2) Repos by concern (api-server, ui, infrastructure), (3) Base permissions: New members = Read, (4) Promote as trust built, (5) Per-repo: Frontend team → Write on ui repos, (6) DevOps → Admin on infrastructure, (7) Cross-functional = PR review requirement, (8) Audit regularly; remove excess access, (9) onboarding playbook documents process
- C) No structure; ad hoc access
- D) One person controls everything

**Answer:** B  
**Explanation:** Scaling access: Needs structure for security and sanity. (1) Org teams mirror organization structure, (2) Repo structure mirrors technical boundaries, (3) Principle of least privilege: everyone starts with minimal, escalate as needed, (4) Regular audits: who has what access and why?, (5) Offboarding checklist: remove person from all access, (6) Documentation: team structure, access rationale, process. This reduces errors and security exposure.

---

**Q108.** You're in a situation where two developers made incompatible changes to the same file and there's a merge conflict. Explain the resolution process. ⭐⭐
- A) Delete one person's changes
- B) (1) Pull latest main, (2) Git shows conflict markers (<<<<, ====, >>>>) in file, (3) Open file, manually choose which changes to keep or combine both, (4) Remove markers, (5) Test changes work, (6) `git add <file>`, (7) `git commit -m "Resolve conflict"`, (8) Push and PR updates, (9) Review to ensure logical correctness, (10) Merge once resolved
- C) Start over
- D) Blame the other developer

**Answer:** B  
**Explanation:** Conflict resolution requires understanding both perspectives: (1) Understand what each change wanted to achieve, (2) Decide if both can coexist or choose one, (3) Manually edit to optimal solution, (4) Test thoroughly (conflicts often hide subtle issues), (5) Communication with other developer if unclear intent, (6) Complete merge cycle. Conflicts are common; resolving them well is crucial skill in team development.

---

**Q109.** Your CI/CD pipeline fails on a PR but you believe the test is flaky (inconsistent failures). What's the best approach? ⭐⭐
- A) Ignore the failure; merge anyway
- B) (1) Investigate: run test locally multiple times to confirm flakiness, (2) If flaky: fix test to be deterministic (remove timing dependencies, randomness), (3) Isolate flaky test, consider skipping temporarily while fixed, (4) Add logging to understand failure patterns, (5) Never ignore test failures; fix the test not the code, (6) Once fixed, re-run PR checks
- C) Always trust your code over tests
- D) Delete the flaky test

**Answer:** B  
**Explanation:** Flaky tests damage CI credibility (developers ignore failures). Action: (1) Investigate thoroughly, (2) Understand root cause (timing? randomness? external dependency?), (3) Fix the test to be deterministic, (4) Add better logging, (5) Consider isolation/mocking external systems, (6) Quarantine flaky test while fixing. Never skip test failures; address root cause. Reliable tests = reliable pipeline = team confidence.

---

**Q110.** You're publishing a critical security vulnerability in your library. You've already released a patched version. What's your disclosure strategy? ⭐⭐⭐
- A) Post on social media immediately
- B) (1) Responsible disclosure: notify users/maintainers privately if enterprise relationships, (2) Publish when patch is available to minimize exposure window, (3) Full transparency: describe vulnerability, impact, fix, (4) High visibility: security advisory in repo README, release notes, email, (5) Provide all versions affected, upgrade path, (6) Acknowledge if possible reporters, (7) Post-incident: review how it slipped through, prevent future
- C) Hide it
- D) Only tell trusted users

**Answer:** B  
**Explanation:** Responsible disclosure balances transparency and harm prevention: (1) Coordinate with maintainers; don't blindside, (2) Fix before public notice (if possible), (3) Announce when patch available so users can upgrade immediately, (4) Clear communication: severity, impact, fix instructions, (5) High visibility so users don't miss, (6) Post-incident review prevents similar issues, (7) Build trust through transparency. Ignoring or delaying creates bigger problems.

---

**Q111.** Design a GitHub workflow for a team with varying skill levels (juniors and seniors) that maintains code quality while unblocking progress. ⭐⭐⭐
- A) No process; everyone does their own thing
- B) (1) **Branch strategy**: Feature branch per task, main always deployable, (2) **PR process**: All code reviewed, but juniors reviewed by seniors (knowledge transfer), (3) **Size limits**: Smaller PRs merge faster; encourage PR size guidelines, (4) **Automation**: Tests + linters run automatically; no "manual testing", (5) **Standards**: Coding standards in linter enforcement not oral tradition, (6) **Pairing**: Seniors pair with juniors on complex tasks, (7) **Mentorship**: Code comments teach not criticize, (8) **Gradual autonomy**: Juniors start with "good first issues", escalate complexity as skills grow
- C) Seniors approve everything
- D) No quality control

**Answer:** B  
**Explanation:** Good team workflow scales: (1) Clear process applies to everyone fairly, (2) Automation enforces standards reliably, (3) Human review focuses on logic/design not style, (4) Pairing transfers knowledge efficiently, (5) Smaller PRs keep review cognitive load low, (6) "Good first issue" pathway builds confidence, (7) Growth planning: gradually increase responsibility. This unblocks juniors (they're productive) while maintaining quality (seniors guide). Team scales without becoming bottleneck.

---

**Q112.** You're evaluating whether to use Monorepo (single repo with multiple projects) vs. multiple separate repositories. What factors matter? ⭐⭐
- A) Doesn't matter; pick randomly
- B) **Monorepo advantages**: Shared dependencies, coordinated changes (related projects together), easier refactoring. **Disadvantages**: Slower operations, complex access control (can't grant per-project easily), all infrastructure for one repo, less modularity. **Multiple repos**: Fast, modular, independent deployment, granular access. **Disadvantage**: Harder coordinated changes, dependency hell, duplication. Choose based: (1) How coupled are projects? (2) How often coordinated changes? (3) Team size? (4) DevOps maturity?
- C) Always use monorepo
- D) Always use multiple repos

**Answer:** B  
**Explanation:** Repo structure is architectural decision: **Monorepo** suits: tightly coupled code (e.g., web app + API where they always sync), single team, shared infrastructure. **Multiple repos** suit: independent projects (library vs. app), independent teams, different deployment cycles, open source (community contributions). Many companies start multiple repos, evolve to monorepo. Google/Facebook use monorepo; others prefer separation. No universal answer; evaluate your needs/constraints actually deciding.

---

---

## Answer Key Summary

| Q | Answer | Difficulty | Domain |
|---|--------|-----------|--------|
| 1 | B | ⭐ | Git Fundamentals |
| 2 | B | ⭐ | Git Basics |
| 3 | B | ⭐⭐ | Commits |
| 4 | B | ⭐ | Branches |
| 5 | B | ⭐⭐ | Git Operations |
| 6 | C | ⭐⭐ | Staging |
| 7 | B | ⭐ | .gitignore |
| 8 | B | ⭐⭐ | Fetch vs Pull |
| 9 | B | ⭐⭐ | Commits |
| 10 | A | ⭐⭐ | Git Log |
| 11 | B | ⭐⭐ | Repository Setup |
| 12 | B | ⭐ | README |
| 13 | C | ⭐⭐ | Collaborators |
| 14 | B | ⭐ | Forking |
| 15 | B | ⭐⭐⭐ | Security |
| 16 | A | ⭐⭐ | Clone vs Fork |
| 17 | B | ⭐ | Visibility |
| 18 | B | ⭐⭐ | Templates |
| 19 | B | ⭐⭐ | Dependencies |
| 20 | C | ⭐⭐ | Permissions |
| 21 | B | ⭐ | Merge Conflicts |
| 22 | B | ⭐⭐ | Rebase |
| 23 | B | ⭐⭐ | Feature Branches |
| 24 | B | ⭐⭐ | Undo Commit |
| 25 | B | ⭐⭐⭐ | Git Reset |
| 26 | B | ⭐⭐ | Revert |
| 27 | B | ⭐⭐ | Squashing |
| 28 | B | ⭐ | GitHub Flow |
| 29 | B | ⭐ | Origin |
| 30 | A | ⭐ | Branch Status |
| 31 | B | ⭐ | Pull Requests |
| 32 | B | ⭐⭐ | PR Updates |
| 33 | B | ⭐⭐ | PR Description |
| 34 | C | ⭐⭐ | Code Review |
| 35 | B | ⭐ | Status Checks |
| 36 | B | ⭐⭐ | Issue Linking |
| 37 | B | ⭐ | Discussions |
| 38 | B | ⭐⭐ | Notifications |
| 39 | C | ⭐⭐ | Code Review |
| 40 | B | ⭐ | Mentions |
| 41 | C | ⭐ | GitHub Desktop |
| 42 | B | ⭐⭐ | GitHub CLI |
| 43 | B | ⭐ | GitHub Mobile |
| 44 | B | ⭐⭐ | Webhooks |
| 45 | C | ⭐ | Integrations |
| 46 | B | ⭐⭐ | Apps vs OAuth |
| 47 | C | ⭐ | Marketplace |
| 48 | B | ⭐⭐ | GitHub Actions |
| 49 | B | ⭐ | Labels |
| 50 | B | ⭐ | Milestones |
| 51 | C | ⭐⭐ | Draft PRs |
| 52 | B | ⭐⭐ | Projects |
| 53 | B | ⭐⭐ | Automation |
| 54 | B | ⭐⭐ | Semantic Versioning |
| 55 | B | ⭐ | Releases |
| 56 | B | ⭐ | Release Notes |
| 57 | B | ⭐⭐ | Project Management |
| 58 | B | ⭐ | Filtering |
| 59 | B | ⭐⭐ | PAT |
| 60 | B | ⭐⭐ | SSH Setup |
| 61 | B | ⭐ | 2FA |
| 62 | B | ⭐⭐ | GitHub Secrets |
| 63 | B | ⭐⭐⭐ | Exposed Secrets |
| 64 | B | ⭐⭐ | HTTPS vs SSH |
| 65 | B | ⭐ | SSH Keys |
| 66 | B | ⭐⭐ | Credential Rotation |
| 67 | B | ⭐⭐ | Audit Log |
| 68 | B | ⭐ | Visibility |
| 69 | B | ⭐⭐ | Outside Collaborators |
| 70 | B | ⭐⭐ | Permissions |
| 71 | B | ⭐⭐ | Branch Protection |
| 72 | B | ⭐⭐ | Org Access |
| 73 | B | ⭐⭐ | Secrets |
| 74 | B | ⭐⭐ | Offboarding |
| 75 | B | ⭐ | Least Privilege |
| 76 | B | ⭐⭐ | Visibility Change |
| 77 | B | ⭐ | Organizations |
| 78 | B | ⭐⭐ | Teams |
| 79 | B | ⭐⭐ | Billing |
| 80 | B | ⭐⭐ | Transfer |
| 81 | B | ⭐⭐⭐ | Org Policies |
| 82 | B | ⭐ | Enterprise |
| 83 | B | ⭐⭐ | Security Incidents |
| 84 | B | ⭐ | Dependabot |
| 85 | B | ⭐ | CI/CD |
| 86 | B | ⭐⭐ | Workflows |
| 87 | B | ⭐ | Failed Tests |
| 88 | B | ⭐⭐ | Code Quality |
| 89 | B | ⭐ | Deployment |
| 90 | B | ⭐ | Pre-commit |
| 91 | B | ⭐⭐ | Test Types |
| 92 | B | ⭐ | Monitoring |
| 93 | B | ⭐ | Open Source |
| 94 | B | ⭐ | Good First Issue |
| 95 | B | ⭐ | CLA |
| 96 | B | ⭐ | Sponsors |
| 97 | B | ⭐ | Learning |
| 98 | B | ⭐ | Trending |
| 99 | B | ⭐ | Discussions |
| 100 | B | ⭐ | Gists |
| 101 | B | ⭐⭐⭐ | Scenario |
| 102 | B | ⭐⭐⭐ | Scenario |
| 103 | B | ⭐⭐ | Scenario |
| 104 | B | ⭐⭐⭐ | Scenario |
| 105 | B | ⭐⭐ | Scenario |
| 106 | B | ⭐⭐⭐ | Scenario |
| 107 | B | ⭐⭐ | Scenario |
| 108 | B | ⭐⭐ | Scenario |
| 109 | B | ⭐⭐ | Scenario |
| 110 | B | ⭐⭐⭐ | Scenario |
| 111 | B | ⭐⭐⭐ | Scenario |
| 112 | B | ⭐⭐ | Scenario |

---

## Tips & Common Exam Traps

### ⚠️ Common Mistakes to Avoid

**1. Git Commands Confusion**
- ❌ Confusing `git reset` (removes commits) vs `git revert` (creates undo commit)
- ✅ Remember: `reset` = destructive, rewrite history; `revert` = safe, adds new commit
- **Exam trap:** "How to undo a commit that's been pushed?" → `git revert` (not `git reset`)

---

**2. SSH Key Security**
- ❌ Placing private key in public locations, sharing private key, wrong permissions
- ✅ Private key stays on your machine only; public key on GitHub; permissions `chmod 600`
- **Exam trap:** "What file goes on GitHub?" → Public key (id_rsa.pub or id_ed25519.pub), never private

---

**3. Merge vs. Rebase**
- ❌ Not understanding when to use each; rebasing on shared branches
- ✅ Use `rebase` on your feature branch before PR for clean history; use `merge` to preserve history
- **Exam trap:** "How to update feature branch from main?" → Can be either, but `rebase` preferred for clean history if branch is local only

---

**4. Private vs. Public Repository**
- ❌ Thinking making repo private deletes history or public forks
- ✅ Making private restricts access but doesn't delete; existing forks remain separate copies
- **Exam trap:** "What happens to existing forks when repo goes private?" → Forks stay as forked copies, now unreadable by others

---

**5. PAT Scope & Storage**
- ❌ Over-scoping PATs (giving full permissions when minimal needed), storing in code
- ✅ Use principle of least privilege; store PATs in environment variables or secret managers
- **Exam trap:** "Where should you store a GitHub PAT?" → NOT in code; use environment variables or GitHub Secrets in Actions

---

**6. Branch Protection Rules**
- ❌ Thinking they prevent merges entirely (they don't if you have access)
- ✅ They enforce requirements: reviews, status checks, but ultimately someone must click merge
- **Exam trap:** "What can't branch protection prevent?" → Still can't prevent force push by admins if rule doesn't forbid it

---

**7. Exposed Secrets**
- ❌ Just deleting the file in the next commit (secrets still in history!)
- ✅ Rotate credentials immediately; use BFG/git-filter-branch to remove from history; force push
- **Exam trap:** "You committed an API key to public repo, but deleted it in next commit. Is it safe?" → NO; it's still in history

---

**8. Collaborative Access Models**
- ❌ Giving everyone admin access "to be safe"
- ✅ Use principle of least privilege: start with read, escalate as needed
- **Exam trap:** "When should you make someone an org owner?" → Only people who need full org control; contributors should be lower roles

---

**9. Issue vs. Discussion**
- ❌ Using issues for Q&A or discussions for bug reports
- ✅ Issues = tasks/bugs (tracked work); Discussions = open-ended conversation (Q&A, ideas, announcements)
- **Exam trap:** "User asks 'how do I use feature X?' as issue" → Better as Discussion; can be converted to issue if it reveals a bug

---

**10. Semantic Versioning**
- ❌ Incrementing versions randomly or not communicating breaking changes
- ✅ MAJOR.MINOR.PATCH: MAJOR = incompatible, MINOR = new features, PATCH = bug fixes
- **Exam trap:** "From v1.5.3 to v2.0.0 is acceptable because?" → Yes, MAJOR bump for incompatible changes; users expect it with semver

---

### 🎯 Exam Success Strategy

**Before starting the exam:**
- [ ] Review the Answer Key Summary 2-3 times; focus on your weak domains
- [ ] Redo questions you got wrong; understand the explanation not just the answer
- [ ] Take a practice run under timed conditions (90-120 min) to build speed

**During the exam:**
- [ ] Read each question fully; trap words: "BEST", "FIRST", "ALWAYS", "NEVER"
- [ ] Flag difficult questions; answer easier ones first for confidence
- [ ] Pay attention to AWS/GitHub terminology: "Branch protection rule", "Outside collaborator", "Dependabot"
- [ ] When in doubt, choose the most secure/professional option

**After the exam:**
- [ ] Review questions you guessed on; understand why you guessed wrong
- [ ] Identify patterns: Do you struggle with Git commands? Permissions? Workflows?
- [ ] Create personal cheat sheet for weak areas

---

### 📈 Scoring Guide

- **90-112 (80-100%):** Excellent! You understand GitHub Foundation deeply
- **75-89 (67-79%):** Good! Passing score; review weak areas for mastery
- **60-74 (54-66%):** Passing level for many exams; focus on weak domains
- **< 60:** Review the study guide and retake after study

---

**Good luck on your GitHub Foundation (GH-900) certification! 🚀**

Remember:
- ✅ Practice the scenarios, not just memorize answers
- ✅ Understand the "why", not just the "what"
- ✅ GitHub is about collaboration; many questions test judgment not just knowledge
- ✅ When in doubt, choose the most secure/maintainable option

Happy studying!
