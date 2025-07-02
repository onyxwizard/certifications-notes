# 🔍 Domain 5 - Identify Security Vulnerabilities in Your Codebase by Using CodeQL

Welcome to **Domain 5** of GitHub Advanced Security (GHAS)! 🚀  
In this guide, you'll learn how to **use CodeQL — a powerful semantic code analysis engine** — to identify security vulnerabilities and coding errors in your codebase.

Whether you're a developer, DevOps engineer, or part of a security team, mastering CodeQL will help you write more secure code and catch issues early in the development lifecycle. Let’s dive in! 💻🔒

## 🧠 What Is CodeQL?

**CodeQL** is a code analysis tool developed by GitHub that treats code like data — allowing you to query it using a custom language called QL (Query Language). It helps you find:

- 🔐 Security vulnerabilities (e.g., SQL injection, XSS)
- 🐞 Bugs and logic errors
- ⚠️ Insecure patterns or outdated practices

With CodeQL, you can:
- Analyze both compiled and interpreted languages
- Create custom queries for specific threats
- Use built-in queries from GitHub researchers and the community

> 💡 Think of CodeQL as a search engine for your code — helping you find not just what the code does, but **what it could do if exploited**.

## 🛠️ How Does CodeQL Work?

CodeQL works in three main steps:

### 1. 📦 Database Creation
First, CodeQL builds a relational database from your codebase. This includes:
- Abstract syntax tree (AST)
- Control-flow graph
- Data-flow graph

Each language has its own schema, ensuring accurate representation of language-specific features.

> 📌 Example: For Java, CodeQL understands classes, methods, and inheritance structures.

### 2. 🧩 Query Execution
Next, you run queries (`.ql` files) on the database to detect potential issues.

A basic query structure looks like this:
```ql
/**
 * @name Example Vulnerability Query
 * @description Finds potentially unsafe function calls
 */
import java

from Method m
where m.getName() = "exec" and m.getDeclaringType().hasQualifiedName("java.lang", "Runtime")
select m, "This method may execute untrusted commands."
```

Queries can be:
- **Alert queries**: Highlight problems in specific code locations
- **Path queries**: Show how data flows between a source and a sink (e.g., user input to system command)

### 3. 📊 Result Interpretation
After running queries, CodeQL returns results in SARIF format (Static Analysis Results Interchange Format), which integrates directly into GitHub as **code scanning alerts**.

You can view these alerts in the **Security tab** of your repository.

