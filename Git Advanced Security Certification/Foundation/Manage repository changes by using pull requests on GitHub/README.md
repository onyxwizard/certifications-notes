# 🔄 Manage Repository Changes by Using Pull Requests on GitHub

Welcome! 👋 This guide will help you understand how to **manage changes in your GitHub repositories using pull requests (PRs)** — one of the most powerful tools for collaboration and code review.

Whether you're a beginner or an experienced contributor, this guide will walk you through everything from creating your first PR to merging it safely into the main branch. Let’s dive in! 🚀

## 🌿 What Are Branches?

Before we talk about pull requests, let's quickly recap **branches**.

Branches are isolated workspaces where developers can make changes without affecting the main codebase. They allow you to:
- Safely develop new features
- Fix bugs without breaking existing functionality
- Experiment with ideas before integrating them

The default branch is often called `main` or `master`. When you create a new branch, you’re working in your own copy of the repository that can later be merged back in.

> 🧠 Tip: Think of branches like separate drafts of a document — each one lets you work independently until you're ready to combine them.

## 📥 What Is a Pull Request?

A **pull request (PR)** is a way to propose changes from one branch to another. It allows team members to:
- Review proposed changes
- Discuss improvements
- Suggest edits
- Approve or reject the changes before they’re merged

Once approved, the changes are **merged** into the target branch (often `main` or `develop`).

> 💡 A PR is more than just a merge tool — it's a conversation hub for improving code together!

## 🛠️ Step-by-Step: Create a Pull Request

### 1. Navigate to Your Repository
Go to your project’s page on [GitHub.com](https://github.com).

### 2. Switch to Your Feature Branch
Click the **Branch** menu and select the branch with your changes.

![Screenshot of creating a new branch](https://learn.microsoft.com/en-us/training/github/manage-changes-pull-requests-github/media/2-new-branch-name-text-box.png)

### 3. Create the Pull Request
Above the list of files, click the yellow banner and select **Compare & pull request**.

![Compare & pull request button](https://learn.microsoft.com/en-us/training/github/manage-changes-pull-requests-github/media/2-compare-and-pull-request.png)

### 4. Fill in the Title and Description
Use clear language to explain:
- What you changed
- Why you made the change
- Any related issues (`#<ISSUE_NUMBER>`)

This helps reviewers understand the context and purpose of your PR.

## 🧾 Describe Your Changes Like a Pro

Good commit messages and PR descriptions make reviews easier and faster. Here’s how to write great ones:

### ✅ Commit Message Tips:
- Use the **imperative mood**: “Fix bug” not “Fixed bug”
- Keep the subject line under 50 characters
- Start with a capital letter, no period at the end
- Optional: use emojis or `@mentions` if appropriate

Example:
```
Fix typo in welcome message

Corrected spelling of "welcome" in homepage banner text.
```

## 🟢 Pass Status Checks

Before a PR can be merged, it may need to pass automated checks such as:
- CI/CD pipeline tests
- Linting rules
- Code formatting standards

If any check fails, fix the issue and push new commits. The status checks will automatically rerun.

> 🔍 Don’t worry if something fails — it’s there to help you catch problems early!

## 🗣️ Get Feedback and Make Improvements

After submitting your PR:
- Other contributors can comment and suggest changes
- You can respond, clarify, or update your code
- You can even ask for specific people to review your changes

If your PR is still a work-in-progress, consider marking it as a **Draft Pull Request**.

![Draft pull request option](https://learn.microsoft.com/en-us/training/github/contribute-open-source/media/3-draft-pr.png)

## 🧩 Merge the Pull Request

When your changes are reviewed and approved, it’s time to merge!

### Steps to Merge:
1. Go to the **Pull requests** tab in your repo.
2. Select the PR you want to merge.
3. Scroll down and choose a merge method:
   - **Create a merge commit**
   - **Squash and merge**
   - **Rebase and merge**

![Pull request merge options](https://learn.microsoft.com/en-us/training/github/manage-changes-pull-requests-github/media/3-select-author-of-merge.png)

4. Confirm the merge and optionally delete the feature branch.

> 🧹 Tip: Delete the compare branch after merging to keep your branch list clean.

## 🏁 Final Thoughts

Using pull requests effectively helps ensure high-quality code, improves team collaboration, and reduces errors.

Here’s what you’ve learned:
- How to create a PR from a feature branch
- How to describe your changes clearly
- How to get feedback and improve your code
- How to merge a PR successfully

## 🧪 Exercise: Review a Pull Request

Now it’s your turn! Try out what you've learned by completing a hands-on exercise:
- Create a real pull request
- Invite others to review
- Make changes based on feedback
- Merge your PR when it’s ready

## ❓ Quick Quiz

### 1. In GitHub, which status allows for ongoing discussion and additional commits?
- ❌ Closed pull request  
- ✅ Open pull request  
- ❌ Draft pull request  

### 2. What should you do if a developer realizes their PR isn't needed anymore?
- ❌ Merge and revert later  
- ❌ Convert to draft  
- ✅ Close without merging  

### 3. What does the base branch represent in a PR?
- ❌ Backup for the main branch  
- ❌ Experimental features  
- ✅ Target branch for merging changes  

## 📚 Want to Learn More?

Check out:
- [GitHub Pull Requests Docs](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)
- [How to Write Good Commit Messages](https://chris.beams.io/posts/git-commit/)
- [Creating Draft Pull Requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests#draft-pull-requests)

## 🙌 Happy Collaborating! 🎉

Pull requests are the heart of collaborative development on GitHub. Now that you know how to use them, go ahead and start contributing to projects, reviewing others' work, and improving code together.

Happy coding! 💻✨
