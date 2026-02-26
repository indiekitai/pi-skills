---
name: pg-diff
description: PostgreSQL schema diff and migration generator. Compare two database schemas and generate SQL migration statements. Use when planning migrations, reviewing schema changes, or syncing environments.
---

# pg-diff

Compare PostgreSQL schemas and generate migration SQL. TypeScript port of Python's migra.

## Setup

```bash
npm install -g @indiekitai/pg-diff
```

## Usage

```bash
# Compare two databases
pg-diff --from "postgres://user:pass@host/db1" --to "postgres://user:pass@host/db2"

# JSON output
pg-diff --from "..." --to "..." --json

# Generate migration SQL only
pg-diff --from "..." --to "..." --sql

# Exclude specific object types
pg-diff --from "..." --to "..." --ignore-indexes
```

## Output

Shows schema differences (added/removed/changed tables, columns, indexes, etc.) and generates the SQL needed to migrate from source to target schema.
