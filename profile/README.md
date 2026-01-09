<div align="center">

# Dotset Labs

**Open-source security tools for the AI era.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.dotsetlabs.com-10b981?style=flat-square)](https://docs.dotsetlabs.com)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## Defense in Depth for AI Development

AI assistants create new attack surfaces. Our tools provide layered security across the development lifecycle:

| Stage | Tool | Purpose |
|:------|:-----|:--------|
| **Pre-install** | [Hardpoint](#hardpoint) | Scan your dev environment for hidden threats |
| **At Runtime** | [Tollgate](#tollgate) | Enforce policies on AI agent actions |
| **Detection** | [Deadfall](#deadfall) | Detect AI compromise with cognitive honeypots |
| **Unified** | [Dotset CLI](#dotset-cli) | All three tools in one command |

---

## Dotset CLI

**One CLI for the complete AI security stack.**

The unified `dotset` command bundles Hardpoint, Tollgate, and Deadfall — install once, protect everywhere.

[![npm](https://img.shields.io/npm/v/@dotsetlabs/dotset?style=flat-square&label=npm)](https://www.npmjs.com/package/@dotsetlabs/dotset)

```bash
npm install -g @dotsetlabs/dotset

# Run with full protection (scan + proxy + honeypots)
dotset run -- npx @modelcontextprotocol/server-postgres

# Or use individual commands
dotset scan                    # Hardpoint security scan
dotset wrap -- <server>        # Tollgate proxy
dotset trap cursor-rules       # Deadfall honeypot
dotset guard init              # Shell guardian
dotset serve --all             # Multi-server orchestration
```

### 19 Commands, Full Coverage

| Category | Commands |
|:---------|:---------|
| **Core** | `init`, `doctor`, `status`, `run` |
| **Scanning** | `scan`, `fix`, `baseline`, `integrity` |
| **MCP Proxy** | `wrap`, `serve`, `validate`, `guard`, `templates` |
| **Honeypots** | `trap` (with `status`, `metrics`) |
| **Audit** | `logs`, `stats`, `export` |

---

## Hardpoint

**Developer environment security scanner for the AI era.**

Hardpoint scans your development environment for threats that traditional security tools miss — malicious AI config files, prompt injection, hidden Unicode, and more.

[![GitHub](https://img.shields.io/badge/source-dotsetlabs/hardpoint-10b981?style=flat-square)](https://github.com/dotsetlabs/hardpoint)

```bash
# Install
go install github.com/dotsetlabs/hardpoint/cmd/hardpoint@latest

# Scan your environment
hardpoint scan

# Auto-fix certain issues
hardpoint fix AI-003 CLAUDE.md

# Manage suppression baselines
hardpoint baseline list
hardpoint baseline add AI-001 --reason "Known safe"
```

### Key Features

| Feature | Description |
|:--------|:------------|
| **AI Config Scanner** | Detects threats in `.cursorrules`, `CLAUDE.md`, `mcp.json` |
| **Hidden Unicode** | Finds invisible characters that can hide malicious instructions |
| **Prompt Injection** | Identifies attempts to override AI assistant behavior |
| **Shell Backdoors** | Scans `.bashrc`, `.zshrc` for suspicious commands |
| **Git Hook Analysis** | Checks for malicious git hooks |
| **SARIF Output** | GitHub Code Scanning integration |

---

## Tollgate

**Policy-based security proxy for MCP (Model Context Protocol) servers.**

Tollgate sits between AI agents and MCP servers, enforcing security policies before any tool is executed.

[![npm](https://img.shields.io/npm/v/@dotsetlabs/tollgate?style=flat-square&label=npm)](https://www.npmjs.com/package/@dotsetlabs/tollgate)
[![GitHub](https://img.shields.io/badge/source-dotsetlabs/tollgate-8b5cf6?style=flat-square)](https://github.com/dotsetlabs/tollgate)

```bash
npm install -g @dotsetlabs/tollgate

# Wrap any MCP server with protection
tollgate wrap npx @anthropic/mcp-server-fs ./

# Or use a config file for custom policies
tollgate start --server postgres
```

### Key Features

| Feature | Description |
|:--------|:------------|
| **Policy Engine** | Allow, deny, or prompt based on tool, arguments, and risk level |
| **Risk Analysis** | Smart analyzers for SQL, Filesystem, Shell, and HTTP API calls |
| **Server Scanner** | Scan any MCP server to discover tools and assess risks before use |
| **Templates** | Growing collection of policy templates for popular MCP servers |
| **Audit Logging** | Every tool invocation logged to SQLite with PII redaction |
| **Compliance** | Export logs in JSON, JSONL, CSV, or CEF formats |
| **Approval Methods** | Terminal prompts, interactive web UI, or webhook integration |

### Works With

- Claude Desktop
- Cursor
- Claude Code
- Any MCP-compatible AI agent

---

## Deadfall

**Cognitive honeypots for AI agent detection.**

Deadfall detects AI agent compromise by exploiting their instruction-following behavior. Trapped files instruct agents to call a verification tool — which triggers an alert.

[![GitHub](https://img.shields.io/badge/source-dotsetlabs/deadfall-f59e0b?style=flat-square)](https://github.com/dotsetlabs/deadfall)

```bash
# Install
go install github.com/dotsetlabs/deadfall/cmd/deadfall@latest

# Initialize in your project
deadfall init

# Create trap files
deadfall trap cursor-rules      # .cursorrules for Cursor
deadfall trap claude-context    # CLAUDE.md for Claude
deadfall trap mcp-config        # mcp.json honeypot

# Verify your setup
deadfall test

# Start the Honey-MCP server
deadfall serve
```

### Key Features

| Feature | Description |
|:--------|:------------|
| **Cognitive Traps** | Exploit AI instruction-following to detect compromise |
| **AI-Specific Types** | Traps for Cursor, Claude, Copilot, MCP clients |
| **Honey-MCP Server** | Honeypot tools that attract malicious agents |
| **Token Correlation** | Alerts include which file was read |
| **Multi-Channel Alerts** | Desktop, log file, webhook delivery |

---

## Trust & Security

**Your data never leaves your machine.** All Dotset Labs tools are 100% local — no cloud, no telemetry, no account required.

- [Hardpoint source code](https://github.com/dotsetlabs/hardpoint)
- [Tollgate source code](https://github.com/dotsetlabs/tollgate)
- [Deadfall source code](https://github.com/dotsetlabs/deadfall)

---

## Links

- [dotsetlabs.com](https://dotsetlabs.com) — Website
- [docs.dotsetlabs.com](https://docs.dotsetlabs.com) — Documentation
- [Dotset CLI on npm](https://www.npmjs.com/package/@dotsetlabs/dotset) — Unified CLI
- [Hardpoint GitHub](https://github.com/dotsetlabs/hardpoint) — Dev environment scanner
- [Tollgate GitHub](https://github.com/dotsetlabs/tollgate) — MCP security proxy
- [Deadfall GitHub](https://github.com/dotsetlabs/deadfall) — Cognitive honeypots

<div align="center">

**Built for developers working with AI.**

</div>
