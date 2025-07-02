# 🛡️ Domain 8 - Manage Sensitive Data and Security Policies Within GitHub

Welcome to **Domain 8** of GitHub Advanced Security (GHAS)! 🚀  
In this guide, you’ll learn how to **secure sensitive data**, set up **security policies**, and respond to **security incidents** using built-in tools in GitHub.

Whether you're a developer, DevOps engineer, or part of a security team, mastering these practices will help you protect your codebase, enforce consistent standards, and ensure compliance with internal or regulatory requirements. Let’s dive in! 💻🔒

## 🧠 Why Managing Sensitive Data Matters

Accidentally committing secrets like API keys, passwords, or SSH keys can lead to serious breaches. That's why it's essential to:
- 🔐 Prevent sensitive data from being committed
- 🧹 Remove any that were already pushed
- 📜 Define clear policies for reporting vulnerabilities

GitHub provides powerful tools to help you do all this — and more!

## 🗑 Scrubbing Sensitive Data from Repositories

If you’ve ever committed a secret by mistake, it’s crucial to remove it completely — not just delete the file.

### ⚠️ Never assume old commits are safe!
Even if you delete a file in a new commit, the data still exists in Git history.

### ✅ Recommended Steps:
1. **Use `git filter-branch` or `BFG Repo-Cleaner`** to rewrite Git history
2. **Force push the cleaned version**
3. **Rotate any exposed credentials immediately**

> 📌 Tip: Always treat any accidentally committed secret as compromised — revoke and replace it right away!

