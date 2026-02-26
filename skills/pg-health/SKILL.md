---
name: pg-health
description: PostgreSQL health checker. Run diagnostics on connection bloat, cache hit ratios, index usage, table stats, vacuum status, and replication lag. Use when analyzing PostgreSQL performance or troubleshooting database issues.
---

# pg-health

PostgreSQL health diagnostics tool. Checks 20+ metrics including connections, cache, indexes, bloat, locks, vacuum, and replication.

## Setup

```bash
npm install -g @indiekitai/pg-health
```

## Usage

```bash
# Full health check
pg-health --url "postgres://user:pass@host:5432/db"

# JSON output for programmatic use
pg-health --url "postgres://user:pass@host:5432/db" --json

# Check specific category
pg-health --url "..." --check connections
pg-health --url "..." --check cache
pg-health --url "..." --check indexes
pg-health --url "..." --check bloat
pg-health --url "..." --check vacuum
pg-health --url "..." --check replication
```

## Output

Returns health status (healthy/warning/critical) for each check with actionable recommendations. JSON mode outputs structured data suitable for dashboards or CI pipelines.
