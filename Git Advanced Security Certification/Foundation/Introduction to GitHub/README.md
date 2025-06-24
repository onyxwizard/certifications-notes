# 🧾 GitHub: Empowering Developers, One Commit at a Time 💻

GitHub is a cloud-based platform that uses **Git**, a distributed version control system, to simplify collaboration and streamline software development. With its AI-powered tools, automation, security features, and global scale, GitHub has become the go-to platform for developers around the world.

Let’s dive into the core pillars of the **GitHub Enterprise Platform**: 🚀



## 🤖 AI – Powering Development with Intelligence

GitHub integrates **generative AI** to enhance every stage of the development lifecycle:
- Smarter **pull requests** and **issues**
- Boosted productivity with **GitHub Copilot**
- Proactive **security checks** powered by AI

AI isn’t just a feature—it’s woven into the fabric of how teams build software today.



## 🤝 Collaboration – The Heart of GitHub

Effortless teamwork is what GitHub is built for:
- Centralized **repositories**
- Real-time **code reviews**
- Streamlined **pull requests** and **issue tracking**

Whether you're a developer, project manager, or ops lead—GitHub brings your team together in one place.



## ⚡ Productivity – Automate the Routine

GitHub accelerates productivity through powerful automation:
- Built-in **CI/CD pipelines**
- Task automation
- Seamless integrations

This lets developers focus on what matters most—**innovation**. 🛠️



## 🔒 Security – Built-In, Not Bolted-On

Security starts at the code level:
- Native **security scanning**
- Automated **dependency updates** (via Dependabot)
- Private repositories with enterprise-grade controls

GitHub meets global compliance standards and is trusted by Microsoft and regulated industries. ✅



## 📈 Scale – Built for Growth

GitHub powers the world’s largest developer community:
- 100M+ developers
- 330M+ repositories
- Countless deployments daily

With real-time insights from this massive ecosystem, GitHub evolves with the needs of developers everywhere. 🌍



## 🏁 Conclusion – A Unified Developer Platform

The **GitHub Enterprise Platform** delivers an unparalleled developer experience by combining:
- **AI-driven innovation**
- **Seamless collaboration**
- **Automation for productivity**
- **Security-first design**
- **Massive global scale**

All in one unified platform. 🚀



🌟 *Built better. Shipped faster. Secured smarter.*  
*Welcome to the future of software development — on GitHub.* 🐙


# 📁 Introduction to Repositories 🚀

Let’s start learning about repositories — one of the most important tools for managing code on GitHub. Repos are where magic happens! 💻✨

### ❓ What is a Repository?

A repository contains all of your project's files and each file's revision history. It's one of the essential parts that helps you collaborate with people. You can use repositories to manage your work, track changes, store revision history, and work with others.

Before we dive too deep, let’s first start with how to create a repository. 🛠️



### ✅ How to Create a Repository

You can create a new repository on your personal account or any organization where you have sufficient permissions.

Let’s tackle creating a repository from github.com. 👇

1. In the upper-right corner of any page, use the drop-down menu, and select **New repository**.

    ![A screenshot of the drop-down menu of the plus sign in the top right corner of GitHub.com, with the first option being New repository.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-new-repo-option.png)

2. Use the **Owner** drop-down menu to select the account you want to own the repository.

    ![A screenshot of the drop-down menu of who should be the owner of the new repository.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-selecting-repo-owner.png)

3. Type a name for your repository, and an optional description.

    ![An image of the text box of the repository name highlighted.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-repo-name-text-box.png)

4. Choose a repository visibility.

   - 🔓 **Public repositories** are accessible to everyone on the internet.
   - 🔒 **Private repositories** are only accessible to you, people you explicitly share access with, and, for organization repositories, certain organization members.

5. Select **Create repository** and congratulations! 🎉 You just created a repository!



### 📄 How to Add a File to Your Repository

Files in GitHub can do a handful of things, but the main purpose of files is to store data and information about your project. It's worth knowing in order to add a file to a repository that you must first have minimum **Write** access within the repository you want to add a file.

Let’s review how to add a file to your repository.

1. On GitHub.com, navigate to the main page of the repository.

2. In your repository, browse to the folder where you want to create a file by selecting the **creating a new file** link or **uploading an existing file**.

