---
name: llm-context
description: Scan a codebase and estimate LLM context usage. Shows file sizes, token counts, and identifies large files that may blow context windows. Use when preparing codebases for AI coding agents or optimizing what to include in prompts.
---

# llm-context

Analyze codebase context size for LLM consumption.

## Setup

```bash
npm install -g @indiekitai/llm-context
```

## Usage

```bash
# Scan current directory
npx @indiekitai/llm-context .

# JSON output
npx @indiekitai/llm-context . --json

# Set context limit (tokens)
npx @indiekitai/llm-context . --limit 128000

# Exclude patterns
npx @indiekitai/llm-context . --exclude "*.test.ts" --exclude "dist/**"

# Show top N largest files
npx @indiekitai/llm-context . --top 20
```

## Output

- Total token count estimate
- Per-file token breakdown
- Files exceeding context budget
- Suggestions for reducing context size
