# 🌐 Introduction to GitHub Administration

Welcome! 👋 This guide will help you understand the **basics of GitHub administration** — from managing teams and organizations to securing access and setting up permissions. Whether you're a new admin or just looking to improve your skills, this document has got you covered!

Let’s dive into how GitHub is structured and how you can manage it like a pro. 🚀

## 🧑‍💼 GitHub Administration at the Team Level

Teams in GitHub are groups of users who collaborate on repositories together. You can organize your team members based on roles, departments, or projects.

### 🔒 Key Features:
- Create **nested teams** to reflect your company's structure.
- Sync teams with **identity providers (IdP)** like Microsoft Entra ID for automatic updates.
- Assign roles like **Team Maintainer** or **Admin** to control what people can do.

### 🛠 What Can Team Admins Do?
- Create, rename, or delete teams
- Add/remove members or sync with IdP groups
- Manage code reviews and reminders
- Set visibility and profile pictures for teams

> ✅ Tip: Use nested teams to simplify permissions and make collaboration easier across departments or skill sets like JavaScript, data science, etc.

## 🏢 GitHub Administration at the Organization Level

Organizations are shared spaces where multiple teams and users work together. As an **Organization Owner**, you have full control over settings, security, billing, and more.

### 📌 Roles & Responsibilities:
- Invite or remove members
- Organize into teams
- Grant repository permissions
- Set up organization-wide **security policies**
- Manage billing and custom scripts

> ⚠️ Recommendation: Try to keep all your repositories under **one organization** unless you have a specific reason not to. Managing multiple organizations increases complexity and cost.

## 🏰 GitHub Administration at the Enterprise Level

Enterprise accounts allow you to centrally manage **multiple organizations**. This is ideal for large companies that need to enforce policies across many teams and repositories.

### 🎯 Enterprise-Level Capabilities:
- Enable **SAML Single Sign-On (SSO)**
- Add/remove organizations
- Set enterprise-wide **repository and team policies**
- Manage **billing and security settings**
- Automate tasks using **APIs or scripts**

> 🔄 Synchronization: Just like with teams, you can sync enterprise-level identities with your IdP for seamless access control.

## 🔐 How Does GitHub Authentication Work?

Authentication is how users prove their identity when accessing GitHub. Let’s look at the most common methods:

### 1. 🧾 Username & Password (Not Recommended)
Basic authentication is risky. Avoid using it for sensitive actions.

### 2. 🔑 Personal Access Tokens (PATs)
Better than passwords. Used for API access or command-line interactions.

### 3. 🛡 SSH Keys
Secure way to authenticate without typing your password every time. Great for developers working with Git via the terminal.

### 4. 🗝 Deploy Keys
SSH keys tied directly to a single repository. Usually read-only but can be configured for write access.

### 🔐 Additional Security Options

#### 📲 Two-Factor Authentication (2FA)
Adds a second layer of protection. Users must enter a code from an app or SMS after logging in.

#### 🔄 SAML SSO
Allows centralized login through your identity provider (like Okta, OneLogin, or Microsoft Entra ID).

#### 📁 LDAP (for GitHub Enterprise Server)
Integrates with directory services like Active Directory for user management.

> 🔐 Best Practice: Always require **2FA** for all members, especially in organizations handling sensitive code.

## 🛡️ GitHub Permissions Overview

GitHub uses a **hierarchical permission model** that includes:

- **Repository-level permissions**
- **Team-level permissions**
- **Organization-level permissions**
- **Enterprise-level permissions**

Each level builds upon the last, giving admins fine-grained control over access and responsibilities.

## 📁 Repository Permission Levels

| Level | Description |
|-------|-------------|
| **Read** | View and comment on issues/PRs, clone repo |
| **Triage** | Manage issues and PRs but can't push changes |
| **Write** | Push changes, manage issues, and PRs |
| **Maintain** | Manage repository settings but not delete it |
| **Admin** | Full control including deletion and transfer |

> 📌 Tip: Follow the **Principle of Least Privilege** – give only the access needed to do the job.

## 👥 Team Permission Levels

| Role | What They Can Do |
|------|------------------|
| **Member** | Same as org members |
| **Maintainer** | Manage team settings, add/remove members, assign reviews |

> 🧩 Nested Teams: Parent teams pass permissions down to child teams — great for hierarchical structures.

## 🏛 Organization Permission Levels

| Role | Responsibility |
|------|----------------|
| **Owner** | Full control over org, including adding/removing members |
| **Member** | Default access depends on org settings |
| **Moderator** | Manage comments and contributors in public repos |
| **Billing Manager** | Handle billing info |
| **Security Manager** | Manage org-wide security settings |

## 🏢 Enterprise Permission Levels

| Role | Responsibility |
|------|----------------|
| **Owner** | Full control over all orgs and settings |
| **Member** | Same as org members |
| **Billing Manager** | Manage billing |
| **Guest Collaborator** | Limited access (Enterprise Managed Users only) |

## 🧭 Managing Access Across Organizations

When managing **multiple organizations**, consider:

- Using **single sign-on (SSO)** for consistent access
- Setting **default permissions** (read vs write)
- Using **Active Directory (AD) synchronization** for team management
- Writing **scripts** or using **GitHub Actions** for automation

## 🧱 Single vs Multiple Organizations

| Option | Pros | Cons |
|--------|------|------|
| **Single Org** | Easier to manage, consistent rules | Less flexibility |
| **Multiple Orgs** | Custom policies per team | More complex setup |

> 🧠 Recommendation: Start with one organization and expand only if needed.

## 📊 Monitoring & Auditing Access

Keep your GitHub environment secure by regularly checking who has access:

- Use **Settings > Manage Access** to view collaborators
- Check the **Audit Log** for access changes
- Use **GitHub APIs** to automate access checks

## 📈 Best Practices Summary

✅ Use teams and nested structures  
✅ Require 2FA for all users  
✅ Use PATs or SSH keys instead of passwords  
✅ Follow the Principle of Least Privilege  
✅ Regularly audit access and permissions  
✅ Automate where possible with scripts or GitHub Actions  
✅ Integrate with your IdP for centralized identity management  

## 📂 Visual References

Here are some screenshots from the original content to help visualize key areas:

- [Team Management](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/teams.png)
- [Personal Access Token Screen](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/personal-access-token.png)
- [Two-Factor Authentication](https://learn.microsoft.com/en-us/training/github/github-introduction-administration/media/2-factor-authentication.png)

## 🙌 Final Thoughts

GitHub administration isn’t just about setting things up — it’s about maintaining a secure, efficient, and collaborative environment for your teams. Whether you're managing a small group or a large enterprise, these tools and practices will help you succeed.

Start simple, stay organized, and always prioritize security. 🔐

## 📚 Want to Learn More?

Check out:
- [GitHub Documentation](https://docs.github.com/)
- [GitHub Learning Lab](https://lab.github.com/)
- [GitHub Actions](https://github.com/features/actions)

Happy administering! 🎉✨
