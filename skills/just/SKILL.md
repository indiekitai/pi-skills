---
name: just
description: JavaScript/TypeScript task runner inspired by casey/just. Define tasks in a Justfile with dependencies, arguments, and shell recipes. Use when you need a simple, modern alternative to make/npm scripts for project automation.
---

# just-ts

Task runner for JavaScript/TypeScript projects. Port of casey/just (Rust).

## Setup

```bash
npm install -g @indiekitai/just-ts
```

## CLI Usage

```bash
# Run default task
just

# Run specific task
just build
just test
just deploy staging

# List available tasks
just --list

# JSON output (task definitions)
just --json

# Dry run
just --dry-run build
```

## Justfile Format

Create a `Justfile` in your project root:

```just
# Build the project
build:
  npm run build

# Run tests with optional filter
test filter="":
  npm test -- {{filter}}

# Deploy to environment
deploy env: build test
  ./scripts/deploy.sh {{env}}

# Clean build artifacts
clean:
  rm -rf dist node_modules
```

## Features

- **Dependencies**: Tasks can depend on other tasks
- **Arguments**: Pass arguments to tasks with default values
- **Shell recipes**: Each line runs in a shell
- **Comments**: `#` comments become task descriptions in `--list`
