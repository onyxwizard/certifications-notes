# 🔐 Domain 3 - Configure and Use Secret Scanning in Your GitHub Repository

Welcome to **Domain 3** of GitHub Advanced Security (GHAS)! 🚀  
In this guide, you’ll learn how to **configure and use secret scanning** — a powerful feature that helps detect and prevent accidental exposure of sensitive information like API keys, tokens, and passwords in your GitHub repositories.

Whether you're a developer, DevOps engineer, or part of a security team, mastering secret scanning is essential for maintaining secure code practices. Let’s dive in! 💻🔒

## 🧠 What Is Secret Scanning?

Secret scanning is an automated feature in GitHub that scans your repositories for **sensitive information**, such as:

- 🔑 API keys
- 🗝 Personal access tokens
- 📦 SSH keys
- 🖥 OAuth tokens

If any secrets are found, GitHub generates **alerts** and notifies repository administrators so they can take action before the secrets are misused.

> 💡 Think of secret scanning as a safety net that catches sensitive data before it becomes a security risk!

## 🔍 How Does Secret Scanning Work?

GitHub scans your entire Git history across all branches for known secret patterns provided by GitHub and its partners. It also checks:

- 📄 Source code files
- 📩 Issue descriptions and comments
- 📤 Pull request titles and descriptions
- 💬 Discussion threads

When a secret is detected:
1. An alert is created in the **Security tab**
2. The service provider (if partnered with GitHub) is notified
3. You receive guidance on how to revoke and replace the secret

## 🛠️ Step-by-Step: Enable Secret Scanning for a Repository

### 1. Go to Repository Settings
1. Open your repo on GitHub
2. Click **Settings** in the top menu

### 2. Navigate to Advanced Security
1. In the left sidebar, click **Advanced Security**
2. Look for **Secret Protection**

### 3. Enable Secret Scanning
1. Click the **Enable** button next to **Secret Protection**
2. Confirm by clicking **Enable Secret Protection**

> 📌 Note: If you see a **Disable** button, it means secret scanning was already enabled at the organization level.

### 4. Enable Push Protection (Optional but Recommended)
1. Scroll down and click **Enable** next to **Push protection**
2. This prevents secrets from being pushed accidentally

