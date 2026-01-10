<div align="center">

# Dotset Labs

**Open-source security tools for AI-augmented development.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.dotsetlabs.com-10b981?style=flat-square)](https://docs.dotsetlabs.com)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## Defense in Depth for AI Development

AI assistants can read secrets, execute commands, and modify your system. We build the security tools that should exist but don't.

| Layer | Tool | Purpose |
|:------|:-----|:--------|
| **SCAN** | [Hardpoint](#hardpoint) | Detect Rules File Backdoor attacks in AI configs |
| **CONTROL** | [Overwatch](#overwatch) | MCP security proxy with tool shadowing detection |

---

## Hardpoint

**AI Configuration Security Scanner**

Detects the Rules File Backdoor attack — where AI config files contain hidden malicious instructions invisible to human review.

[![GitHub](https://img.shields.io/badge/source-dotsetlabs/hardpoint-10b981?style=flat-square)](https://github.com/dotsetlabs/hardpoint)

```bash
# Install
go install github.com/dotsetlabs/hardpoint/cmd/hardpoint@latest

# Scan AI config files
hardpoint scan

# Trust verified configs
hardpoint trust CLAUDE.md
```

### Detection Rules

| Rule | Category | Description |
|:-----|:---------|:------------|
| **AI-008** | Semantic Hijacking | Hidden instructions in comments/structure (80+ patterns) |
| **AI-005** | MCP Injection | Command injection in MCP configurations |
| **AI-004** | Encoded Content | Malicious patterns in Base64/encoded content |
| **GIT-001** | Git Hooks | Malicious commands in git hooks |
| **GIT-002** | Git Hooks | Credential exfiltration attempts |
| **GIT-003** | Git Hooks | Unexpected network access |
| **GIT-004** | Git Hooks | Obfuscated hook content |
| **GIT-005** | Git Config | Suspicious remote URLs |
| **GIT-006** | Git Config | Malicious credential helpers |

### AI Config Files Scanned

`.cursorrules` • `CLAUDE.md` • `AGENTS.md` • `mcp.json` • `.github/copilot-instructions.md` • `.windsurfrules`

### CLI Commands

`scan` • `fix` • `ignore` • `trust` • `verify` • `rules` • `init` • `hook` • `doctor`

---

## Overwatch

**MCP Security Proxy with Tool Shadowing Detection**

Intercept and control AI tool operations through the Model Context Protocol. Detect when malicious servers impersonate trusted tools.

[![npm](https://img.shields.io/npm/v/@dotsetlabs/overwatch?style=flat-square&label=npm)](https://www.npmjs.com/package/@dotsetlabs/overwatch)
[![GitHub](https://img.shields.io/badge/source-dotsetlabs/overwatch-06b6d4?style=flat-square)](https://github.com/dotsetlabs/overwatch)

```bash
npm install -g @dotsetlabs/overwatch

# Wrap any MCP server with policy enforcement
overwatch wrap npx @modelcontextprotocol/server-postgres

# Initialize configuration
overwatch init
```

### Core Features

| Feature | Description |
|:--------|:------------|
| **Policy Engine** | Declarative YAML policies with allow/deny/prompt actions |
| **Tool Shadowing Detection** | Schema hashing, collision detection, mutation monitoring (CVE-2025-6514) |
| **Session Approvals** | Time-limited grants with SQLite persistence |
| **Path-Based Rules** | Restrict filesystem access by glob patterns |
| **Audit Logging** | Complete trail with JSON, CSV, CEF export |

### CLI Commands

`wrap` • `start` • `sessions` • `logs` • `stats` • `init` • `policies` • `doctor`

### Works With

Claude Desktop • Cursor • Any MCP-compatible AI agent

---

## Trust & Security

**Your data never leaves your machine.** All tools are 100% local — no cloud, no telemetry, no account required.

| Tool | Language | Source | License |
|:-----|:---------|:-------|:--------|
| Hardpoint | Go | [github.com/dotsetlabs/hardpoint](https://github.com/dotsetlabs/hardpoint) | MIT |
| Overwatch | TypeScript | [github.com/dotsetlabs/overwatch](https://github.com/dotsetlabs/overwatch) | MIT |

---

## Links

- [dotsetlabs.com](https://dotsetlabs.com) — Website
- [docs.dotsetlabs.com](https://docs.dotsetlabs.com) — Documentation
- [Hardpoint](https://github.com/dotsetlabs/hardpoint) — AI Configuration Security Scanner
- [Overwatch](https://github.com/dotsetlabs/overwatch) — MCP Security Proxy

<div align="center">

**Built for developers working with AI.**

</div>