![Screenshot showing CodeQL analysis alerts](https://learn.microsoft.com/en-us/training/github/codebase-representation-codeql/media/code-scanning-alert-screenshot.png)

## 🧰 Supported Languages

CodeQL supports many popular programming languages, including:
- C / C++
- C#
- Go
- Java / Kotlin
- JavaScript / TypeScript
- Python
- Ruby
- Swift

This makes it versatile for multi-language projects and teams.

## 🧪 How to Prepare a CodeQL Database

Before analyzing your code, you must create a CodeQL database.

### Step-by-step:

1. ✅ Install the **CodeQL CLI**
2. 📂 Check out the version of your code you want to analyze
3. 🧱 For compiled languages, ensure dependencies are installed and the project is buildable
4. 🧹 Run the extraction process:
   ```bash
   codeql database create my-database --language=java --command="make"
   ```

The result is a snapshot of your code that you can query with CodeQL.

## 📋 Understanding the CodeQL Database Structure

A CodeQL database includes two main tables:

| Table | Description |
|-------|-------------|
| `expressions` | Contains rows for every expression analyzed |
| `statements` | Contains rows for every statement analyzed |

These tables allow detailed inspection of control flow, data flow, and logical relationships in your code.

## 🔎 Types of Queries

There are two key types of CodeQL queries:

### 1. ❗ Alert Queries
Identify specific issues in your code, such as:
- Hardcoded credentials
- Improper input validation
- Unsafe deserialization

Example: A query that finds all uses of `eval()` in JavaScript.

### 2. 🔄 Path Queries
Show how data moves through your code — especially useful for identifying:
- Cross-site scripting (XSS)
- Command injection
- Sensitive data leaks

Example: Tracking how user input flows into a database query without sanitization.

## 📝 Writing Custom CodeQL Queries

You can write your own `.ql` files to detect custom patterns relevant to your organization.

### Basic Query Template:
```ql
/**
 * @name My Custom Query
 * @description Finds insecure API usage
 * @kind path-problem
 * @problem.severity warning
 * @id java/insecure-api-call
 */

import java
import semmle.code.java.dataflow.FlowSources
import semmle.code.java.dataflow.FlowSinks

from PathNode source, PathNode sink
where source.asExpr().(Literal).getValue() = "unsafe"
  and sink.getNode().getEnclosingCallable().getName() = "execute"
select sink, source, sink, "Potential unsafe API call detected."
```

> 📌 Tip: Always include metadata like description, severity, and ID for better integration with GitHub.

## 📦 Query Metadata Explained

Metadata tells GitHub how to interpret and display your query results.

It includes:
- Query name and description
- Severity level (`warning`, `error`)
- Kind of problem (`alert`, `path-problem`)
- Unique ID for tracking

GitHub provides a [style guide for metadata](https://github.com/github/codeql/blob/main/docs/query-metadata-style-guide.md) to ensure consistency across teams and tools.

## 🧱 Optimizing CodeQL Performance

Sometimes CodeQL scans take longer than expected. Here's how to improve performance:

✅ Increase memory or CPU on self-hosted runners  
✅ Avoid large predicates that generate massive tables  
✅ Optimize custom queries for efficiency  
✅ Use caching for repeated analyses  

For troubleshooting, refer to the official [CodeQL performance guide](https://codeql.github.com/docs/writing-codeql-queries/troubleshooting-query-performance/).

## 🛡️ Detecting Data-Flow Vulnerabilities

CodeQL excels at detecting **data-flow vulnerabilities**, such as:
- 🕵️‍♂️ SQL injection
- 🧨 Command injection
- 🛑 Sensitive data leakage

By tracing how untrusted data flows from sources (like user input) to sinks (like databases or APIs), you can uncover hidden risks.

## 🧩 Integrating CodeQL with GitHub Actions

To automate CodeQL scanning in your CI/CD pipeline:

1. Add a workflow file: `.github/workflows/codeql.yml`
2. Configure the languages and events to trigger scans
3. Push changes and watch alerts appear in the **Security tab**

Here’s an example workflow:
```yaml
name: "CodeQL"
on:
  push:
    branches: [main]
  schedule:
    - cron: '0 0 * * 0' # Weekly scan
jobs:
  analyze:
    name: Analyze
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repo
        uses: actions/checkout@v3
      - name: Initialize CodeQL
        uses: github/codeql-action/init@v2
      - name: Perform CodeQL Analysis
        uses: github/codeql-action/analyze@v2
```

## 📁 Uploading SARIF Files Manually

If you're using CodeQL outside GitHub (e.g., internal CI systems), you can upload results manually:

1. Generate a SARIF file from your CodeQL CLI run
2. Upload using GitHub’s CodeQL Action or the REST API
3. View results in the **Security > Code scanning alerts** tab

Example CLI command:
```bash
codeql database analyze my-database my-query.ql --format=sarifv2 --output=results.sarif
```

## 🧹 Troubleshooting Common Issues

Some common issues when working with CodeQL:

⚠️ **Long scan times**: Optimize queries or increase runner resources  
🚫 **Permission errors**: Ensure your token has `security_events` write permissions  
🔄 **SARIF upload fails**: Disable CodeQL temporarily before re-uploading  
🛠 **CLI setup issues**: Verify paths and environment variables  

Refer to the [official troubleshooting guide](https://docs.github.com/en/code-security/code-scanning/troubleshooting-code-scanning) for detailed solutions.

## 🙌 Final Thoughts

Using CodeQL to identify security vulnerabilities gives you deep insights into your codebase — beyond what traditional static analyzers offer. By turning code into data, you can write precise queries to detect real-world threats and prevent them before they reach production.

Start today by enabling CodeQL in your repositories, writing custom queries, and integrating it into your CI/CD pipelines. And don’t forget to share knowledge with your team so everyone benefits.

Stay secure! 🔐✨

## 📚 Want to Learn More?

Check out:
- [CodeQL Documentation](https://codeql.github.com/)
- [CodeQL CLI Setup Guide](https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/)
- [Writing Secure Code with CodeQL](https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning)

## ✅ Exercise: Write and Run a CodeQL Query

Try what you've learned by completing a hands-on exercise:
- Set up the CodeQL CLI
- Create a database from a sample codebase
- Write a custom query to detect a vulnerability
- Run the query and review results
- Upload findings to GitHub

This practice will reinforce your understanding and help you become a GHAS pro! 💪

Ready to start securing your code? Start scanning today! 🔍🚀