![Screenshot of secret scanning enabled in repository settings](https://learn.microsoft.com/en-us/training/github/configure-use-secret-scanning-github-repository/media/enable-secret-scanning-repo-settings.png)

## 🏢 Enable Secret Scanning for an Organization

To enable secret scanning across all private repositories in your organization:

1. Go to **Organization Settings**
2. Select **Advanced Security**
3. Enable **Secret Scanning** for all repositories
4. Optionally enable **Push protection** at the organization level

This ensures consistent protection across all teams and projects.

## 🧹 Exclude Files from Secret Scanning

Sometimes, test files or dummy data may trigger false alerts. To exclude them:

1. Create a `.github/secret_scanning.yml` file
2. Add paths to ignore using `paths-ignore`

Example:
```yaml
paths-ignore:
  - "test/secrets/*.js"
  - "**/sample-keys/**"
```

> ⚠️ Limits:
- Up to 1,000 entries in `paths-ignore`
- File size must be under 1 MB

## 📣 Manage Who Gets Secret Scanning Alerts

Only users with **write, maintain, or admin** access to the repo can view secret scanning alerts. You can grant additional users access:

1. Go to **Settings > Advanced Security**
2. Under **Access to alerts**, search for people or teams
3. Click **Save changes**

![Screenshot of Access to alerts section](https://learn.microsoft.com/en-us/training/github/configure-use-secret-scanning-github-repository/media/access-to-alerts.png)

## 🧾 Review and Respond to Secret Scanning Alerts

### 1. View Alerts
Go to **Security > Secret scanning** to see all detected secrets.

You can filter by:
- 🔍 Secret type
- 🟡 Validity
- 🧹 Bypassed status
- 🪙 Provider

![Screenshot of secret type filter in secret scanning alerts](https://learn.microsoft.com/en-us/training/github/configure-use-secret-scanning-github-repository/media/secret-scanning-alerts-filter-secret-type.png)

### 2. Take Action
When a secret is found:
- Consider it compromised ✅
- Revoke the old secret ❌
- Generate a new one ✨
- Update any services using the old secret 🔄
- Delete the old secret from the repository 🗑️

After fixing, close the alert with a reason:
- Revoked and no longer in use
- False positive
- Already rotated

![Screenshot of closing a secret scanning alert](https://learn.microsoft.com/en-us/training/github/configure-use-secret-scanning-github-repository/media/alert-close-reason.png)

## 🎯 Create Custom Secret Patterns (Advanced)

For internal secrets not covered by default patterns, you can define custom regex patterns.

### Steps to Create a Custom Pattern:
1. Go to **Settings > Advanced Security**
2. Under **Secret Protection**, click **New pattern**
3. Enter:
   - Pattern name
   - Regex pattern (using Hyperscan syntax)
   - Optional: sample string for testing
4. Click **Save and dry run** to test without triggering alerts
5. Review results and adjust if needed
6. When ready, click **Publish pattern**

![Screenshot of creating a new custom pattern](https://learn.microsoft.com/en-us/training/github/configure-use-secret-scanning-github-repository/media/new-custom-pattern-octocat.png)

## 🛡️ Understand Push Protection

Push protection stops secrets from being committed in the first place.

- 🔍 Scans every push for supported secrets
- ⚠️ Blocks the push if a secret is detected
- 📱 Prompts contributors with remediation steps

Push protection is **on by default** for public repositories. For private repos with GHAS, you can enable it manually.

## 🧪 Exercise: Scan for Secrets and Prevent Leaks

Try what you've learned by completing a hands-on exercise:
- Enable secret scanning and push protection
- Trigger a fake secret leak
- Review and resolve the alert
- Set up custom patterns for internal secrets

This practice will help reinforce your understanding and build real-world skills. 💪

## 📢 Notify Service Providers Automatically

When a secret is found, GitHub automatically notifies the issuing service provider (if they’re a GitHub partner). They may:
- Revoke the secret 🔒
- Issue a new one 🔄
- Contact you directly 📞

This adds an extra layer of protection beyond just alerting you.

## 🧩 Who Can Use Secret Scanning?

| Type of Repo | Secret Scanning Available? | Notes |
|--------------|-----------------------------|-------|
| Public Repos | ✅ Yes | Enabled by default |
| Private Repos | ✅ Yes (with GHAS license) | Must be enabled manually |
| Enterprise Orgs | ✅ Yes | Can configure globally |

> 📌 Tip: Secret scanning **cannot be configured or turned off** in public repos. To manage settings, switch to a private repo with GHAS.

## 🙌 Final Thoughts

Secret scanning is a critical tool in your security arsenal. By detecting and preventing accidental exposure of credentials early in development, you reduce the risk of breaches and protect both your code and your organization.

Start today by enabling secret scanning, reviewing alerts, and configuring push protection. And don’t forget to teach your team about the importance of keeping secrets out of source control!

Stay secure! 🔐✨

## ✅ Module Assessment

### Question 1:
**What do you need to do if you want to change the settings for secret scanning on a public repository?**
- ❌ Enable secret scanning on the repository
- ✅ Switch the repository to a private one with GitHub Advanced Security
- ❌ Get admin permissions on the repository

### Question 2:
**Where can you configure the recipients of secret scanning alerts?**
- ❌ In the Watch settings of a repository
- ✅ In the Advanced Security settings of a repository
- ❌ In the Manage Access settings of a repository

### Question 3:
**Can secret scanning be disabled on public repositories?**
- ❌ Yes, anytime
- ✅ No, it's always enabled
- ❌ Only by GitHub support
