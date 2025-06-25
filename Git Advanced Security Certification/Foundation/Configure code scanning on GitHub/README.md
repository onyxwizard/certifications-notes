
# 🔍 GitHub Code Scanning: A Beginner’s Guide 🛡️

GitHub Code Scanning helps you find and fix security vulnerabilities and coding errors in your code — before they become real problems.

In this guide, we’ll walk through:
- ✅ What code scanning is
- 💡 How to set up **CodeQL analysis**
- 🧰 How to use **third-party tools with SARIF files**
- ⚙️ How to **configure and customize** code scanning
- 📊 Real-world examples and exercises

Let’s get started! 🚀

## 🧠 What Is Code Scanning?

**Code scanning** uses **CodeQL**, GitHub's powerful code analysis engine, to scan your repository and detect:
- 🔐 Security vulnerabilities
- 🐞 Coding errors
- 🧹 Potential performance issues

🔍 When a potential issue is found, GitHub shows an alert in the **Security tab** of your repository. Once you fix the problem, the alert closes automatically.

### Why Use Code Scanning?
- Find and fix issues early 🕵️‍♂️
- Prevent new vulnerabilities from being introduced 🛑
- Schedule scans or run them automatically on events like `push` or `pull_request` 🕒
- Works for both public and private repositories (with GitHub Advanced Security enabled) 🌐

## 🦁 About Code Scanning with CodeQL

**CodeQL** is GitHub’s custom query language that treats code like data. This lets you write queries to find patterns that indicate security flaws or bugs.

### Supported Languages:
- C/C++
- C#
- Go
- Java/Kotlin
- JavaScript/TypeScript
- Python
- Ruby
- Swift

### Three Ways to Set Up Code Scanning with CodeQL:

1. **Default Setup** – Quick and easy setup using GitHub Actions  
2. **Advanced Setup** – Generate and edit a workflow file directly in your repo  
3. **CLI Setup** – Run CodeQL outside GitHub and upload results manually

## 🛠️ Enable CodeQL in Your Repository (Default Setup)

Follow these steps to enable CodeQL using the default setup:

1. On GitHub.com, go to your repository’s main page.
2. Under your repo name, click the **Security** tab.
   ![Screenshot of the security tab.](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/2-security-tab-screenshot.png)
3. Click **Set up code scanning**.
   ![Screenshot of the set up code scanning button.](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/3-set-up-code-scanning-button-screenshot.png)
4. Select **Default** from the dropdown.
5. Review the default settings. You can click **Edit** to change how CodeQL runs.
6. Click **Enable CodeQL**.

✅ The default setup configures CodeQL to analyze your code every time:
- You push changes to any protected branches
- You open a pull request against the default branch

> 💡 Pro Tip: Code scanning runs as a GitHub Action, so be aware of your monthly minutes usage!

## 💸 Billing for GitHub Actions

Since CodeQL runs via GitHub Actions:
- Public repos: ✅ Free unlimited minutes
- Private repos: Minutes depend on your plan:
  - GitHub Free: 2,000 minutes/month
  - GitHub Pro / Team: 3,000 minutes/month
  - GitHub Enterprise: 50,000 minutes/month

You can control spending with **spending limits** to avoid unexpected charges.

## 🧪 Enable Code Scanning with Third-Party Tools

Sometimes, you want to use your own tools to scan code and then **upload the results to GitHub**.

### 🔁 Upload Results Using:
- 🔄 **Code Scanning API**
- 🧰 **CodeQL CLI**
- 🧩 **GitHub Actions**

#### 📄 SARIF Files
SARIF (**Static Analysis Results Interchange Format**) is the standard format used by many static analysis tools. GitHub accepts SARIF v2.1.0 files to show alerts in your repo.

##### Example: Upload SARIF File Using GitHub Actions
```yaml
name: "Upload SARIF"
on:
  push:
  schedule:
    - cron: '45 15 * * 4' # Runs every Thursday at 15:45 UTC

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      security-events: write
    steps:
      - uses: actions/checkout@v2
      - name: Upload SARIF file
        uses: github/codeql-action/upload-sarif@v1
        with:
          sarif_file: results.sarif
```

📌 **Note:** Max file size = 10 MB (gzip-compressed), max results = 5,000 per upload

## ⚙️ Configure Code Scanning

Once you've set up code scanning, you might want to **customize how often scans run**, what files are scanned, or even what severity levels block pull requests.

### Edit Workflow File
Workflow files live in `.github/workflows/`. To edit:
1. Click the **Edit** button on the workflow file.
   ![Screenshot of the Edit button](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/2-edit-button-screenshot.png)
2. Make your changes.
3. Commit the file.

### 🔁 Configure Scan Frequency

You can trigger scans:
- On every **push**
- On **pull request**
- On a **schedule**

Example:
```yaml
on:
  push:
    branches: [main]
  pull_request:
    branches: [main]
  schedule:
    - cron: '20 14 * * 1' # Every Monday at 14:20 UTC
```

### 🚫 Define Severity Levels That Block PRs

By default, only `Error`, `Critical`, or `High` severity issues block merges. You can change this:

1. Go to **Settings > Code security and analysis**
2. In **Protection rules**, select the severity level you want to enforce.

![Screenshot of the severity dropdown](https://learn.microsoft.com/en-us/training/github/configure-code-scanning/media/3-severities-4-level-severity-screenshot.png)

### 🚫 Avoid Unnecessary Pull Request Scans

You can skip scanning if only certain files are changed:

```yaml
on:
  pull_request:
    branches: [main]
    paths-ignore:
      - '**/*.md'
      - '**/*.txt'
```

This prevents unnecessary scans when documentation-only files are updated.

## 🧪 Exercise: Configure Code Scanning

Try editing a real CodeQL workflow file:
1. Open `.github/workflows/codeql-analysis.yml`
2. Change the scan schedule to run every Tuesday at 9 AM UTC
3. Add a path ignore rule for `.json` files
4. Commit your changes and watch it run!

## 🧾 Module Assessment: Check Your Knowledge

### 1. When code scanning is enabled, what is one default event that triggers a scan?
✅ **Pushing a change**

### 2. Which of the following are the tools used to upload a SARIF file?
✅ **GitHub Actions, the code scanning API, and the CodeQL CLI**

### 3. What is the difference between scheduled versus triggered events in code scanning?
✅ **Scheduled events run based on a specified schedule and triggered events run on code events such as a push.**

## 🎯 Summary

| Feature | Description |
|--------|-------------|
| **Code Scanning** | Detects security issues and bugs in your code |
| **CodeQL** | Powerful query engine for deep code analysis |
| **SARIF Files** | Standard format for uploading third-party scan results |
| **GitHub Actions** | Used to automate and schedule scans |
| **Severity Rules** | Control what issues block merges |
| **Customization** | Edit workflows to fit your team's needs |

## 📌 Next Steps

Want to dig deeper?
- [Configure CodeQL workflows](https://docs.github.com/en/code-security/code-scanning/automatically-scanning-your-code-for-vulnerabilities-and-errors/configuring-codeql-workflows)
- [Use GitHub Actions for CI/CD](https://docs.github.com/en/actions)
- [Explore GitHub Advanced Security features](https://github.com/features/security)

🎉 You’ve now learned how to secure your code using GitHub’s powerful **code scanning** features. Whether you're using **CodeQL**, **third-party tools**, or **customizing scan settings**, you're well on your way to writing safer, cleaner code!
