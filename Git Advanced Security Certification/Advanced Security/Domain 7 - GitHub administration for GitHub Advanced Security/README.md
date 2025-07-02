# 🛡️ Domain 7 - GitHub Administration for GitHub Advanced Security

Welcome to **Domain 7** of GitHub Advanced Security (GHAS)! 🚀  
In this guide, you'll learn how to **administer and manage GitHub Advanced Security at the organization and enterprise levels**. Whether you're a DevOps engineer, security professional, or part of an enterprise team, mastering GHAS administration will help you secure your codebase and enforce policies across your teams.

Let’s dive in! 💻🔐

## 🧠 What Is GitHub Advanced Security (GHAS)?

GitHub Advanced Security (GHAS) is a suite of tools that helps organizations detect and fix security vulnerabilities in their codebases early in the development lifecycle.

### ✅ Key Features:
- 🔍 **Code Scanning**: Detects coding errors and vulnerabilities
- 🕵️ **Secret Scanning**: Prevents accidental exposure of sensitive data
- 🔄 **Dependabot Alerts & Updates**: Keeps dependencies up-to-date and secure
- 📊 **Security Overview**: Provides centralized visibility into security risks

> 💡 These features are available by default on public repositories — but require a **GHAS license** for use on private and internal repositories.

## 🏢 Enable GHAS for Organizations and Enterprises

To enable GHAS features across your organization or enterprise:

1. Go to **Organization Settings > Code security and analysis**
2. Click **Enable all** next to the feature you want to activate
3. Optionally check **Automatically enable for new repositories**
4. Click **Enable FEATURE**

This ensures all current and future repositories benefit from advanced security protections.

![Screenshot of enabling GHAS for all repositories](https://learn.microsoft.com/en-us/training/github/github-administration-github-advanced-security/media/enable-org.png)

## ⚙️ Enable GHAS on GitHub Enterprise Server

For self-hosted environments like GitHub Enterprise Server:

### Prerequisites:
- Valid GHAS license
- Upgraded GitHub Enterprise Server with GHAS support
- Met prerequisites for each feature (code scanning, secret scanning, Dependabot)

### Steps:
1. Log in to your GitHub Enterprise Server admin console
2. Navigate to **Admin Center > Advanced Security**
3. Toggle on features: Code Scanning, Secret Scanning, Dependabot
4. Save settings and wait for configuration to complete

You can also enable via the administrative shell if needed.

## 👥 Manage Access to Security Alerts

Only users with sufficient permissions should view and act on security alerts.

| Alert Type | Required Permission |
|------------|---------------------|
| Code Scanning | Write access |
| Secret Scanning | Repository administrator or org owner |

You can grant additional users or teams access under:
**Settings > Security > Advanced Security > Access to alerts**

![Screenshot of managing alert access](https://learn.microsoft.com/en-us/training/github/github-administration-github-advanced-security/media/security-policy-org.png)

## 📜 Set a Security Policy at the Organization Level

A strong security policy ensures consistent usage of GHAS features across your organization.

### Steps:
1. Go to **Enterprise Settings > Policies > Advanced Security**
2. Choose whether to allow all org admins to configure GHAS or restrict it
3. Apply policies to all or selected organizations

This helps enforce compliance and reduce misconfigurations.

## 📂 Set a Security Policy at the Repository Level

Each project should have a documented way to report vulnerabilities.

### Steps:
1. Go to your repo > **Security > Security policy**
2. Click **Start setup**
3. Create a `SECURITY.md` file with:
   - Supported versions
   - Reporting guidelines
   - Contact details
4. Commit the file to your repo’s root, `.github`, or `docs` folder

This makes it easy for contributors to responsibly disclose issues.

## 📊 Use the Security Overview

The **Security tab** provides a centralized dashboard for monitoring security health across your organization or repository.

### Features:
- View active alerts (code scanning, secret scanning, Dependabot)
- Filter by severity, type, and date
- Track remediation progress
- Identify risky repositories needing attention

![Screenshot of Security Overview at the organization level](https://learn.microsoft.com/en-us/training/github/github-administration-github-advanced-security/media/security-overview.png)

This is especially useful when rolling out GHAS to large teams or enterprises.

## 🤖 Use the GitHub Advanced Security API Endpoints

GHAS offers REST API endpoints to automate management tasks such as:

- Listing security alerts
- Updating alert states
- Enabling/disabling features programmatically

Use these APIs in scripts or dashboards to monitor and manage security posture at scale.

> 📌 Example: Automate weekly reports of open alerts across all repos in your org.

## 🧩 Integrate GHAS into Your Software Development Lifecycle

GHAS isn’t just a tool — it’s a **security strategy** that integrates into every phase of development.

### How GHAS Helps Across the SDLC:
- **Plan**: Define security policies and access controls
- **Write**: Use secret scanning to prevent credential leaks
- **Build**: Run code scanning to catch bugs early
- **Test**: Review Dependabot alerts for outdated dependencies
- **Deploy**: Monitor for ongoing risks using Security Overview
- **Maintain**: Use advisories to responsibly disclose and fix issues

This proactive approach reduces technical debt and improves overall code quality.

## 🧪 Module Assessment

### Question 1:
**Which GHAS feature isn't available on public repositories?**
- ❌ Secret scanning  
- ✅ Security Overview  
- ❌ Code scanning  

### Question 2:
**Where can you enable GHAS for all private/internal repositories in an organization?**
- ❌ Site admin page of enterprise account  
- ❌ Organization's Security tab  
- ✅ Organization's Code and security settings  

### Question 3:
**How do you ensure everyone uses GHAS correctly?**
- ❌ Give write access to all users  
- ❌ Add SECURITY.md to personal repos  
- ✅ Set a security policy at the organization level  

## 🙌 Final Thoughts

GitHub Advanced Security gives administrators powerful tools to **secure code, enforce policies, and respond to threats quickly**. From enabling features at scale to managing access and setting documentation standards, GHAS becomes an essential part of any modern software development workflow.

By applying what you’ve learned in this domain, you’re not just securing code — you’re building a safer, more resilient development culture.

Stay secure! 🔐✨

## 📚 Want to Learn More?

Check out:
- [GitHub Advanced Security Documentation](https://docs.github.com/en/code-security)
- [Enabling GHAS for Enterprise Cloud](https://docs.github.com/en/enterprise-cloud@latest/admin/advanced-security/enabling-github-advanced-security-for-your-enterprise)
- [Managing GHAS Features via API](https://docs.github.com/en/rest/code-scanning)

## ✅ Exercise: Configure GHAS for Your Organization

Try what you've learned by completing a hands-on exercise:
- Enable GHAS features for an organization
- Set up a security policy
- Configure access to alerts
- Generate and review security advisories

This practice will reinforce your understanding and help you become a GHAS pro! 💪

Ready to take control of your GitHub security? Start administering GHAS today! 🚀🔒
