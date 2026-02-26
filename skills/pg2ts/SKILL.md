---
name: pg2ts
description: Generate TypeScript types from PostgreSQL schemas. Connects to a database and outputs TypeScript interfaces for all tables. Use when setting up type-safe database access or keeping types in sync with schema.
---

# pg2ts

Generate TypeScript type definitions from PostgreSQL database schemas.

## Setup

```bash
pip install pg2ts  # or just download pg2ts.py
```

## Usage

```bash
# Generate types for all tables
python pg2ts.py --url "postgres://user:pass@host:5432/db"

# Output to file
python pg2ts.py --url "..." -o types.ts

# JSON metadata output
python pg2ts.py --url "..." --json

# Filter by schema
python pg2ts.py --url "..." --schema public

# Include enums
python pg2ts.py --url "..." --enums
```

## Output

Generates TypeScript interfaces matching database tables, with proper type mappings (int→number, text→string, jsonb→Record, etc.). JSON mode outputs metadata about the generated types.
