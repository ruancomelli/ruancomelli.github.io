+++
title = "Today I set up a perfect Cursor workspace for this website"
date = 2025-01-13
description = "Quick log of getting my development environment just right"

[taxonomies]
tags = ["tools", "workflow", "cursor"]

[extra]
kind = "Log"
+++

Spent some time today getting my Cursor setup perfect for working on this Zola site. Here's what made the biggest difference:

**Extensions that matter:**

- Even Better TOML (essential for frontmatter)
- Zola syntax highlighting
- Live Server (for quick previews)

**Workspace settings:**

```json
{
  "files.associations": {
    "*.md": "markdown"
  },
  "markdown.preview.breaks": true
}
```

**The game changer:** Set up a custom snippet for new blog posts that auto-fills the frontmatter template. No more copying and pasting dates or forgetting required fields.

**Cursor AI integration:** The AI understands Zola's structure really well now that I've been working in this workspace. It suggests the right shortcode syntax and catches frontmatter mistakes.

Small improvements that add up to a much smoother writing experience. The friction between "I want to write something" and "I'm actually writing" is now almost zero.
