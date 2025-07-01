# 🔍 Search and Organize Repository History by Using GitHub

Welcome! 👋 In this guide, you'll learn how to **search and organize repository history on GitHub** using powerful tools like filters, blame, and cross-linking. Whether you're new to a project or trying to track down a bug, these skills will help you navigate your codebase like a pro. 🚀

Let’s dive in!

## 🧩 Why Search and Organize Repository History?

When you join a large project or encounter a bug, understanding the history of changes helps you:
- Find the source of issues quickly
- Identify who worked on specific files
- Link related commits, issues, and pull requests
- Understand why certain changes were made

GitHub offers powerful tools to make this process efficient and intuitive.

## 🕵️‍♂️ Use Filters to Narrow Down Your Search

GitHub allows you to **filter commits, issues, pull requests**, and more based on various criteria.

### Example Filter Queries:
| Query | What It Does |
|-------|--------------|
| `is:open is:issue assignee:@me` | Show open issues assigned to me |
| `is:closed is:pr author:contoso` | Closed PRs created by @contoso |
| `author:johndoe` | Show all changes made by Johndoe |
| `path:src/sidebar.js` | Show commits affecting sidebar.js |

Use these filters in global search or context-specific tabs like **Issues** or **Pull Requests** for better results.

## 🧾 Explore File History with Blame View

The **Blame View** shows you who last modified each line of a file and when.

### 💡 When to Use Blame:
- To find the person responsible for a specific change
- To understand when and why a bug was introduced
- To locate experts on a particular file or feature

Just click the **Blame** button next to any file to see its full history.

![Screenshot of GitHub blame](https://learn.microsoft.com/en-us/training/github/search-organize-repository-history-github/media/2-github-blame.png)

## 🔗 Cross-Link Issues, Commits, and Pull Requests

GitHub makes it easy to connect different parts of your project.

### ✅ Autolinked References
You can automatically link:
- Issues by typing `#<ISSUE_NUMBER>`
- Commits by pasting the first 7+ characters of a SHA hash

Example:
```
Fixed issue reported in #15
```

GitHub turns these into clickable links that help you trace connections across your project.

![Screenshot of an autolinked issue](https://learn.microsoft.com/en-us/training/github/search-organize-repository-history-github/media/2-autolinked-issue.png)

## 📣 Mention Users with @Mentions

Want to loop someone into a discussion? Just use an `@mention`.

Example:
```
@johndoe Can you confirm if this fix matches the original design?
```

This notifies the user and adds them to the conversation — perfect for collaboration and knowledge sharing.

![Screenshot of an @ mention](https://learn.microsoft.com/en-us/training/github/search-organize-repository-history-github/media/2-user-mention.png)

## 🔍 Master the GitHub Search Bar

GitHub has two main types of search:

### 1. 🌐 Global Search
- Found at the top of every GitHub page
- Lets you search across **all repositories, users, issues, and more**
- Great for broad searches across multiple projects

![A screenshot of a search across GitHub](https://learn.microsoft.com/en-us/training/github/search-organize-repository-history-github/media/2-global-search.png)

### 2. 🔍 Context Search
- Available on repository tabs like **Issues**, **Pull Requests**, or **Insights**
- Scoped to the current repo only
- Allows filtering by labels, authors, projects, and more

![Screenshot of a context search within a repository](https://learn.microsoft.com/en-us/training/github/search-organize-repository-history-github/media/2-context-search.png)

> Tip: Use [Advanced Search](https://github.com/search/advanced) to build complex queries and filter results precisely.

## 🧪 Exercise: Connect the Dots in a GitHub Repository

Now it’s time to practice what you’ve learned!

In this hands-on exercise:
- Build a small repository with sample commits and issues
- Duplicate issues and explore how they’re linked
- Fix a content defect using search and blame tools

You’ll get real experience navigating and organizing repository history like a seasoned developer. 💻✅

## ❓ Quick Quiz

### 1. How does GitHub's top-level search bar differ from repository tab searches?
- ❌ They're otherwise the same
- ❌ Different filter syntax options
- ✅ Top-level searches everything; tab searches are scoped

### 2. What does `git blame` do?
- ❌ Creates a bug report
- ✅ Shows commit history per line in a file

## 📚 Want to Learn More?

Check out:
- [GitHub Search Documentation](https://docs.github.com/en/search-github)
- [Using Git Blame](https://docs.github.com/en/repositories/working-with-files/using-files/viewing-a-file-s-history)
- [Autolinked References](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/autolinked-references-and-urls)

## 🙌 Final Thoughts

Searching and organizing repository history is a superpower in software development. With tools like filters, blame, and cross-linking, you can uncover insights, fix bugs faster, and collaborate more effectively.

So go ahead — explore your repositories, trace bugs to their roots, and become a GitHub history master! 🎯✨