For full instructions, see [Removing sensitive data from a repository](https://docs.github.com/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository)

## 📄 Communicate Your Security Policy with SECURITY.md

The `SECURITY.md` file is where you tell users how to responsibly report vulnerabilities in your project.

### 📝 What to Include:
- Supported versions of your software
- How to report security issues
- Contact details for maintainers
- Any legal disclaimers or known risks

Place this file in the root, `.github`, or `docs` folder of your repository.

> 📂 Example: [SECURITY.md example on GitHub](https://learn.microsoft.com/en-us/training/github/manage-sensitive-data-security-policies/media/security-md.png)

This helps speed up fixes and ensures responsible disclosure.

## 🛡 Use GitHub Security Advisories

GitHub Security Advisories let you:
- Privately discuss and fix security issues
- Coordinate patches with contributors
- Publicly disclose advisories after fixes are released

Once published, advisories appear in the **Common Vulnerabilities and Exposures (CVE)** list — helping notify others who may be affected.

> 📢 This feature makes it easier for your community to stay secure and updated.

## 🧩 Other Community Health Files

GitHub recognizes several key files that improve transparency and collaboration:

| File | Purpose |
|------|---------|
| `CODE_OF_CONDUCT.md` | Sets behavior expectations for contributors |
| `CONTRIBUTING.md` | Guides users on how to contribute |
| `FUNDING.yml` | Shows how to support the project financially |
| `GOVERNANCE.md` | Explains decision-making structure |

These files build trust and make your project more welcoming to contributors.

## 🔒 GitHub Enterprise Security Features

GitHub offers enterprise-grade features to help organizations meet compliance and security needs.

### ✅ Key Tools:
- **Code scanning (with CodeQL)**
- **Secret scanning**
- **Dependabot alerts and updates**
- **Security advisories**
- **Access control and rulesets**

### 📋 Compliance Reports:
- SOC 1 Type 2
- SOC 2 Type 2
- ISO/IEC 27001:2013

These certifications help satisfy audits and regulatory requirements.

## 🛡 Set Up Preventive Security Measures

Prevention is better than cure. Here’s how to stop sensitive data leaks before they happen:

### ✅ Best Practices:
- Use `.gitignore` to exclude sensitive files
- Enable **secret scanning** and **push protection**
- Enforce **branch protection rules**
- Require **2FA** for all organization members
- Automate checks via **GitHub Actions**

By setting these up early, you reduce risk across your entire development lifecycle.

## 📜 Documenting Security Policies

Clear documentation builds trust and improves response times during security incidents.

### 📄 Create a `SECURITY.md` file that includes:
- Supported versions of your project
- Reporting guidelines
- Severity levels and patch timelines

You can also define additional policies at the organization or enterprise level to enforce consistent settings across repositories.

## 🛠 Automate Security Processes

Automating security checks ensures consistency and reduces human error.

### 🤖 Examples:
- Automatically open issues when a vulnerability is found
- Block pushes containing secrets using **push protection**
- Notify teams when Dependabot finds outdated dependencies
- Run code scanning on every pull request

GitHub Actions and custom workflows make automation easy and scalable.

## 🧾 Responding to Sensitive Data Exposure

If a secret or vulnerability is exposed:
1. Treat it as compromised
2. Revoke the secret or patch the vulnerability
3. Update affected systems
4. Delete the old data from your repo
5. Close the alert in GitHub

GitHub often notifies service providers automatically, so they can take action too.

## 📋 Export Audit Logs and Git Events

Audit logs track important actions like:
- User access changes
- Repository deletions
- Secret scanning alerts
- Dependency updates

You can export these logs for:
- Internal audits
- Regulatory compliance
- Incident investigations

Go to **Organization Settings > Audit log** and download events for analysis.

## 🎯 Setting Security Policies

Setting clear security policies helps everyone follow best practices and ensures consistent enforcement.

### 🧱 At the Organization Level:
- Enable GHAS features across all repos
- Set default branch protections
- Define CODEOWNERS and review requirements

### 🏢 At the Enterprise Level:
- Enforce security settings globally
- Control access with SCIM and SAML SSO
- Monitor compliance centrally

GitHub gives you fine-grained control over who does what — making it easier to maintain a secure environment.

## 👥 Why Security Policies Matter

Security policies keep your ecosystem safe by:
- Guiding workflows with standardized processes
- Ensuring proper access controls
- Making vulnerability reporting easy and consistent
- Reducing the risk of misconfigurations

> 🧭 Think of them as guardrails — guiding developers toward secure practices without slowing them down.

## 🧪 Module Assessment

### Question 1:
**What file should you use to create documentation for collaborators that lists supported versions of the project?**
- ❌ CONTRIBUTING.md  
- ❌ SUPPORT.md  
- ✅ SECURITY.md  

### Question 2:
**Which tool should you use to automate part of your security process?**
- ✅ Add Dependabot to your code base  
- ❌ Add access restrictions to your enterprise  
- ❌ Create security documentation  

### Question 3:
**Which two pieces of information should be included in a security advisory?**
- ✅ Product affected and severity  
- ❌ Severity and exposure list  
- ❌ Administrator name and severity  

## 🙌 Final Thoughts

Managing sensitive data and defining strong security policies isn’t just about preventing mistakes — it’s about building a culture of security within your team.

From removing secrets to setting policies and automating responses, GitHub gives you the tools to make security part of your everyday workflow.

Start today by adding a `SECURITY.md` file, enabling secret scanning, and automating your security checks. And don’t forget to train your team so everyone understands their role in keeping your code safe.

Stay secure! 🔐✨

## 📚 Want to Learn More?

Check out:
- [Adding a Security Policy](https://docs.github.com/code-security/getting-started/adding-a-security-policy-to-your-repository)
- [GitHub Security Features Overview](https://docs.github.com/code-security/getting-started/github-security-features)
- [GitHub Security Advisories](https://docs.github.com/en/code-security/security-advisories)

## ✅ Exercise: Set Up Security Policies

Try what you've learned by completing a hands-on exercise:
- Create a `SECURITY.md` file
- Enable secret scanning and push protection
- Set up Dependabot alerts
- Generate and resolve a security advisory
- Export audit logs for review

This practice will reinforce your understanding and help you become a GHAS pro! 💪

Ready to secure your GitHub projects? Start managing sensitive data and setting policies today! 🔍🚀
