---
name: lipgloss
description: Terminal styling library with CSS-like API. Apply colors, borders, padding, margins, and alignment to terminal text. Use when building beautiful CLI output or terminal UIs in TypeScript/Node.js.
---

# lipgloss

CSS-like terminal styling for TypeScript/Node.js. Port of charmbracelet/lipgloss.

## Setup

```bash
npm install @indiekitai/lipgloss
```

## CLI Usage

```bash
# Style text from CLI
npx @indiekitai/lipgloss "Hello World" --fg "#FF69B4" --bold --border rounded --padding 1

# JSON output
npx @indiekitai/lipgloss "Hello World" --fg red --json
```

## Programmatic Usage

```typescript
import { NewStyle, Color } from '@indiekitai/lipgloss';

const style = NewStyle()
  .Foreground(Color('#FF69B4'))
  .Bold(true)
  .Border('rounded')
  .Padding(1, 2)
  .MarginTop(1);

console.log(style.Render('Hello World'));
```

## Features

- **Colors**: Hex, ANSI 256, named colors, adaptive (light/dark)
- **Text**: Bold, italic, underline, strikethrough, faint, blink
- **Layout**: Padding, margins, width/height, alignment (left/center/right)
- **Borders**: Rounded, thick, double, hidden, custom
- **Composition**: JoinHorizontal, JoinVertical, Place
