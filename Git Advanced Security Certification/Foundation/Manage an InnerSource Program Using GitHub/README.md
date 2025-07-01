# 🌐 Manage an InnerSource Program Using GitHub

Welcome! 👋 This guide will help you understand how to **set up and manage a successful InnerSource program** using **GitHub**. Whether you're leading a team, working in a large organization, or simply looking to improve collaboration within your company, this document is for you.

InnerSource brings the best practices of open-source development into private, internal environments — like your company’s own codebase. It helps teams collaborate more effectively, reuse code, and build better software together. Let's dive in! 🚀

## 💡 What Is InnerSource?

**InnerSource** means applying open-source principles to internal software projects. It allows employees within your organization to:

- View, modify, and share code freely.
- Collaborate across teams.
- Improve productivity by reusing existing solutions.

### 🌱 Benefits of InnerSource

1. **Transparency**  
   Teams can see how others solve problems and reuse code or assets, making development faster and more efficient.

2. **Reduced Friction**  
   If one team depends on another, they can propose changes directly instead of waiting for someone else to act.

3. **Standardized Practices**  
   Encourage consistent workflows, contribution guidelines, and communication standards across all teams.

> 📚 Learn more: [An Introduction to InnerSource](https://resources.github.com/whitepapers/introduction-to-innersource/)

## 🔧 Set Up Your InnerSource Program on GitHub

### 1. Choose Repository Visibility

GitHub supports three levels of visibility for repositories:

- **Public**: Visible to everyone (for true open-source projects).
- **Internal**: Only visible to members of your organization ✅ *(Best for InnerSource)*
- **Private**: Visible only to specific users or teams.

Use **Internal** visibility to keep your InnerSource project accessible within your company while maintaining control.

### 2. Set Permissions

Assign access based on contributor roles:

| Role | Best For |
|------|----------|
| **Read** | Non-code contributors who want to view or discuss the project |
| **Triage** | Contributors managing issues/pull requests without writing code |
| **Write** | Developers actively contributing code |
| **Maintain** | Project managers handling repository settings |
| **Admin** | Owners with full control over the repo |

> 🔐 Make sure permissions are clear so people have just enough access to contribute.

## 🗂️ Create Discoverable Repositories

As your InnerSource program grows, it becomes harder to find relevant repositories. Help your team discover what’s available by following these best practices:

✅ Use **descriptive names**, like `warehouse-api` or `supply-chain-web`.  
✅ Add a **clear description** so users know what the repo does.  
✅ **License your code** so users understand how they can use it.  
✅ Include a **README.md** file as the landing page.

## 📄 Write a Great README

Your README is the first thing people see when visiting your repo. Make it count!

### What to Include:

- Purpose and vision of the project
- Visual aids (screenshots, diagrams, code samples)
- Links to demos or production versions
- Prerequisites and setup instructions
- Dependencies used in the project

Place your `README.md` in the root folder, `.github`, or `docs` directory for GitHub to display it automatically.

> 🎨 Check out some [Awesome README Examples](https://github.com/matiassingers/awesome-readme) for inspiration.

## 🛠️ Guide Contributions with Key Files

Help contributors understand how to work with your project by including these files:

### 📝 CONTRIBUTING.md
This file explains:
- How to submit issues or pull requests
- Coding conventions
- Expected behavior from contributors

GitHub shows a link to this file when users create issues or PRs.

> 📚 Find great examples at [Awesome CONTRIBUTING.md](https://github.com/mntnr/awesome-contributing)

### 👮 CODEOWNERS
Define who should review specific parts of the codebase. This ensures that changes go through the right reviewers.

### 📋 ISSUE & PULL REQUEST TEMPLATES
Use `.github/ISSUE_TEMPLATE.md` and `.github/PULL_REQUEST_TEMPLATE.md` to guide users in submitting complete information.

Example template fields:
- Description of the issue or change
- Steps to reproduce bugs
- Environment details
- Screenshots or logs

> 📁 Explore [Awesome GitHub Templates](https://github.com/devspace/awesome-github-templates)

## 🔄 Define Clear Workflows

Make sure everyone understands how to contribute by defining your Git workflow:

- Which branches to use for features and bug fixes
- How to open pull requests
- How to handle releases and deployments

If you're unsure where to start, try the **[GitHub Flow](https://guides.github.com/introduction/flow/)**.

Also, define how your team handles branching strategies and release cycles. Communicating this clearly reduces confusion and improves efficiency.

## 📊 Measure Success

Tracking the right metrics helps you understand how well your InnerSource program is working.

### 📈 Focus On These Metrics:

- Code review turnaround time
- Pull request size and frequency
- Number of unique contributors
- Number of cross-team interactions
- Projects reusing shared code

Avoid focusing only on output-based metrics like number of lines written. Instead, measure **team collaboration** and **process improvements**.

> 📖 See real-world success stories in [InnerSource Case Studies](https://gist.github.com/githubteacher/9fe53687a5f173d1d64c24c68625349e)

## 🧰 Ready to Launch?

Here’s a quick checklist to make sure your InnerSource program is set up for success:

✅ Set repository visibility to Internal  
✅ Assign appropriate permissions  
✅ Add a descriptive README  
✅ Include CONTRIBUTING, CODEOWNERS, and templates  
✅ Define workflows and contribution guidelines  
✅ Track meaningful metrics  

## 🙌 Final Thoughts

InnerSource isn’t just about code — it’s about culture. By encouraging transparency, collaboration, and reuse, you’re helping your teams move faster, smarter, and more efficiently.

Start small, iterate often, and don’t forget to celebrate your wins along the way! 🎉

## 📣 Want to Learn More?

Check out:
- [GitHub InnerSource Resources](https://resources.github.com/)
- [GitHub Flow](https://guides.github.com/introduction/flow/)
- [Git Branching Strategy](https://learn.microsoft.com/en-us/azure/devops/repos/git/git-branching-guidance)

Happy InnerSourcing! 🚀✨
