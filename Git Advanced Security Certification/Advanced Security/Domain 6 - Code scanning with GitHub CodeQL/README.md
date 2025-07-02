# 🔍 Domain 6 - Code Scanning with GitHub CodeQL

Welcome to **Domain 6** of GitHub Advanced Security (GHAS)! 🚀  
In this guide, you'll learn how to **use GitHub CodeQL for code scanning** — a powerful way to detect security vulnerabilities and coding errors in your repositories.

Whether you're a developer, DevOps engineer, or part of a security team, mastering CodeQL will help you write more secure code and catch issues early in the development lifecycle. Let’s dive in! 💻🔒

## 🧠 What Is Code Scanning with GitHub CodeQL?

**Code scanning** is an automated process that helps identify potential security vulnerabilities and bugs in your source code. It's built into GitHub and powered by **GitHub CodeQL**, a semantic code analysis engine that treats code like data.

With CodeQL:
- You can find real-world vulnerabilities like SQL injection, XSS, and command injection
- You can write custom queries to detect patterns unique to your organization
- You get alerts directly in the **Security tab** of your repository

> 💡 Think of CodeQL as a search engine for your code — helping you find not just what the code does, but what it could do if exploited.

## 🛠️ How Does Code Scanning Work?

Code scanning works in three main steps:

### 1. 📦 Create a CodeQL Database
CodeQL builds a relational database from your codebase using:
- Abstract syntax trees (AST)
- Control-flow graphs
- Data-flow graphs

This allows deep analysis of complex logic and relationships in your code.

> 📌 Example: For Java, CodeQL understands object-oriented structures like inheritance and polymorphism.

### 2. 🧩 Run Queries on the Database
Queries are written in **QL**, a logic-based query language designed for code analysis.

Here’s a basic example:
```ql
/**
 * @name Unsafe Function Call
 * @description Detects use of unsafe eval() function
 */
import javascript

from FunctionCall call
where call.getFunc().getName() = "eval"
select call, "Avoid using eval() with untrusted input."
```

You can run:
- ✅ Built-in queries from GitHub researchers
- ✅ Custom queries created by your team
- ✅ Community-maintained queries from open-source projects

### 3. 📊 View Results as Alerts
After running queries, results are uploaded in **SARIF format** (Static Analysis Results Interchange Format), which integrates directly into GitHub as **code scanning alerts**.

You can view these alerts in the **Security tab** of your repository.

![Screenshot showing CodeQL analysis alerts](https://learn.microsoft.com/en-us/training/github/codebase-representation-codeql/media/query-metadata.png)

## 🧰 Supported Languages

CodeQL supports many popular programming languages, including:
- C / C++
- C#
- Go
- Java / Kotlin
- JavaScript / TypeScript
- Python
- Ruby
- Swift

This makes it versatile for multi-language projects and teams.

## 🛠️ Step-by-Step: Enable Code Scanning with CodeQL

### Option 1: Use Default Setup (Recommended)

1. Go to your repo > **Security tab**
2. Click **Set up code scanning**
3. Choose **Default setup**
4. Select **Enable CodeQL**

GitHub will create a workflow file (`.github/workflows/codeql-analysis.yml`) and start scanning your code automatically.

> ✅ This method requires no configuration — perfect for most projects.

### Option 2: Use Advanced Setup (Custom Workflow)

For advanced users who want full control:

1. Go to **Security tab**
2. Click **Set up code scanning**
3. Choose **Advanced setup**
4. Download the workflow template
5. Customize settings (languages, paths, schedule, etc.)
6. Commit the updated workflow back to your repo

#### Example Customization:
```yaml
on:
  push:
    branches: [ "main" ]
  schedule:
    - cron: '0 0 * * 0'  # Run weekly on Sunday at midnight
```

This lets you define when and what gets scanned.

## 📁 Understanding the CodeQL Workflow File

The default workflow file looks like this:

```yaml
name: "CodeQL"
on:
  push:
    branches: [ "main" ]
jobs:
  analyze:
    name: Analyze
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v3
      - name: Initialize CodeQL
        uses: github/codeql-action/init@v2
      - name: Perform CodeQL Analysis
        uses: github/codeql-action/analyze@v2
```

You can edit this file to:
- Scan specific directories only
- Change scan frequency
- Add custom queries or rules

## 🧪 Review and Manage Code Scanning Alerts

All alerts appear in the **Security > Code scanning alerts** section of your repo.

From there, you can:
- Filter by severity (critical, high, medium, low)
- Sort by language or date
- Investigate the affected files
- Dismiss false positives

> 🧠 Tip: Always triage alerts — not all are relevant to your context.

## 🧹 Resolving Alerts

When you fix an issue:
1. Update the code
2. Push the changes
3. The alert will close automatically

If the alert was a false positive:
1. Open the alert
2. Click **Dismiss**
3. Choose a reason (e.g., “Inaccurate” or “Not relevant”)

This keeps your alert list clean and focused on real issues.

## 🔄 Schedule Regular Scans

To keep your codebase secure over time, set up scheduled scans:

### In your workflow file:
```yaml
on:
  schedule:
    - cron: '0 0 * * 0'  # Weekly
```

This ensures you catch any newly discovered issues even if no active development is happening.

## 👥 Who Can View and Manage Alerts?

Only users with **write, maintain, or admin** access to the repo can view and manage code scanning alerts.

Repository owners and admins can grant additional users access via:
- **Settings > Advanced Security > Access to alerts**

## 🧱 Integrate with CI/CD Pipelines

Code scanning fits seamlessly into your existing CI/CD workflows.

Use GitHub Actions to:
- Scan on every push or PR
- Fail builds if critical issues are found
- Upload results from local or remote tools

This brings security into your daily development flow — no extra effort required.

## 🎯 Best Practices for Using Code Scanning

✅ Start early — configure code scanning as soon as possible  
✅ Fix issues as they appear — don’t let them pile up  
✅ Use scheduled scans to stay proactive  
✅ Review and dismiss false positives  
✅ Combine with secret scanning and Dependabot for full coverage  
✅ Train your team to act on alerts quickly  

> 🧬 Remember: Code scanning isn’t just about finding bugs — it’s about preventing future ones.

## 🙌 Final Thoughts

Code scanning is one of the most powerful tools in your GitHub Advanced Security arsenal. By detecting issues early and providing actionable insights, it helps teams write better, safer code without slowing down development.

Start today by enabling code scanning, reviewing alerts, and integrating it into your CI/CD pipeline. And don’t forget to share knowledge with your team so everyone benefits.

Stay secure! 🔐✨

## 📚 Want to Learn More?

Check out:
- [Code Scanning Documentation](https://docs.github.com/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning)
- [Using CodeQL](https://docs.github.com/code-security/code-scanning/using-codeql-code-scanning-for-checkmarx-one)
- [Integrating with Code Scanning](https://docs.github.com/code-security/code-scanning/integrating-with-code-scanning)

## ✅ Exercise: Configure Code Scanning

Try what you've learned by completing a hands-on exercise:
- Enable code scanning for a repo
- Trigger a scan manually
- Review and resolve an alert
- Customize the workflow file
- Upload a SARIF file from an external tool

This practice will reinforce your understanding and help you become a GHAS pro! 💪

Ready to secure your code? Start scanning today! 🔍🚀
