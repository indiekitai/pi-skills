---
name: pgcomplete
description: Context-aware SQL auto-completion engine for PostgreSQL. Provides smart completions for tables, columns, functions, schemas based on SQL context. Use when building SQL editors or interactive database tools.
---

# pgcomplete

PostgreSQL auto-completion engine. TypeScript port of pgcli's completer.

## Setup

```bash
npm install -g @indiekitai/pgcomplete
```

## Usage

```bash
# Interactive mode (connect to database)
npx @indiekitai/pgcomplete --url "postgres://user:pass@host:5432/db"

# One-shot completion
npx @indiekitai/pgcomplete --url "..." --complete "SELECT * FROM u"

# JSON output
npx @indiekitai/pgcomplete --url "..." --complete "SELECT " --json
```

## MCP Tools

- `complete` — Get completions for a SQL fragment
- `list_tables` — List all tables in database
- `list_columns` — List columns for a table
- `list_functions` — List available functions
- `list_schemas` — List schemas