3. Once added, above the list of files select the **Add file ᐁ** drop-down menu. Then select **Create new file**.

    ![A screenshot of the option to add a file to your new repository highlighted in red with the add file button towards the right of the screen.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/add-file-options.png)

4. In the file name field, type the name and extension for the file. To create subdirectories, type the **`/`** directory separator.

5. In the file contents text box, type **content** for the file.

6. To review the new content, above the file contents, select **Preview**.

    ![Screenshot showing a yml file with the preview button highlighted in the top left.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-preview-option-in-a-file.png)

7. Select **Commit changes**.

8. In the **Commit message** field, type a short and meaningful commit message that describes the change you made to the file. You can attribute the commit to more than one author in the commit message.

9. If you have more than one email address associated with your account on GitHub.com, select the email address drop-down menu. Then select the email address to use as the Git author email address. Only verified email addresses appear in this drop-down menu. If you enabled email address privacy, then _[username]@users.noreply.github.com_ is the default commit author email address.

    ![Screenshot showing a commit change with a description box and the drop-down menu of the email to select as the author of the commit.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-commit-description-box.png)

10. Below the **Commit message** fields, decide whether to add your commit to the current branch or to a new branch. If your current branch is the default branch, you should choose to create a new branch for your commit, and then create a pull request.

    ![Screenshot showing creating a new branch from a commit option select with the textbox of the new branch below it.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-create-a-new-branch.png)

11. Select **Commit changes** or **Propose changes**.

🎉 Congratulations, you just created a new file in your repository! You have also created a new branch and made a commit.



### 💬 What Are Gists?

Now that we have a good understanding of repositories, we can review gists. Similarly to repositories, gists are a simplified way to share code snippets with others.

Every gist is a Git repository, which you can fork and clone and be made either public or secret.

- 🔍 Public gists: Displayed publicly and searchable
- 🕶️ Secret gists: Not searchable, but visible if someone has the URL

To learn more about gists, see the linked article in our Resources section at the end of this module titled _Creating Gists_.



### 📚 What Are Wikis?

Every repository on GitHub.com comes equipped with a section for hosting documentation, called a wiki.

You can use your repository's wiki to share long-form content about your project, such as:
- How to use it
- How you designed it
- Its core principles

While a README file quickly tells what your project can do, you can use a wiki to provide additional documentation.

🔐 Note: If your repository is private, only people who have at least read access to your repository will have access to your wiki.

## 🔍 How to Search for Repositories

Looking for something specific? GitHub's search bar is powerful!

You can search by:
- Name
- Topic
- Language
- Stars
- Visibility (`is:public`, `is:private`)
- And more!

Example query:  
`react user:facebook language:javascript`

