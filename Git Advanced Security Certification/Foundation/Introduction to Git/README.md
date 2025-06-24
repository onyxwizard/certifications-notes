# 🧠 Introduction to Git – Certification Prep Guide

> _“With Git, every developer gets their own sandbox. With GitHub, they get a playground.”_ – DevOps Wizard 🧙‍♂️

Welcome to your **certification prep guide for Git fundamentals**! This document covers everything you need to know about **Git basics**, including what version control is, how Git works, and essential commands.

This guide aligns with Microsoft Learn modules and real-world scenarios, making it perfect for **GitHub certification prep** or general Git mastery.


## 🔍 What is Version Control?

A **Version Control System (VCS)** helps track changes in files over time. It allows multiple people to work on the same project simultaneously without conflicts and lets you revert to any previous state of your work.

### Why Use Version Control?
✅ Track who made what change and when  
✅ Revert to earlier versions safely  
✅ Work on experimental features using **branches**  
✅ Collaborate efficiently across teams  
✅ Maintain a full history of your project  

Git is one of the most popular VCS tools — fast, distributed, open-source, and widely used in industry.


## 🌐 Distributed Version Control Explained

Unlike older systems like SVN that rely on a central server, **Git is distributed**. That means:

- Every developer has a **full copy** of the repository (including full history)
- You can commit changes **locally**, even offline
- If the remote server fails, any local clone can restore it
- Collaboration happens via **pushing** and **pulling** between repos

This makes Git **robust, scalable, and secure** — ideal for both small and enterprise-level projects.


## 📚 Git Terminology You Must Know

Before diving into commands, let’s review key Git terms:

| Term | Meaning |
|------|---------|
| **Working Tree** | The actual files you’re working on |
| **Repository (Repo)** | The `.git` folder storing all metadata and history |
| **Commit** | A snapshot of your current changes |
| **Branch** | A line of development; main branch is usually `main` or `master` |
| **HEAD** | Refers to the current commit or branch |
| **Hash / SHA-1** | Unique ID representing a commit or object |
| **Object** | Git stores data as blobs (files), trees (directories), commits, and tags |
| **Remote** | A reference to another repo (like GitHub) |
| **Staging Area** | Where you prepare changes before committing |

💡 Pro Tip: Use `git help` or `git <command> --help` to explore more details about each command!

## 🛠️ Essential Git Commands

Here are the core Git commands you'll use daily and should master for certification.

| Command | Description |
|--------|-------------|
| `git init` | Initialize a new Git repository |
| `git clone <url>` | Clone an existing repo from a remote source |
| `git status` | Show the working tree status (which files are modified, staged, etc.) |
| `git add <file>` | Add changes to the staging area |
| `git commit -m "message"` | Save a snapshot of your changes with a message |
| `git log` | View commit history |
| `git config --global user.name/email` | Set your Git identity |
| `git branch` | List branches or create a new one |
| `git checkout <branch>` | Switch to a different branch |
| `git push origin <branch>` | Push your changes to a remote repository |
| `git pull` | Fetch and merge changes from a remote repo |

📘 Example:
```bash
# Configure Git globally
git config --global user.name "YourName"
git config --global user.email "you@example.com"

# Create a new repo
mkdir MyProject && cd MyProject
git init

# Make some changes, then stage and commit
git add .
git commit -m "Initial commit"

# View commit history
git log
```



## 🧪 Exercise Summary: Try Out Git

Here's a quick recap of setting up and using Git locally:

1. **Check Git version**:  
   ```bash
   git --version
   ```

2. **Configure Git**:  
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your@email.com"
   ```

3. **Initialize a repo**:  
   ```bash
   mkdir Cats && cd Cats
   git init -b main
   ```

4. **Check status and start tracking files**:  
   ```bash
   git status
   # Create or modify files here
   git add .
   git commit -m "First commit"
   ```

5. **View history**:  
   ```bash
   git log
   ```

You now have a fully functional Git repo and understand the basic workflow!



## 🧩 Module Assessment – Practice Questions

Test your knowledge with these sample questions aligned with the module assessment:

### 1. Which of the following is a common use case for a version control system?
- ❌ Deleting earlier versions permanently  
- ✅ Making experimental changes in an isolated branch  
- ❌ Gathering feature requirements  

### 2. What is another name for a version control system?
- ❌ Version Management Software (VMS)  
- ❌ Software Control Management (SCM)  
- ✅ Software Configuration Management (SCM)  

### 3. What’s the difference between Git and GitHub?
- ✅ Git lets you work with local branches and push to a remote. GitHub acts as the remote repository.  
- ❌ Git runs in the cloud, GitHub provides access  
- ❌ Git is individual, GitHub is group-focused  

### 4. What Git command gives information about how to use Git?
- ❌ `git init`  
- ❌ `git status`  
- ✅ `git help`



🎯 Keep practicing with real repos, branching, and merging — it's the best way to reinforce learning!





📘 Stay tuned for the next guide: **"Introduction to GitHub"**

Happy coding! 🧑‍💻✨
