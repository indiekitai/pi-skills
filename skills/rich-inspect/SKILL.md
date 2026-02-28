---
name: rich-inspect
description: Inspect JavaScript/TypeScript objects with colorful formatted output showing properties, methods, types, and docs. Port of Python Rich's inspect(). Use when debugging or exploring objects and modules.
---

# rich-inspect

Inspect any JS/TS object with rich terminal output. Port of Python Rich's inspect().

## Setup

```bash
npm install -g @indiekitai/rich-inspect
```

## Usage

```bash
# Inspect a JSON file
npx @indiekitai/rich-inspect data.json

# Inspect a JS module's exports
npx @indiekitai/rich-inspect ./my-module.js

# Show all members (including private)
npx @indiekitai/rich-inspect data.json --all

# Show only methods
npx @indiekitai/rich-inspect ./module.js --methods

# JSON output
npx @indiekitai/rich-inspect data.json --json
```

## MCP Tools

- `inspect_file` — Inspect a JS/TS file's exports
- `inspect_json` — Inspect a JSON structure