🔍 Visit [GitHub Explore](https://github.com/explore/repositories) to start browsing today!

# ⚙️ Components of the GitHub Flow

In this guide, we’ll explore the essential parts of the **GitHub flow**: **branches**, **commits**, **pull requests**, and how they all come together to help you collaborate safely and efficiently.

Let’s dive in! 🚀


## 🌿 What Are Branches?

In the last section, we created a new file and a new branch in your repositories.

Branches are an essential part of the GitHub experience because they're where we can make changes **without affecting the entire project** we're working on.

Your branch is a **safe place to experiment** with new features or fixes. If you make a mistake, you can revert your changes or push more changes to fix it. Your changes won't update on the default branch until you merge your branch.

📌 **Tip:** Alternatively, you can create a new branch and check it out by using Git in a terminal:
```bash
git checkout -b newBranchName
```

## 💾 What Are Commits?

In the previous unit, you added a new file into the repository by pushing a commit. Let’s briefly review what commits are.

A **commit** is a change to one or more files on a branch. Every time a commit is created, it's assigned a unique ID and tracked along with the time and contributor. Commits provide a clear audit trail for anyone reviewing the history of a file or linked item, such as an issue or pull request.

![A screenshot of a list of GitHub commits to a main branch.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-commits.png)

Within a Git repository, a file can exist in several valid states as it goes through the version control process. The primary states for a file in a Git repository are **Untracked** and **Tracked**.

### 🔍 File States in Git

- **Untracked:** An initial state of a file when it isn't yet part of the Git repository. Git is unaware of its existence.

- **Tracked:** A tracked file is one that Git is actively monitoring. It can be in one of the following substates:

  - **Unmodified:** The file is tracked, but it hasn't been modified since the last commit.
  - **Modified:** The file has been changed since the last commit, but these changes aren't yet staged for the next commit.
  - **Staged:** The file has been modified, and the changes have been added to the staging area (also known as the index). These changes are ready to be committed.
  - **Committed:** The file is in the repository's database. It represents the latest committed version of the file.

These states and substates are important to collaborating with your team to know where each and every commit is in the process of your project.

Now let’s move on to **pull requests**. 🔄



## 📥 What Are Pull Requests?

A **pull request** is the mechanism used to signal that the commits from one branch are ready to be merged into another branch.

The team member submitting the **pull request** asks one or more reviewers to verify the code and approve the merge. These reviewers have the opportunity to comment on changes, add their own, or use the pull request itself for further discussion.

Once the changes have been approved (if required), the pull request's source branch (the compare branch) is merged into the base branch.

![A screenshot of a pull request and a comment within the pull request.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-pull-request.png)



## 🔄 The GitHub Flow

![Screenshot showing a visual representation of the GitHub Flow in a linear format that includes a new branch, commits, pull request, and merging the changes back to main in that order.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/2-branching.png)

The GitHub flow can be defined as a lightweight workflow that allows for safe experimentation. You can test new ideas and collaboration with your team by using branching, pull requests, and merging.

Now that we know the basics of GitHub, we can walk through the GitHub flow and its components.

### 🧭 Step-by-step GitHub Flow:

1. **Create a branch** so that the changes, features, and fixes you create don't affect the main branch.
2. **Make your changes** — deploy them to your feature branch before merging into the main branch to ensure validity in a production environment.
3. **Create a pull request** to ask collaborators for feedback. Some repositories require an approving review before pull requests can be merged.
4. **Review and implement feedback** from your collaborators.
5. Once confident in your changes, get your pull request approved and **merge it into the main branch**.
6. Finally, **delete your branch**. This signals your work is complete and prevents accidental reuse of old branches.

🎉 That’s it — you’ve completed a full GitHub flow cycle!

# 🤝 GitHub is a Collaborative Platform

Collaboration lies at the heart of everything GitHub does. In previous sections, we explored **repositories** and **pull requests** — essential tools that help you manage code and contributions.

In this unit, we’ll dive into two more powerful collaboration tools: **Issues** and **Discussions** — both designed to help teams communicate, plan, and build together.

Let’s get started! 🚀

## 🧾 Issues – Track Ideas, Tasks & Bugs

GitHub Issues are used to track ideas, feedback, tasks, or bugs related to your project. They’re flexible and can be created in multiple ways:
- From a task list
- From a note in a project board
- From a comment in an issue or pull request
- From a specific line of code
- Or even from a custom URL

### ✅ How to Create an Issue from a Repository

1. On GitHub.com, navigate to the main page of the repository.

2. Under your repository name, select **Issues**.

    ![Screenshot showing the top portion of the main page of a repository with the Issues section highlighted.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/issues-tab.png)

3. Select **New issue**.

4. If your repo uses templates, choose one by clicking **Get started**, or select **Open a blank issue**.

    ![A screenshot of the issue templates menu, with the Open a blank issue option highlighted.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/open-a-blank-issue.png)

5. Enter a title in the **Add a title** field.

6. Type a description in the **Add a description** field.

7. (Optional) As a maintainer, you can:
   - Assign the issue to someone
   - Add it to a project board
   - Associate it with a milestone
   - Apply labels

8. Click **Submit new issue** when done.

🎉 You've just created an issue!

Some conversations don’t belong in issues — they're better suited for **Discussions**. Let’s take a look at how to use them.


## 💬 Discussions – Engage in Conversations

GitHub Discussions are perfect for open-ended conversations that aren’t tied directly to code. Use them to:
- Ask and answer questions
- Share knowledge
- Make announcements
- Discuss ideas or improvements

### 🔧 Enabling Discussions in Your Repository

Only **repository owners** or users with **Write access** can enable discussions.

1. Go to your repository’s main page.

2. Under your repository name, click **Settings**.

    ![A screenshot of the top portion of the main page of a repository with the Settings section highlighted.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/settings-tab.png)

3. Scroll down to the **Features** section, then click **Setup discussions** under the Discussions tab.

    ![A screenshot of the Discussions box with the green Setup discussion button highlighted.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/set-up-discussion.png)

4. Edit the welcome message template to reflect your community tone and resources.

5. Click **Start discussion**.

You’re now ready to start creating discussions!


### 📝 How to Create a New Discussion

Anyone who can view the repository can create a discussion.

1. Navigate to the main page of the repository or organization.

2. Under the name, click **Discussions**.

    ![A screenshot of the top portion of the main page of a repository with the Discussions section highlighted.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/discussions-tab.png)

3. On the right side of the page, click **New discussion**.

4. Choose a category by clicking **Get started**. All discussions must be filed under a category defined by maintainers or admins.

    ![A screenshot of the select a discussion category menu selection, with the top option Announcements and the get started button highlighted.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/announcements.png)

#### Default Discussion Categories

|**Category**|**Purpose**|**Format**|
|---|---|---|
|📣 Announcements|Updates and news from project maintainers|Announcement|
|#️⃣ General|Anything and everything relevant to the project|Open-ended discussion|
|💡 Ideas|Ideas to change or improve the project|Open-ended discussion|
|🗳️ Polls|Polls with multiple options for voting|Polls|
|🙏 Q&A|Questions for the community to answer|Question and Answer|
|🙌 Show and tell|Creations, experiments, or tests related to the project|Open-ended discussion|

5. Give your discussion a clear title and write the body content.

    ![A screenshot of starting a new discussion page with the Discussion title box and content box empty.](https://learn.microsoft.com/en-us/training/github/introduction-to-github/media/start-a-new-discussion.png)

6. Click **Start discussion**.

🎉 Your discussion is live and ready for responses!



## 🎯 Summary

In this unit, you learned:
- ✅ How to create and manage **GitHub Issues**
- 💬 How to enable and create **GitHub Discussions**
- 🗂️ The purpose and structure of discussion categories
- 🧭 When to use issues vs. discussions for effective collaboration

These tools empower teams to stay aligned, communicate clearly, and move projects forward — all within the GitHub platform.

# 🛠️ GitHub Platform Management

  
Now that you're familiar with the basics of GitHub — like repositories, branches, commits, issues, and pull requests — it’s time to level up and explore how to **manage your experience** on GitHub.


In this guide, we’ll cover:

- 🔔 Managing notifications and subscriptions  

- 📡 Subscribing to threads and finding mentions  

- 🌐 Publicizing your project or organization using **GitHub Pages**

Let’s dive in! 💻✨

  
## 🔔 Managing Notifications and Subscriptions

Notifications help you stay informed about activity happening across your repositories, issues, and conversations.

### 📬 What Are Subscriptions?

You can choose to receive updates through **subscriptions** for specific types of activity on GitHub.com. These updates appear as **notifications**.

### 📢 Types of Subscription Options

You can subscribe to be notified about:

- 🗣️ A conversation in a specific issue, pull request, or gist  

- 🤖 CI activity (e.g., status of workflows in repositories using **GitHub Actions**)  

- 📥 Repository-wide activity such as issues, pull requests, releases, or security alerts  

- 🧩 Discussions (if enabled in the repo)  

- 📦 All activity in a repository  

### 🔄 Automatic Subscriptions

You’re automatically subscribed to conversations when you:

- Open an issue or pull request  

- Comment on a thread  

- Get assigned to an issue or pull request  


### 🚫 Unsubscribe or Customize


If you no longer want to follow a conversation:

- **Unsubscribe**

- **Unwatch** the repository

- Or customize what notifications you receive going forward

💡 Tip: If you want to find issues or discussions where you were mentioned, use the `mentions:` qualifier in GitHub’s search bar:

```bash

mentions:@username

```


## 🌐 What is GitHub Pages?

To wrap up our GitHub journey, let’s explore **GitHub Pages** — a powerful tool for sharing your work with the world.


GitHub Pages allows you to:

- 🏗️ Host a static website directly from a GitHub repository  

- Showcase your **portfolio**, **project documentation**, or **organization page**  

- Use HTML, CSS, and JavaScript files — optionally processed through a build step  

- Publish changes instantly by pushing to your branch  

  

Once published, your site is live and publicly accessible at a custom URL like:

```

https://<your-username>.github.io/<repository-name>

```

It’s perfect for developers, teams, and open-source projects who want to share their story, tools, or ideas in a visually appealing way.


## 🧪 Exercise: Let’s Put It All Together!

In the next hands-on exercise, you'll walk through the full **GitHub flow** by:

  

1. ✅ Creating a new repository  

2. 🌿 Creating a new branch  

3. 📄 Committing a file  

4. 📥 Opening a pull request  

5. 🧾 Merging the pull request  

  

This will solidify everything you've learned so far and show you how to collaborate effectively using GitHub.


## 🎯 Summary

  

In this unit, you learned:

- 🔔 How to manage notifications and subscriptions  

- 🧵 How to follow or find important threads and mentions  

- 🌍 How to publicize your work using GitHub Pages  

  

These tools help you stay connected, organized, and visible while working on GitHub.


# 📚 GitHub Knowledge Check

Test your understanding of key GitHub concepts with this quiz! Each question includes all answer choices, with correct answers clearly marked.


## 1. ✅ Why use GitHub Issues for task tracking?

**Question:**  
In a collaborative project, a team member suggests using GitHub Issues for tracking tasks. What is the primary advantage of using GitHub Issues for task management?

- ✅ **They provide a centralized location for tracking ideas, feedback, tasks, and bugs.**  
- ❌ They automatically resolve tasks without team input.  
- ❌ They restrict visibility of tasks to only project managers.



## 2. 💬 When to Use GitHub Discussions

**Question:**  
Why might a GitHub Discussion be more appropriate than an Issue for certain topics?

- ✅ **Discussions facilitate open-ended conversations and community engagement.**  
- ❌ They provide automatic notifications for all participants.  
- ❌ They automatically track progress on project tasks.



## 3. 🌿 Preparing for Deployment Using Branches

**Question:**  
Your team is preparing to deploy a new feature using GitHub branches. What should be done to ensure the feature branch is ready for deployment?

- ❌ Commit all changes directly to the main branch without review.  
- ✅ **Ensure all changes are reviewed and approved through a pull request before merging into the main branch.**  
- ❌ Delete the feature branch to finalize the deployment process.


## 4. 🔔 Benefits of Customizing Notifications

**Question:**  
What is a benefit of customizing notification settings on GitHub?

- ❌ It automatically unsubscribes you from all repository notifications.  
- ✅ **It allows you to stay informed about specific activities without being overwhelmed by irrelevant updates.**  
- ❌ It enables automatic deletion of old notifications.



## 5. 🧱 Purpose of Creating a Branch

**Question:**  
In the GitHub flow, what is the main purpose of creating a branch before starting work on new features or fixes?

- ✅ **To ensure the main branch is always stable and unaffected by ongoing work.**  
- ❌ To create backups of the main branch.  
- ❌ To automatically merge changes with the main branch.



## 6. 🗣️ GitHub Discussions for Collaboration

**Question:**  
Your team wants to enhance collaboration by using GitHub Discussions. What is a key feature of GitHub Discussions that supports open communication?

- ❌ They automatically generate action items for team members.  
- ✅ **They enable fluid, open conversation accessible to everyone with repository access.**  
- ❌ They are limited to code-related topics only.



## 7. 🛠️ GitHub Issues vs Discussions

**Question:**  
In what scenario would GitHub Issues be more effective than Discussions?

- ❌ When making announcements and sharing news with the team.  
- ✅ **When tracking specific tasks and bugs that require resolution.**  
- ❌ When seeking community input on project ideas and improvements.


## 8. 📁 Role of a GitHub Repository

**Question:**  
What is the primary function of a GitHub repository?

- ❌ To host discussions and community engagement.  
- ❌ To automate code deployment processes.  
- ✅ **To manage project files and track their revision history.**


## 9. 📤 Adding Files to a Repository

**Question:**  
Which action is necessary for adding a file to a GitHub repository?

- ✅ **Having write access to the repository.**  
- ❌ Being a repository owner.  
- ❌ Having read access to the repository.


📘 Stay tuned for the next guide: **"Introduction to GitHub's products"**

Happy coding! 🧑‍💻✨