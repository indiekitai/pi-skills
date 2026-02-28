---
name: clash-init
description: Generate Clash/mihomo proxy configuration files. Supports Shadowsocks, VMess, VLESS, Trojan, Hysteria2 protocols with built-in rule templates. Use when setting up or configuring proxy/VPN clients.
---

# clash-init

Clash/mihomo configuration generator. Interactive or CLI mode.

## Setup

```bash
npm install -g @indiekitai/clash-init
```

## Usage

```bash
# Interactive mode
npx @indiekitai/clash-init

# Shadowsocks config
npx @indiekitai/clash-init --ss --server 1.2.3.4 --port 443 --password "xxx" --cipher "2022-blake3-aes-128-gcm"

# With China direct template
npx @indiekitai/clash-init --ss --server 1.2.3.4 --port 443 --password "xxx" --template china

# Test connectivity
npx @indiekitai/clash-init --test

# Check WARP exit IP
npx @indiekitai/clash-init --check-warp

# JSON output
npx @indiekitai/clash-init --json
```

## MCP Tools

- `generate_config` — Generate Clash YAML config
- `test_proxy` — Test proxy server connectivity
- `check_ip` — Check current exit IP and ISP
