---
title: "Markdown Formatting Guide for Developers"
date: 2026-06-10T11:00:00Z
lastmod: 2026-06-10T11:00:00Z
draft: false
description: "Complete markdown syntax guide for technical writing and note-taking"
categories:
  - Reference
  - Markdown
tags:
  - markdown
  - formatting
  - reference
  - technical-writing
---

## Markdown Essentials for Technical Documentation

Markdown is the universal language for technical writers and developers. This guide covers all essential markdown syntax for effective note-taking and blog writing.

## Text Formatting

### Basic Formatting

```markdown
**Bold text** or __Bold text__
*Italic text* or _Italic text_
***Bold and italic***
~~Strikethrough text~~
`Inline code`
```

**Result:**

**Bold text** or __Bold text__
*Italic text* or _Italic text_
***Bold and italic***
~~Strikethrough text~~
`Inline code`

## Headings

Use headings to structure your content hierarchically:

```markdown
# Heading 1 (h1) - Main Title
## Heading 2 (h2) - Major Section
### Heading 3 (h3) - Subsection
#### Heading 4 (h4) - Minor Section
##### Heading 5 (h5) - Details
###### Heading 6 (h6) - Sub-details
```

**Best Practice:** Start with `##` in blog posts, reserve `#` for page titles.

## Lists

### Unordered Lists

```markdown
- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3
```

- Item 1
- Item 2
  - Nested item 2.1
  - Nested item 2.2
- Item 3

### Ordered Lists

```markdown
1. First step
2. Second step
   1. Substep 2.1
   2. Substep 2.2
3. Third step
```

1. First step
2. Second step
   1. Substep 2.1
   2. Substep 2.2
3. Third step

### Checklist (Task Lists)

```markdown
- [x] Completed task
- [ ] Incomplete task
- [x] Another completed task
```

- [x] Completed task
- [ ] Incomplete task
- [x] Another completed task

## Code

### Inline Code

Use backticks for inline code:
```markdown
The `function()` method returns a value.
```

The `function()` method returns a value.

### Code Blocks

#### Basic Code Block

````markdown
```
Plain text code without syntax highlighting
```
````

#### With Syntax Highlighting

Specify the language after the opening triple backticks:

````markdown
```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
```
````

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
```

#### Other Popular Languages

```python
# Python
def factorial(n):
    return 1 if n <= 1 else n * factorial(n - 1)
```

```go
// Go
func main() {
    fmt.Println("Hello, World!")
}
```

```bash
# Bash
echo "Running a bash script"
for i in {1..5}; do
    echo "Number: $i"
done
```

```sql
-- SQL
SELECT * FROM users 
WHERE active = true 
ORDER BY created_at DESC;
```

```html
<!-- HTML -->
<div class="container">
  <h1>Hello World</h1>
  <p>This is a paragraph.</p>
</div>
```

## Blockquotes

```markdown
> This is a blockquote
> It can span multiple lines
>
> And have multiple paragraphs
```

> This is a blockquote
> It can span multiple lines
>
> And have multiple paragraphs

### Nested Blockquotes

```markdown
> This is the first level
> > This is nested
> > > This is more nested
```

> This is the first level
> > This is nested
> > > This is more nested

## Links and Images

### Links

```markdown
[Link text](https://example.com)
[Link with title](https://example.com "Page title")
<https://example.com>
```

[Link text](https://example.com)
[Link with title](https://example.com "Page title")

### Images

```markdown
![Alt text](https://via.placeholder.com/200)
![Image with title](https://via.placeholder.com/200 "Image title")
```

### Reference-Style Links

```markdown
This is a [link][1] and [another link][2].

[1]: https://example.com
[2]: https://another-example.com
```

## Tables

### Basic Table

```markdown
| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |
```

| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |

### Aligned Columns

```markdown
| Left   | Center | Right |
|:-------|:------:|------:|
| Left   | Center | Right |
| Data   | Data   | Data  |
```

| Left   | Center | Right |
|:-------|:------:|------:|
| Left   | Center | Right |
| Data   | Data   | Data  |

## Horizontal Rules

Three or more of any of: `---`, `***`, `___`

```markdown
---
***
___
```

## Escape Characters

Use backslash to escape markdown characters:

```markdown
\*Not italic\*
\[Not a link\](https://example.com)
\# Not a heading
```

\*Not italic\*
\[Not a link\](https://example.com)
\# Not a heading

## HTML and Special Formatting

### Superscript and Subscript

```markdown
H~2~O (subscript)
E=mc^2^ (superscript)
```

H~2~O (subscript)
E=mc^2^ (superscript)

### Keyboard Keys

```markdown
Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.
```

Press <kbd>Ctrl</kbd> + <kbd>C</kbd> to copy.

### Highlighting

```markdown
==Highlighted text==
```

### Small Text

```markdown
<small>This is smaller text</small>
```

<small>This is smaller text</small>

## Emoji

```markdown
😊 🎉 🚀 ⚡ 📝 🔧 💡 ✅ ❌ ⚠️
```

😊 🎉 🚀 ⚡ 📝 🔧 💡 ✅ ❌ ⚠️

## Pro Tips for Technical Writing

### 1. Consistent Code Formatting

Always use backticks for filenames, commands, and technical terms:
- ✅ "Edit your `config.toml` file"
- ❌ "Edit your config.toml file"

### 2. Use Lists for Steps

```markdown
## Installation Steps

1. Download the package
2. Extract the files
3. Run `./install.sh`
4. Follow the prompts
```

### 3. Highlight Important Information

```markdown
> **Note:** This is important information
> **Warning:** Be careful with this step
> **Tip:** This might be helpful
```

### 4. Code Comments in Examples

```bash
# First, navigate to the project
cd my-project

# Install dependencies
npm install

# Start the development server
npm run dev
```

### 5. Link Related Content

```markdown
See also: [Getting Started Guide](/posts/getting-started/)
Learn more: [Advanced Topics](/posts/advanced/)
```

## Common Markdown Tools

- **Editors:** VS Code, Sublime Text, Vim, Obsidian
- **Viewers:** GitHub, GitLab, Notion, Markdown Preview Plus
- **Converters:** Pandoc, Markdownify
- **Validators:** Markdown Lint

## Browser Support

Markdown is rendered by:
- GitHub (`.md` files)
- GitLab
- Reddit
- Discord (partial support)
- Most documentation sites

## Conclusion

Mastering markdown will significantly improve your technical writing. The syntax is simple, yet powerful enough for complex documentation.

**Practice:** Use this guide as a reference while writing your next blog post or technical note. Soon, markdown will become second nature!

---

**Quick Reference Cheatsheet:**

| Element | Markdown | Result |
|---------|----------|--------|
| Bold | `**text**` | **text** |
| Italic | `*text*` | *text* |
| Code | `` `text` `` | `text` |
| Link | `[text](url)` | Link |
| Image | `![alt](url)` | Image |
| Heading | `## Text` | ## Text |
| List | `- item` | • item |
| Quote | `> text` | Indented |

---

Happy writing! ✍️
