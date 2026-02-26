---
name: pg-top
description: PostgreSQL real-time activity monitor. Show running queries, locks, blocking chains, and per-database stats. Use when debugging slow queries, investigating locks, or monitoring database load.
---

# pg-top

Real-time PostgreSQL activity monitor. TypeScript port of Python's pg_activity.

## Setup

```bash
npm install -g @indiekitai/pg-top
```

## Usage

```bash
# Show current activity
pg-top --url "postgres://user:pass@host:5432/db"

# JSON output (snapshot mode)
pg-top --url "..." --json

# Show only active queries
pg-top --url "..." --active

# Show locks and blocking chains
pg-top --url "..." --locks

# Show database-level stats
pg-top --url "..." --stats

# Filter by duration (show queries running > 5s)
pg-top --url "..." --min-duration 5
```

## Output

Displays running queries with PID, duration, state, and SQL text. Lock mode shows blocking chains. JSON mode provides structured data for automation.
