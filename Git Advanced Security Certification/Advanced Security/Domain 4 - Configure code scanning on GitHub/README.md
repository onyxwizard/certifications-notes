# 🔍 Domain 4 - Configure Code Scanning on GitHub

Welcome to **Domain 4** of GitHub Advanced Security (GHAS)! 🚀  
In this guide, you’ll learn how to **configure and use code scanning** — a powerful tool that helps detect security vulnerabilities and coding errors in your GitHub repositories.

Whether you're a developer, DevOps engineer, or part of a security team, mastering code scanning is essential for building secure and reliable software. Let’s dive in! 💻🔒

## 🧠 What Is Code Scanning?

**Code scanning** is an automated feature in GitHub that analyzes your source code to find:

- 🔐 Security vulnerabilities (like SQL injection or XSS)
- 🐞 Coding errors
- ⚠️ Bad practices that could lead to bugs or exploits

It uses **GitHub’s CodeQL engine**, a powerful semantic analysis tool, to deeply understand your code and find issues others might miss.

> 💡 Think of code scanning like a spellchecker for security and quality — catching problems before they become real threats!

## 🛠️ Why Code Scanning Matters

Modern software development moves fast, but it's easy for small mistakes to slip through the cracks. That's where code scanning comes in:

- 🕵️‍♂️ Finds hidden bugs and vulnerabilities
- 🧪 Helps prevent new issues from being introduced
- 📊 Gives developers instant feedback during pull requests
- 📈 Integrates into CI/CD pipelines for continuous security

By using code scanning, you’re not just fixing code — you're improving the overall health and safety of your project. 🛡️

## 🔍 Supported Languages and Tools

GitHub supports code scanning for many popular programming languages including:
- JavaScript / TypeScript
- Python
- Java
- C/C++
- C#
- Go
- Ruby
- Swift
- Kotlin
- And more!

You can also integrate third-party tools by uploading results in **SARIF format**.

## 🧰 How Does Code Scanning Work?

1. **Analysis**: CodeQL scans your repository for patterns that match known vulnerabilities.
2. **Alerts**: If an issue is found, an alert appears in the **Security tab** of your repo.
3. **Fixing**: You fix the issue in your code.
4. **Closing**: Once fixed, the alert is automatically closed.

> 📌 Tip: Code scanning runs automatically on every pull request — helping catch issues early!

## ✅ Prerequisites for Code Scanning

Before enabling code scanning, make sure your repo meets these requirements:

✅ Repository must be **private** (with GHAS license) or **public**  
✅ Must have **write permissions**  
✅ Must enable **GitHub Actions** (for default setup)  
✅ Must allow workflow files in `.github/workflows`  

## 🛠️ Step-by-Step: Enable Code Scanning

### Option 1: Use Default Setup (Recommended)

1. Go to your repo > **Security tab**
2. Click **Set up code scanning**
3. Choose **Default setup**
4. Select **Enable CodeQL**

GitHub will create a workflow file (`.github/workflows/codeql-analysis.yml`) and start scanning your code.

> 📝 This method requires no configuration — perfect for most projects.

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

## 🧩 Use SARIF Files for External Results

If you use external tools like SonarQube or Checkmarx, you can still upload their findings into GitHub using **SARIF files**.

### Steps to Upload SARIF:
1. Generate a SARIF file from your tool
2. Use GitHub’s `upload-sarif` action to submit it
3. View alerts in the **Security tab**

Example:
```yaml
- name: Upload SARIF file
  uses: github/codeql-action/upload-sarif@v2
  with:
    sarif-file: results.sarif
```

> 📦 This makes it easy to bring in findings from internal tools or other CI systems.

## 🧪 Review and Manage Code Scanning Alerts

All alerts appear in the **Security > Code scanning alerts** section of your repo.

From there, you can:
- Filter by severity (critical, high, medium, low)
- Sort by language or date
- Investigate the affected files
- Dismiss false positives

![Screenshot of code scanning alerts](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/code-scanning-alerts.png)

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
