# @indiekitai/pi-skills

Developer tools as agent skills for [Pi](https://pi.dev), [Claude Code](https://docs.anthropic.com/en/docs/claude-code), [Codex CLI](https://github.com/openai/codex), and [Amp](https://amp.dev).

## Install

### Pi
```bash
pi install npm:@indiekitai/pi-skills
```

### Claude Code
```bash
git clone https://github.com/indiekitai/pi-skills ~/indiekit-skills
mkdir -p ~/.claude/skills
for skill in ~/indiekit-skills/skills/*/; do
  ln -s "$skill" ~/.claude/skills/$(basename "$skill")
done
```

### Codex CLI
```bash
git clone https://github.com/indiekitai/pi-skills ~/.codex/skills/indiekit-skills
```

## Available Skills

### PostgreSQL Suite
| Skill | Description |
|-------|-------------|
| [pg-health](skills/pg-health/SKILL.md) | Database health diagnostics (20+ checks) |
| [pg-inspect](skills/pg-inspect/SKILL.md) | Schema inspector (tables, indexes, functions, enums) |
| [pg-diff](skills/pg-diff/SKILL.md) | Schema diff & migration SQL generator |
| [pg-top](skills/pg-top/SKILL.md) | Real-time query & lock monitor |
| [pg2ts](skills/pg2ts/SKILL.md) | Generate TypeScript types from schemas |

### Developer Tools
| Skill | Description |
|-------|-------------|
| [env-audit](skills/env-audit/SKILL.md) | Scan codebases for env vars, generate .env.example |
| [throttled](skills/throttled/SKILL.md) | Rate limiting (fixed/sliding window, token bucket, GCRA) |
| [llm-context](skills/llm-context/SKILL.md) | Estimate LLM context usage for codebases |
| [just](skills/just/SKILL.md) | Task runner (Justfile format, like make but better) |
| [git-standup](skills/git-standup/SKILL.md) | Generate daily standup reports from git history |
| [clash-init](skills/clash-init/SKILL.md) | Generate Clash/mihomo proxy configs (SS, VMess, VLESS, Trojan, Hysteria2) |
| [pgcomplete](skills/pgcomplete/SKILL.md) | Context-aware SQL auto-completion for PostgreSQL |
| [rich-inspect](skills/rich-inspect/SKILL.md) | Inspect JS/TS objects with rich terminal output |

### Automation
| Skill | Description |
|-------|-------------|
| [trello-autopilot](skills/trello-autopilot/SKILL.md) | Auto-fix Trello bug cards with coding agents |

### Terminal Rendering
| Skill | Description |
|-------|-------------|
| [glamour](skills/glamour/SKILL.md) | Render Markdown in terminals with themes |
| [lipgloss](skills/lipgloss/SKILL.md) | CSS-like terminal text styling |

## Each tool also has

- **CLI** with `--json` output
- **MCP Server** for direct AI agent integration
- **npm package** under `@indiekitai/` scope

## License

MIT
