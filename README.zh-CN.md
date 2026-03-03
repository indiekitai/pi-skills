[English](README.md) | [中文](README.zh-CN.md)

# @indiekitai/pi-skills

为 [Pi](https://pi.dev)、[Claude Code](https://docs.anthropic.com/en/docs/claude-code)、[Codex CLI](https://github.com/openai/codex) 和 [Amp](https://amp.dev) 打造的开发者工具技能包。

## 安装

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

## 可用技能

### PostgreSQL 套件
| 技能 | 描述 |
|------|------|
| [pg-health](skills/pg-health/SKILL.md) | 数据库健康诊断（20+ 项检查） |
| [pg-inspect](skills/pg-inspect/SKILL.md) | Schema 检查器（表、索引、函数、枚举） |
| [pg-diff](skills/pg-diff/SKILL.md) | Schema 对比与迁移 SQL 生成 |
| [pg-top](skills/pg-top/SKILL.md) | 实时查询与锁监控 |
| [pg2ts](skills/pg2ts/SKILL.md) | 从 Schema 生成 TypeScript 类型 |

### 开发工具
| 技能 | 描述 |
|------|------|
| [env-audit](skills/env-audit/SKILL.md) | 扫描代码库中的环境变量，生成 .env.example |
| [throttled](skills/throttled/SKILL.md) | 限流工具（固定窗口/滑动窗口/令牌桶/GCRA） |
| [llm-context](skills/llm-context/SKILL.md) | 估算代码库的 LLM 上下文使用量 |
| [just](skills/just/SKILL.md) | 任务运行器（Justfile 格式，比 make 更好用） |
| [git-standup](skills/git-standup/SKILL.md) | 从 git 历史生成每日站会报告 |
| [clash-init](skills/clash-init/SKILL.md) | 生成 Clash/mihomo 代理配置（SS、VMess、VLESS、Trojan、Hysteria2） |
| [pgcomplete](skills/pgcomplete/SKILL.md) | PostgreSQL 上下文感知 SQL 自动补全 |
| [rich-inspect](skills/rich-inspect/SKILL.md) | 以丰富的终端输出检查 JS/TS 对象 |

### 自动化
| 技能 | 描述 |
|------|------|
| [trello-autopilot](skills/trello-autopilot/SKILL.md) | 用 Coding Agent 自动修复 Trello Bug 卡片 |

### 终端渲染
| 技能 | 描述 |
|------|------|
| [glamour](skills/glamour/SKILL.md) | 在终端中渲染 Markdown，支持主题 |
| [lipgloss](skills/lipgloss/SKILL.md) | 类 CSS 的终端文本样式 |

## 每个工具还提供

- **CLI** 命令行工具，支持 `--json` 输出
- **MCP Server**，可直接与 AI Agent 集成
- **npm 包**，发布在 `@indiekitai/` scope 下

## License

MIT
