---
name: glamour
description: Render Markdown beautifully in the terminal with ANSI styling. Supports themes (dark, light, dracula, tokyo-night, etc.), custom styles, and word wrapping. Use when displaying formatted Markdown content in CLI tools or terminal UIs.
---

# glamour

Stylesheet-based Markdown rendering for terminals. TypeScript port of charmbracelet/glamour.

## Setup

```bash
npm install -g @indiekitai/glamour
```

## CLI Usage

```bash
# Render a Markdown file
npx @indiekitai/glamour README.md

# Choose a theme
npx @indiekitai/glamour README.md --style dark
npx @indiekitai/glamour README.md --style dracula
npx @indiekitai/glamour README.md --style tokyo-night

# Set width
npx @indiekitai/glamour README.md --width 80

# JSON output (rendered text + metadata)
npx @indiekitai/glamour README.md --json

# Pipe markdown
echo "# Hello **world**" | npx @indiekitai/glamour
```

## Programmatic Usage

```typescript
import { render } from '@indiekitai/glamour';

const output = render('# Hello **world**', { style: 'dark', width: 80 });
console.log(output);
```

## Built-in Themes

dark, light, ascii, notty, pink, dracula, tokyo-night

## MCP Tools

- `render_markdown` — Render with theme and width options
- `render_plain` — Strip formatting, plain text output
- `list_styles` — Show available themes
