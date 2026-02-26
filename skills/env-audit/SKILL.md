---
name: env-audit
description: Scan codebases for environment variable usage and generate documented .env.example files. Supports Python, Node, Go, Rust, Ruby, Shell, Docker. Use when auditing env vars, creating .env templates, or checking for undocumented variables in CI.
---

# env-audit

Scan source code for environment variable references and generate documented templates.

## Setup

```bash
pip install env-audit  # or just download env_audit.py
```

## Usage

```bash
# Scan current directory, output .env.example format
python env_audit.py .

# JSON output
python env_audit.py . --json

# Stats only
python env_audit.py . --stats

# CI check mode (exit 1 if undocumented vars)
python env_audit.py . --check

# Output to file
python env_audit.py . -o .env.example

# Alternative output formats
python env_audit.py . --format typescript
python env_audit.py . --format zod
```

## Supported Languages

Python, JavaScript/TypeScript (Node), Go, Rust, Ruby, Shell/Bash, Docker

## Output

Categorized environment variables with:
- Required vs optional detection
- Sensitive variable marking (passwords, keys, secrets)
- Default value extraction
- File location references
