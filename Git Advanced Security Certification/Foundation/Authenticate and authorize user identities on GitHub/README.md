# 🔐 Authenticate and Authorize User Identities on GitHub

Welcome! 👋 This guide will help you understand how to **authenticate and authorize user identities** using GitHub, especially in enterprise environments. Whether you're managing a small team or an entire organization, secure identity management is crucial for protecting your codebase and collaboration tools.

Let’s dive into the modern authentication methods, SAML SSO setup, two-factor authentication (2FA), SCIM integration, and more! 🚀

## 🧑‍💼 What Is Identity Authentication?

Authentication is how users prove their identity when accessing GitHub. It's the first step in ensuring that only the right people can access your repositories, issues, and other resources.

### 🛡️ Why It Matters:
- Prevent unauthorized access
- Reduce phishing and credential theft
- Improve security while maintaining usability

## 🔐 Modern Authentication Methods in GitHub Enterprise

GitHub supports several advanced authentication methods to keep your systems secure:

### 1. 🗝 Passkeys & WebAuthn
- Use physical devices like YubiKeys or biometric logins (fingerprint, facial recognition)
- Eliminate passwords with phishing-resistant login methods
- Great for high-security environments

### 2. 📱 GitHub Mobile for 2FA
- Get push notifications for quick approval
- Secure without slowing down developers
- Works even without internet access

### 3. 🔁 OAuth and GitHub Apps
- OAuth apps use GitHub’s OAuth flow for secure external app access
- GitHub Apps authenticate as installations with granular permissions
- Ideal for CI/CD pipelines and automation workflows

### 4. 🏢 Enterprise Managed Users (EMU)
- All authentication happens through your Identity Provider (IdP)
- No self-managed accounts — full control from your IdP
- Enforces centralized policies and session management

> 💡 Tip: Always prefer passwordless methods like passkeys or hardware tokens for the strongest security!

## 🔄 SAML Single Sign-On (SSO)

SAML SSO links your IdP (like Microsoft Entra ID, Okta, or OneLogin) with GitHub, allowing users to sign in once and access all authorized GitHub resources.

### 🔒 Key Benefits:
- Centralized identity verification
- Reduced risk of weak or reused passwords
- Easy compliance with enterprise policies

### 🧩 Supported IdPs:
- Microsoft Entra ID
- Okta
- OneLogin
- PingOne
- Shibboleth
- Google Workspace

> 📌 Note: GitHub provides limited support for any IdP implementing SAML 2.0.

## 🧭 Configuring SAML SSO

You can configure SAML SSO at either the **organization level** or **enterprise level**, depending on your needs.

### Organization-Level Setup:
1. Go to **Your organizations > Settings > Security**
2. Input your IdP’s SAML URL and certificate
3. Test and save configuration
4. Enable **Require SAML SSO** to enforce it

### Enterprise-Level Setup:
1. Go to **Your enterprises > Settings > Security**
2. Configure SAML with your IdP details
3. Enforce across all organizations in the enterprise

> ⚠️ When enforcing SAML, noncompliant users are removed automatically from the org but remain in the enterprise until next access.

