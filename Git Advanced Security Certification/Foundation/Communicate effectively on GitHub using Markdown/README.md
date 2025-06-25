
# 📝 GitHub Flavored Markdown (GFM) Guide

Markdown is a lightweight and easy-to-use syntax for styling text. GitHub uses its own version called **GitHub Flavored Markdown** (GFM), which includes all standard Markdown features plus some custom enhancements.

This guide covers the basics of formatting text, writing code blocks, and using inline formatting in GFM.



## 🖋️ Formatting Text

You can emphasize text using **bold**, *italic*, or both.

### Italic Text
Use a single asterisk `*` or underscore `_` on each side:

```markdown
*This text is italic*
_This text is also italic_
```

> *This text is italic*  
> _This text is also italic_


### Bold Text
Use double asterisks `**` or double underscores `__`:

```markdown
**This text is bold**
__This text is also bold__
```

> **This text is bold**  
> __This text is also bold__



### Combined Emphasis
You can mix **bold** and *italic* together:

```markdown
_**Bold and italic**_
**_Also bold and italic_**
```

> _**Bold and italic**_  
> **_Also bold and italic_**



## 💻 Code Formatting

### Inline Code
Wrap short snippets of code with backticks:

```markdown
Use the `var` keyword to declare a variable.
```

> Use the `var` keyword to declare a variable.



### Code Blocks
For multi-line code examples, use triple backticks (```) before and after the block:

````markdown
```javascript
var first = 1;
var second = 2;
var sum = first + second;
```
````

> ```javascript
> var first = 1;
> var second = 2;
> var sum = first + second;
> ```



### Syntax Highlighting
Add the language name after the opening backticks for syntax highlighting:

````markdown
```python
def greet(name):
    print(f"Hello, {name}!")
```
````

> ```python
> def greet(name):
>     print(f"Hello, {name}!")
> ```

Supported languages include:
- `javascript`
- `python`
- `html`
- `css`
- `bash`
- And many more!



## 🔁 Escaping Special Characters

If you want to show literal asterisks or underscores instead of applying formatting, escape them with a backslash `\`.

```markdown
\_This is all \*\*plain\*\* text\_
```

> _This is all **plain** text_



## ✅ Summary

| Format | Markdown Syntax | Output |
|--------|------------------|--------|
| Italic | `*text*` or `_text_` | *text* |
| Bold   | `**text**` or `__text__` | **text** |
| Inline Code | ``` `code` ``` | `code` |
| Code Block | ``` ```code``` ``` | Multi-line code block |
| Escaped Character | `\*literal asterisk\*` | \*literal asterisk\* |



## 🧠 Tips
- Always close emphasis tags (`*`, `_`, `**`, `__`) properly.
- Use fenced code blocks for readability when sharing longer code examples.
- Specify the language in code blocks for better syntax highlighting.
- Escape special characters if you don’t want them to format the text.