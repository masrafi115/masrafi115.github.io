---
title: "Getting Started with Hugo and Markdown Note Taking"
date: 2026-06-10T10:30:00Z
lastmod: 2026-06-10T10:30:00Z
draft: false
description: "A comprehensive guide to setting up Hugo for blogging and markdown note-taking"
categories:
  - Hugo
  - Blogging
  - Markdown
tags:
  - hugo
  - static-site-generator
  - markdown
  - tutorial
image: ""
---

## Introduction

Hugo is a powerful static site generator that allows you to create fast, scalable websites using markdown. Whether you're building a blog, documentation site, or personal knowledge base, Hugo provides an excellent foundation.

In this post, we'll explore how to set up Hugo and use it for both blogging and markdown note-taking.

## Why Hugo?

### Key Benefits

1. **Speed** - Hugo is incredibly fast, generating sites in milliseconds
2. **Simplicity** - No databases required, just markdown files
3. **Flexibility** - Extensive theme ecosystem and customization options
4. **Git-Friendly** - Your content lives in version control
5. **Free Hosting** - Deploy to GitHub Pages, Netlify, or Vercel for free

## Installation

### Prerequisites

- Go (version 1.13 or later)
- Git
- A code editor (VS Code, Sublime Text, etc.)

### Installing Hugo

**On macOS (using Homebrew):**
```bash
brew install hugo
```

**On Ubuntu/Linux:**
```bash
sudo apt-get install hugo
```

**On Windows:**
```bash
choco install hugo -confirm
```

Verify the installation:
```bash
hugo version
```

## Creating Your First Site

```bash
hugo new site my-blog
cd my-blog
git init
```

## Adding a Theme

Hugo uses themes to control the site's appearance. The Maverick theme is a clean, minimal theme perfect for developers.

```bash
git submodule add https://github.com/canhtran/maverick.git themes/maverick
```

Update your `hugo.toml`:
```toml
theme = "maverick"
baseURL = "https://yourdomain.com/"
```

## Content Organization

### Structure

```
content/
├── post/
│   ├── my-first-post.md
│   └── another-post.md
├── page/
│   ├── about.md
│   └── contact.md
└── notes/
    ├── quick-tips.md
    └── learning-resources.md
```

## Creating Blog Posts

### New Post

```bash
hugo new post/my-first-post.md
```

### Front Matter (Metadata)

Every markdown file starts with YAML front matter:

```yaml
---
title: "My First Post"
date: 2026-06-10T10:30:00Z
lastmod: 2026-06-10T10:30:00Z
draft: false
description: "This is a demo post"
categories:
  - Blog
tags:
  - hugo
  - demo
image: "/images/my-image.jpg"
---
```

## Markdown for Note-Taking

### Basic Syntax

**Bold:** `**text**` → **text**
*Italic:* `*text*` → *text*
`Code:` `` `code` `` → `code`

### Headings

```markdown
# H1 - Main Title
## H2 - Section
### H3 - Subsection
#### H4 - Minor heading
```

### Lists

**Unordered:**
```markdown
- Item 1
- Item 2
  - Nested item
```

**Ordered:**
```markdown
1. First
2. Second
   1. Nested numbered
```

### Code Blocks

Syntax highlighting with language specification:

````markdown
```go
func main() {
    fmt.Println("Hello, Hugo!")
}
```
````

### Blockquotes

```markdown
> "The best time to plant a tree was 20 years ago. 
> The second best time is now." - Chinese Proverb
```

> "The best time to plant a tree was 20 years ago. The second best time is now." - Chinese Proverb

### Tables

```markdown
| Feature | Hugo | Others |
|---------|------|--------|
| Speed   | ⚡   | 🐢     |
| Learning| Easy | Hard   |
| Setup   | 5min | 1hour  |
```

| Feature | Hugo | Others |
|---------|------|--------|
| Speed   | ⚡   | 🐢     |
| Learning| Easy | Hard   |
| Setup   | 5min | 1hour  |

## Running Locally

Start the development server:

```bash
hugo server
```

Then visit `http://localhost:1313` in your browser. The site auto-reloads when you make changes!

## Building for Production

Generate static files:

```bash
hugo
```

This creates a `public/` directory with your static site ready to deploy.

## Organizing Notes

### Create a Notes Section

1. Create `content/notes/_index.md`
2. Organize notes by topic:

```
content/notes/
├── golang/
│   ├── goroutines.md
│   └── interfaces.md
├── web-development/
│   ├── rest-apis.md
│   └── authentication.md
└── databases/
    └── sql-optimization.md
```

### Note Template

```yaml
---
title: "Goroutines in Go"
date: 2026-06-10
draft: false
tags: [golang, concurrency]
categories: [Go]
---

## What are Goroutines?

Your content here...
```

## Tips for Effective Note-Taking

### 1. Use Tags & Categories

Organize by both topic and type:
```yaml
tags: [golang, concurrency, performance]
categories: [Learning, Reference]
```

### 2. Consistent Naming

Use clear, descriptive names:
- ✅ `understanding-go-interfaces.md`
- ❌ `notes.md`

### 3. Link Related Content

```markdown
See also: [Goroutines Guide](/post/goroutines-guide/)
```

### 4. Version Your Knowledge

Update `lastmod` when you revise notes:
```yaml
lastmod: 2026-06-10T14:30:00Z
```

## Deployment

### GitHub Pages

1. Create a `gh-pages` branch
2. Set GitHub Pages source in repository settings
3. Push to deploy

### With GitHub Actions

Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy Hugo

on:
  push:
    branches:
      - master

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
      - name: Build
        run: hugo
      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./public
```

## Conclusion

Hugo provides an elegant solution for both blogging and note-taking. With its powerful markdown support, fast build times, and seamless Git integration, it's an excellent choice for developers who want to document their learning journey.

### Next Steps

1. ✅ Install Hugo
2. ✅ Create your site
3. ✅ Choose a theme (Maverick recommended)
4. ✅ Write your first post
5. ✅ Deploy to GitHub Pages

Happy blogging! 📝

---

**Questions or suggestions?** Feel free to reach out on [GitHub](https://github.com/masrafi115) or via [email](mailto:mainulhasanmasrafi49715@gmail.com).