![Screenshot of SAML SSO requirement](https://learn.microsoft.com/en-us/training/github/authenticate-authorize-user-identities-github/media/require-saml-sso-authentication.png)

## 🔐 Two-Factor Authentication (2FA)

2FA adds an extra layer of security by requiring a second form of identification beyond just a username and password.

### ✅ Enforcing 2FA:
1. Go to **Security settings** in your organization
2. Check **Require two-factor authentication**
3. Notify users in advance to avoid disruptions

> ⚠️ Warning: Enabling 2FA removes non-compliant accounts, including bot accounts.

### 📲 2FA Methods:
| Method | Description |
|-------|-------------|
| **Security Keys** | Most secure — hardware-based, phishing-resistant |
| **TOTP Apps** | Time-based codes (e.g., Google Authenticator) |
| **SMS** | Least secure — use only if TOTP isn’t viable |

> 📷 [Time-based one-time password example](https://learn.microsoft.com/en-us/training/github/authenticate-authorize-user-identities-github/media/two-factor-identification-totp-example.png)  
> 📷 [SMS code example](https://learn.microsoft.com/en-us/training/github/authenticate-authorize-user-identities-github/media/two-factor-authentication-sms-six-digit-code-example.png)

## 🔐 Auditing 2FA Compliance

To check who has 2FA enabled:
1. Go to **Your organizations > People tab**
2. Filter by **2FA**

From here, identify and follow up with noncompliant users via email or internal messaging.

## 🔁 Automating Authorization with SCIM

SCIM (System for Cross-domain Identity Management) automates provisioning and deprovisioning of GitHub users and groups based on your IdP.

### 🎯 Benefits:
- Auto-create and update users
- Remove access instantly when someone leaves
- Revoke stale tokens after session ends

### 📦 Supported Providers:
- Okta
- Microsoft Entra ID
- OneLogin
- Ping Identity
- Google Workspace

### 🛠 Example SCIM Request:
```json
POST /scim/v2/Users
Content-Type: application/json
{
  "userName": "jdoe",
  "name": {
    "givenName": "John",
    "familyName": "Doe"
  },
  "emails": [
    {
      "value": "jdoe@example.com",
      "primary": true
    }
  ]
}
```

## 🔄 SCIM vs Manual User Management

| Feature | SCIM-Based | Manual |
|--------|------------|--------|
| Provisioning | Automated | Manual steps |
| Updates | Synced in real-time | Risk of inconsistencies |
| Deprovisioning | Instant removal | Delayed or missed |
| Scalability | Scales easily | Cumbersome at scale |
| Compliance | Easier to audit | Harder to track |

## 🔗 Connecting Your IdP to GitHub

You can use either a **supported IdP** or bring your own SAML 2.0 IdP.

### 🛠 Integration Steps:
#### For Paved Path IdPs:
1. Navigate to enterprise security settings
2. Select your IdP
3. Follow guided setup instructions

#### For Custom IdPs:
1. Go to security settings
2. Choose custom IdP
3. Enter SAML metadata
4. Validate connection

> 📊 Comparison Table:
| Feature | Paved Path | Bring Your Own IdP |
|--------|------------|---------------------|
| Setup | Guided | Manual |
| Flexibility | Limited | Full |
| Maintenance | GitHub-managed | Self-managed |
| Customization | Minimal | Full |
| Support | GitHub-supported | Self-supported |

## 👥 Managing Identities and Access

Ensure every user is authenticated and authorized correctly:

### 🔐 Credential Management:
- Link SSH keys and PATs to IdP identities
- Audit sessions regularly
- Revoke expired or unused credentials

### 👁 Auditing SAML Sessions:
- View active sessions in settings
- Revoke individual sessions as needed

## 🤝 Team Synchronization

If your company uses Microsoft Entra ID or Okta, you can sync GitHub teams with IdP groups automatically.

### 🔄 Features:
- Sync users between IdP groups and GitHub teams
- Map custom group names using `syncmap.yml`
- Dynamic configuration via `settings` file

> ⚠️ To use team sync, ensure SAML SSO and SCIM are both enabled.

## 🧑‍🤝‍🧑 Team Sync vs Group SCIM

| Feature | Team Sync | Group SCIM |
|--------|-----------|------------|
| Focus | Team-level mapping | User and group lifecycle |
| Automation | Syncs group membership only | Full automation |
| Ideal Use | GitHub Teams management | Large orgs with high turnover |
| Deprovisioning | Manual or IdP-dependent | Fully automated |
| Identity Model | Classic | Managed Users |

## 📈 Choosing the Right Approach

| Use Case | Recommended Solution |
|----------|----------------------|
| Manage repo access by teams | Team Sync |
| Automate user lifecycle | Group SCIM |
| Full IdP-based governance | Group SCIM |
| GitHub Teams is core to workflow | Team Sync |

## 📉 Usage Limits for Team Sync

Be aware of these limits when using team synchronization:
- Max members per team: **5,000**
- Max members per organization: **10,000**
- Max teams per organization: **1,500**

Exceeding these may cause performance issues or sync failures.

## 🧪 Module Assessment

### Question 1:
**What type of user authentication verifies identity against a known identity provider?**
- ❌ Two-factor authentication (2FA)
- ❌ Time-based One-time Password (TOTP)
- ✅ SAML Single Sign-on (SAML SSO)
- ❌ Short Message Service (SMS)

### Question 2:
**You're an admin and want to enable team synchronization for your organization. What installation permissions do you need to configure team synchronization for Microsoft Entra ID?**
- ❌ Provide tenant URL
- ✅ Read all users' full profiles
- ❌ Generate SSWS token
- ❌ Enable SAML SSO

### Question 3:
**Where does a user authenticate after enabling SAML SSO?**
- ❌ With GitHub login
- ❌ With organization credentials
- ✅ With the Identity Provider (IdP)

### Question 4:
**What two-factor authentication method supports the secure backup of your authentication codes in the cloud?**
- ✅ Time-based One-time Password (TOTP)
- ❌ SMS
- ❌ Security Key

## 📚 Want to Learn More?

Check out these resources:
- [GitHub Authentication Docs](https://docs.github.com/authentication)
- [GitHub Enterprise Cloud Getting Started](https://docs.github.com/get-started/onboarding/getting-started-with-github-enterprise-cloud)
- [SCIM API Documentation](https://docs.github.com/scim)

## 🙌 Final Thoughts

Securing user identities on GitHub is about more than just passwords — it's about building a system where authentication is seamless, authorization is controlled, and access is always verified.

Start with SAML SSO, enforce 2FA, automate with SCIM, and simplify team management with team synchronization.

Happy securing! 🔐✨
