# 🐍 Using GitHub Copilot with Python

Welcome! 👋 In this guide, you'll learn how to **boost your Python development workflow using GitHub Copilot** — an AI-powered coding assistant that suggests code right in your editor.

Whether you're building APIs, automating tasks, or writing complex logic, GitHub Copilot can help you write code faster and more efficiently. Let’s dive in! 🚀

## 💡 What Is GitHub Copilot?

GitHub Copilot is like a smart pair-programming partner that helps you write code by suggesting lines or even entire functions based on what you're typing.

### 🔧 Key Features:
- Suggests code snippets in real-time
- Understands natural language comments
- Works inside popular IDEs like VS Code, PyCharm, VIM, and more
- Uses OpenAI Codex to understand context and provide relevant suggestions

> 📌 Tip: The better your prompts or comments, the better the suggestions will be!

## 🛠️ Getting Started with GitHub Copilot

Before you start coding with Copilot, make sure you have:

1. A **GitHub account** with [GitHub Copilot access](https://github.com/features/copilot)
2. Your favorite **IDE installed** (like Visual Studio Code)
3. The **GitHub Copilot extension** installed in your IDE

### ✅ Free Tier Available:
GitHub Copilot offers a **free tier** with:
- 2,000 code autocompletes per month
- 50 chat messages per month  
Perfect for students, educators, and open-source contributors!

🎓 Educators and students can apply for **Copilot Pro for free** at: [https://aka.ms/Copilot4Students](https://aka.ms/Copilot4Students)

## 🧪 Hands-On: Set Up GitHub Copilot in VS Code

1. Open **Visual Studio Code**
2. Go to **Extensions Marketplace**
3. Search for "**GitHub Copilot**"
4. Install the extension
5. Sign in to your GitHub account when prompted

Now you’re ready to start coding with intelligent suggestions!

## 🌐 Use GitHub Codespaces for a Preconfigured Environment

GitHub Codespaces gives you a **ready-to-code cloud environment**, preloaded with tools and extensions like GitHub Copilot.

### 🚀 Quick Setup Steps:
1. Open the [preconfigured Codespace link](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-python)
2. Click **Create new codespace**
3. Wait a few moments while it loads

You’ll land in a browser-based VS Code environment with GitHub Copilot already set up!

## 🧑‍💻 Exercise: Update a Python Web API with GitHub Copilot

Let’s walk through how to use GitHub Copilot to enhance a Python web API project.

### 🎯 Goals:
- Create a FastAPI endpoint that accepts text input
- Generate a checksum from the input
- Return the result via a POST request

### Step 1: Add a Pydantic Model

In your `main.py` file, add a comment like this:

```python
# Define a Pydantic model for incoming data
```

GitHub Copilot will suggest a class like:

```python
class Text(BaseModel):
    text: str
```

Press `Tab` to accept the suggestion! ✅

### Step 2: Generate a New Endpoint

Add another comment:

```python
# Create a FastAPI endpoint that accepts a POST request with a JSON body containing a single field called "text" and returns a checksum of the text
```

GitHub Copilot will generate the route and logic for you.

### Step 3: Add Missing Imports

If you get errors about missing modules (`base64`, `os`), ask GitHub Copilot Chat:

> "Help me add the necessary imports for base64 encoding and OS random generation."

Or manually add:

```python
import base64
import os
```

### Step 4: Test Your API

Go to the `/docs` endpoint in the browser tab within your Codespace. You should see your new API listed and ready to test!

Click **Try it out** and send a sample request to verify everything works.

## 🧠 Prompt Engineering Tips

The quality of GitHub Copilot’s suggestions depends heavily on how well you phrase your prompt.

### ✅ Good Prompt Example:
```python
# Create a FastAPI endpoint that accepts a POST request with a JSON payload in a POST request
```

### ❌ Bad Prompt Example:
```python
# Create an API endpoint
```

💡 The more specific you are, the better the results!

## 🧰 Best Practices When Using GitHub Copilot

- **Start simple, then elaborate**  
  Begin with a basic idea and build upon it step by step.

- **Cycle through suggestions**  
  Press `Ctrl + Enter` (or `Cmd + Enter` on Mac) to see multiple options.

- **Use GitHub Copilot Chat**  
  Ask questions directly to refine your code or debug issues.

- **Leverage context from open files**  
  Copilot uses all open files to give smarter suggestions.

## 🧪 Module Assessment

### Question 1:
**How does GitHub Copilot work?**

✅ *Uses natural language prompts and code context to generate suggestions*  
❌ *Only works with selected text*  
❌ *Uses radio signals to communicate*

### Question 2:
**What are some GitHub Copilot Free features?**

✅ *Provides code suggestions and limited chat messages directly in your IDE*  
❌ *Unlimited unrestricted AI coding help*  
❌ *Slower responses to save quota*

### Question 3:
**How do you accept GitHub Copilot suggestions?**

✅ *Press the Tab key*  
❌ *Press F1 or F4*

### Question 4:
**Which statement is valid?**

✅ *A prompt is our input — instructions that tell Copilot what to generate*  
❌ *A prompt is a collection of songs or laptops*

### Question 5:
**What does the output quality depend on?**

✅ *How well the prompt is written*  
❌ *Your code editor or extension installation*

## 🙌 Final Thoughts

GitHub Copilot is a powerful tool that can significantly speed up your Python development. From generating boilerplate code to helping with complex logic, it's a great assistant for developers of all skill levels.

Start small, experiment with different prompts, and soon you’ll wonder how you ever coded without it! 💻✨

## 📚 Want to Learn More?

Check out:
- [GitHub Copilot Documentation](https://docs.github.com/en/codespaces/developing-in-codespaces/using-github-copilot-in-codespaces)
- [FastAPI Official Docs](https://fastapi.tiangolo.com/)
- [GitHub Copilot Free Signup](https://gh.io/copilot)

## 🏁 Congratulations!

You’ve just learned how to use **GitHub Copilot with Python** to build a web API, create endpoints, and even test them — all with the help of AI-powered suggestions.

Keep experimenting, keep learning, and most importantly — keep coding! 🎉🚀
