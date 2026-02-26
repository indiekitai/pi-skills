---
name: pg-inspect
description: PostgreSQL schema inspector. Extract detailed schema information including tables, columns, indexes, constraints, views, functions, enums, and sequences. Use when you need to understand a database structure or generate documentation.
---

# pg-inspect

Inspect PostgreSQL database schemas programmatically. TypeScript port of Python's schemainspect.

## Setup

```bash
npm install -g @indiekitai/pg-inspect
```

## Usage

```bash
# Full schema inspection
pg-inspect --url "postgres://user:pass@host:5432/db"

# JSON output
pg-inspect --url "postgres://user:pass@host:5432/db" --json

# Inspect specific objects
pg-inspect --url "..." --tables
pg-inspect --url "..." --views
pg-inspect --url "..." --functions
pg-inspect --url "..." --indexes
pg-inspect --url "..." --enums
pg-inspect --url "..." --sequences
pg-inspect --url "..." --constraints

# Filter by schema
pg-inspect --url "..." --schema public
```

## Output

Returns structured schema information. JSON mode provides complete schema metadata for code generation, migration planning, or documentation.
