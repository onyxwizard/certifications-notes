

# 🧪 GitHub Codespaces: Customize & Manage Your Dev Environment

GitHub Codespaces provides a **cloud-based development environment** that allows you to code, build, test, and deploy directly from your browser — with all the tools and extensions you need at your fingertips.

In this module, you'll learn how to:
- 🛠️ Customize your Codespace with **extensions and plugins**
- 🔁 Understand the **Codespace lifecycle**
- 💾 Save and persist your changes
- ❓ Test your knowledge with assessment questions



## 🛠️ Customize Your Codespace with Extensions or Plugins

You can enhance your development experience by installing **plugins and extensions** inside your Codespace. Whether you're using **VS Code (in-browser or desktop)** or **JetBrains IDEs**, you can tailor your workspace to suit your needs.

### ✅ For VS Code Users

1. Open the **Extensions panel** (`Ctrl+Shift+X` or click the puzzle icon).
2. Search for your favorite extension.
3. Click **Install** — it will be installed in your current Codespace.

> Some popular extensions:
- Python (Microsoft)
- Prettier (Code formatter)
- GitLens (Git superpowers)
- GitHub Theme Kit (custom themes)

### ⚙️ For JetBrains IDEs

1. From the **Settings menu**, go to **Plugins**.
2. Search or upload a plugin `.jar` file.
3. Install and restart your IDE inside the Codespace.



## 🔁 How Codespaces Work

When you start a Codespace, several steps occur behind the scenes:

1. **Virtual Machine & Storage Allocation**: A VM and storage are assigned to your session.
2. **Container Creation**: A Docker container is created based on your configuration.
3. **Connection Established**: You're connected via the web or desktop client.
4. **Post-Creation Setup**: Scripts or configurations in `.devcontainer.json` run automatically.

> This ensures your environment is consistent, secure, and ready to use every time you open it.


## 💾 Save Changes in a Codespace

Changes made inside your Codespace are saved **to the virtual machine in the cloud**.

### AutoSave Behavior:
- In **web-based Codespaces**, changes are automatically saved periodically.
- In **desktop-connected Codespaces**, you must enable **AutoSave** manually.

### Important Notes:
- If you close your Codespace without committing, you’ll be prompted to save your work.
- **Uncommitted changes may be lost** if the Codespace is deleted or times out.
- To ensure your work is preserved, always:
  - ✅ Commit your changes
  - 🚀 Push them to your remote repository



## 🔄 Open an Existing Codespace

If you’ve used a Codespace before, you can easily reopen it:

1. Go to your repository on GitHub.
2. Click the **Code** dropdown.
3. Select **Open with GitHub Codespaces**.
4. Choose an existing session or create a new one.



## ❓ Module Assessment Questions

Here are the practice questions covered in this module to help reinforce your understanding:

### Question 1:
**Which directory is the clone placed in after creating a Codespace?**

- ✅ `/workspaces` directory  
- ❌ `/temp` directory  
- ❌ `~/.bashrc` directory  
- ❌ Linux directory

### Question 2:
**What's the maximum number of Codespaces that you can create per repository or branch?**

- ❌ You can only create two Codespaces  
- ❌ You can create a total of 10 Codespaces  
- ✅ You can create a total of 30 Codespaces  

> Note: These limits may vary depending on your GitHub plan (Free, Pro, Team, etc.)



## 🎯 Summary

By completing this module, you now understand how to:

✅ Add and manage **extensions/plugins** in your Codespace  
🔁 Understand the **lifecycle of a Codespace**  
💾 Save and preserve your **changes safely**  
🧠 Test your knowledge with **assessment questions**
