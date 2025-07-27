# 🧠 Ultimate Markdown Cheat Sheet (2025 Edition)

Your go-to guide for writing **clean**, **professional**, and **powerful** markdown docs, blogs, or GitHub READMEs.  
Includes collapsibles, file trees, task lists, emojis, tables, code blocks, and more.

---

## 1. ✅ Headers

```md
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

---

## 2. ✍️ Text Styles

```md
**bold**
_italic_
~~strikethrough~~
**_bold italic_**
> blockquote
```

---

## 3. 📋 Lists

### Bullet List

```md
- Item 1
- Item 2
  - Subitem
```

### Numbered List

```md
1. First
2. Second
   1. Sub-numbered
```

---

## 4. 📌 Task Lists

```md
- [x] Completed
- [ ] Incomplete
```

- [x] Completed  
- [ ] Incomplete

---

## 5. 🌐 Links

```md
[OpenAI](https://openai.com)
```

---

## 6. 🖼 Images

```md
![Alt text](https://your-image-url.com/image.png)
```

---

## 7. 🧾 Tables

```md
| Name    | Role      |
|---------|-----------|
| AKR     | Developer |
| Bro | Assistant |
```

| Name    | Role      |
|---------|-----------|
| AKR     | Developer |
| Bro | Assistant |

---

## 8. 🧠 Blockquotes

```md
> This is a blockquote
> Multiple lines supported
```

> This is a blockquote  
> Multiple lines supported

---

## 9. ✨ Code Blocks

### Inline

```md
Use `npm install` to install.
```

### Multiline

<pre>
```js
const greet = () => {
  console.log("Hello, Bro!");
}
```
</pre>

---

## 10. 🌳 Collapsible Tree Structure (GitHub/VS Code)

```md
<details>
<summary>📁 your-app/</summary>

<details>
<summary>📁 src/</summary>

- App.js  
- index.js

</details>

- package.json  
- README.md

</details>
```

<details>
<summary>📁 your-app/</summary>

<details>
<summary>📁 src/</summary>

- App.js  
- index.js

</details>

- package.json  
- README.md

</details>

---

## 11. 📂 Collapsible Section

```md
<details>
<summary>Click to expand</summary>

Hidden content goes here.

</details>
```

<details>
<summary>Click to expand</summary>

Hidden content goes here.

</details>

---

## 12. 🧪 Syntax Highlighting

```js
// JavaScript
console.log("Hello world");
```

```bash
# Bash
npm install -g expo-cli
```

```python
# Python
def greet():
    print("Hello, HHM!")
```

---

## 13. 😎 Emojis

Use directly (copy/paste or use codes like `:rocket:`)

✅ 🔥 💻 🚀 📁 📦 🛠️ 🧠 🧱 📝 🤖 🧙‍♂️ 💡

---

## 14. 📏 Horizontal Line

```md
---
```

---

## 15. 🏷 Footnotes (GitHub doesn’t support, but Obsidian does)

```md
Here is a footnote reference.[^1]

[^1]: Here is the footnote.
```

---

## 16. 🧩 HTML in Markdown

Works in GitHub, VS Code, Obsidian.

```html
<b>bold</b>
<i>italic</i>
<details><summary>Title</summary>Hidden</details>
```

---

## 17. 🗂️ File/Folder Trees

```md
project/
├── src/
│   └── index.js
├── public/
│   └── index.html
└── package.json
```

---

## 18. 📚 Advanced Tip: Custom Anchors

```md
<a name="section-name"></a>
```

Link to it:

```md
[Jump to section](#section-name)
```

---

## 19. 📅 Date & Time Format (Markdown Extensions Only)

```md
==Highlight==
==Important==
```

> These are useful in Obsidian/Markdown Preview Enhanced.

---

## 20. ⚠️ Gotchas

| Platform      | Supports HTML? | Supports Collapsibles? | Footnotes? |
|---------------|----------------|-------------------------|------------|
| GitHub        | ✅              | ✅ (`<details>`)        | ❌         |
| VS Code       | ✅              | ✅                      | ❌         |
| Obsidian      | ✅              | ✅                      | ✅         |
| GitHub Pages  | ✅              | ✅                      | ❌         |

---

> Written by [AKR].  
> Use it, copy it, remix it.