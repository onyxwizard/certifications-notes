# 🔄 Domain 2 - Configure Dependabot Security Updates on Your GitHub Repo

Welcome to **Domain 2** of GitHub Advanced Security (GHAS)! 🚀  
In this guide, you'll learn how to **configure and manage Dependabot security updates** for your GitHub repositories. Dependabot helps keep your project secure by automatically updating dependencies and alerting you to known vulnerabilities.

Whether you're a developer, DevOps engineer, or part of a security team, mastering Dependabot will help you build safer software from the start. Let’s dive in! 🔐

## 🧠 What Is Dependabot?

**Dependabot** is an automated dependency management tool built into GitHub that helps you:
- Keep your project dependencies up-to-date
- Automatically detect and fix vulnerable packages
- Create pull requests to update outdated dependencies to secure versions

By integrating Dependabot into your workflow, you can reduce the risk of using outdated libraries with known security flaws. 💡

> 📌 Note: Dependabot uses the **Dependency Graph** and the **GitHub Advisory Database** to identify issues and suggest fixes.

## 🔍 Why Dependabot Matters

Modern applications rely heavily on third-party libraries and frameworks. Unfortunately, many of these dependencies may contain known vulnerabilities that attackers can exploit.

Here's why Dependabot is essential:
- ⚠️ Detects vulnerable dependencies early
- 🤖 Automates security patching
- 🛡 Reduces manual work and human error
- 🧩 Integrates directly into your GitHub workflow

## 🛠️ How Dependabot Works

Dependabot checks your dependencies regularly and performs two main functions:

### 1. **Dependabot Alerts**
- Notifies you when a vulnerability is found in your dependencies
- Displays alerts in the **Security tab** of your repository
- Includes links to affected files and fixed versions

### 2. **Dependabot Security Updates**
- Automatically creates pull requests to update vulnerable dependencies
- Merges changes after review and approval
- Helps maintain a secure and stable codebase

> 📦 Dependabot supports multiple ecosystems like `npm`, `pip`, `Maven`, `RubyGems`, and more!

## 📁 Prerequisites for Using Dependabot

Before enabling Dependabot, ensure your repo meets the following requirements:

✅ The repository must not be a **fork**  
✅ The repository must not be **archived**  
✅ Must have **write permissions**  
✅ Must enable the **dependency graph**  
✅ Must enable **Dependabot alerts**

Once these are set, you're ready to configure automatic security updates.

## 🔧 Step-by-Step: Enable Dependabot Security Updates

### Option 1: Enable via GitHub UI

1. Go to your repository's **main page**
2. Click **Settings**
3. Under **Security**, select **Code security and analysis**
4. Scroll down to **Dependabot security updates**
5. Click **Enable**

GitHub will now monitor your dependencies and open PRs when updates are available.

![Screenshot of enabling Dependabot security updates](https://learn.microsoft.com/en-us/training/github/configure-dependabot-security-updates-on-github-repo/media/dependabot-alerts.png)

### Option 2: Enable via `dependabot.yml`

To customize how Dependabot behaves, create a `.github/dependabot.yml` file.

#### Example Configuration:
```yaml
version: 2
updates:
  - package-ecosystem: "npm"
    directory: "/"
    schedule:
      interval: "daily"
```

This tells Dependabot to check for updates daily in your `npm` dependencies.

> 📝 You can define schedules, specific ecosystems, and even private registries.

## 🧪 Use Dependency Review (Optional)

You can also use the **Dependency Review GitHub Action** to analyze dependency changes in pull requests.

### To Add It:
1. Go to your repo > **Actions** tab
2. Search for **"Dependency Review"**
3. Select **Configure** and commit the workflow file

This adds a new check that runs whenever a PR includes dependency changes.

![Screenshot of finding the dependency review GitHub action](https://learn.microsoft.com/en-us/training/github/configure-dependabot-security-updates-on-github-repo/media/find-dependency-review-from-repo.png)

## 🧱 Grouped Security Updates (Optional)

Reduce the number of individual PRs by enabling **grouped security updates**.

When enabled, Dependabot opens one PR per ecosystem to update all vulnerable dependencies at once.

### To Enable:
1. Go to **Settings > Code security and analysis**
2. Enable **Grouped security updates**

> 🧩 Only applies to security updates — version updates are handled separately.

## 🛑 Dismissing or Resolving Alerts

Sometimes, you may want to dismiss an alert if:
- The vulnerability doesn’t apply to your use case
- A fix isn't available yet

### To Resolve an Alert:
1. Go to the **Security tab**
2. Select **Dependabot alerts**
3. Choose the alert you want to resolve
4. Either:
   - Merge the suggested PR
   - Manually update the dependency
   - Dismiss the alert with a reason

## 🧭 Custom Auto-Triage Rules

You can create custom rules to automatically dismiss or reopen alerts based on severity or other criteria.

### Example Rule:
- Dismiss low-severity alerts until a patch is available

### Steps:
1. Go to **Settings > Code security and analysis**
2. Click the gear icon next to **Dependabot alerts**
3. Select **New rule**
4. Define your conditions and actions

![Screenshot of new custom Dependabot rule](https://learn.microsoft.com/en-us/training/github/configure-dependabot-security-updates-on-github-repo/media/new-custom-dependabot-rule.png)

## 👥 Grant Access to Dependabot Alerts

Only users with **write**, **maintain**, or **admin** access can view Dependabot alerts. Repository owners and admins can grant additional users access through settings.

## 📈 Monitor and Maintain Security

Security is an ongoing process. Here’s how to stay on top of it:

✅ Regularly check your **Security tab**  
✅ Review and merge Dependabot PRs promptly  
✅ Use notifications to stay informed  
✅ Update your `dependabot.yml` as needed  
✅ Revisit dismissed alerts periodically  

> 📊 Tip: Set up scheduled scans and integrate with CI/CD pipelines for continuous protection.

## 🙌 Final Thoughts

Configuring Dependabot security updates ensures your project stays protected from known vulnerabilities without slowing down development.

From enabling alerts to automating updates and managing exceptions, Dependabot gives you powerful tools to maintain a secure codebase — all within GitHub.

So go ahead, turn on Dependabot, and let automation do the heavy lifting while you focus on building great software. 💻✨

## 📚 Want to Learn More?

Check out:
- [Dependabot Documentation](https://docs.github.com/en/code-security/dependabot)
- [Dependency Graph Overview](https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph)
- [Using Dependabot with Private Registries](https://docs.github.com/en/code-security/dependabot/working-with-dependabot/configuring-access-to-private-registries-for-dependabot)

## ✅ Exercise: Configure Dependabot Security Updates

Try what you've learned by completing a hands-on exercise:
- Enable Dependabot alerts and security updates
- Review and resolve a real vulnerability
- Configure grouped updates
- Customize behavior with `dependabot.yml`

This practice will reinforce your understanding and help you become a GHAS pro! 💪

