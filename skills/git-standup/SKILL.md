---
name: git-standup
description: Generate daily standup reports from git commit history. Scans single or multiple repos, groups by project, supports markdown and JSON output. Use when creating work summaries or daily standups.
---

# git-standup

Generate work standup reports from git history. Zero dependencies.

## Setup

```bash
npm install -g @indiekitai/git-standup
```

## Usage

```bash
# Yesterday's commits
npx @indiekitai/git-standup

# Custom time range
npx @indiekitai/git-standup --since "2 days ago"

# Scan multiple repos
npx @indiekitai/git-standup --dir ~/projects

# Filter by author
npx @indiekitai/git-standup --author "sen"

# Output formats
npx @indiekitai/git-standup --json
npx @indiekitai/git-standup --markdown
```

## MCP Tools

- `generate_standup` — Generate standup report for given repos/time range
- `list_repos` — Discover git repos in a directory
