---
name: trello-autopilot
description: Automatically scan Trello boards for bug cards, invoke a coding agent to fix them, and move cards to Done. Use when automating bug triage and fix workflows with Trello.
---

# trello-autopilot

Trello bug auto-fix pipeline. Scans a board for bug cards, invokes Claude Code to fix, moves cards when done.

## Setup

```bash
npm install -g @indiekitai/trello-autopilot
export TRELLO_API_KEY="your-key"
export TRELLO_TOKEN="your-token"
```

## Usage

```bash
# Scan and fix bugs
npx @indiekitai/trello-autopilot --board "MyProject" --list "Bugs" --done "Done" --repo /path/to/repo

# Dry run (scan only, don't fix)
npx @indiekitai/trello-autopilot --board "MyProject" --list "Bugs" --dry-run

# JSON output
npx @indiekitai/trello-autopilot --board "MyProject" --list "Bugs" --json
```

## MCP Tools

- `scan_bugs` — List bug cards from a Trello board/list
- `fix_bug` — Invoke coding agent to fix a specific bug card
- `move_card` — Move a card to another list
