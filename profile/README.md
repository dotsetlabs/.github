<div align="center">

# Dotset Labs

**Open-source security tools for the AI era.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.dotsetlabs.com-10b981?style=flat-square)](https://docs.dotsetlabs.com)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## Tollgate

**Policy-based security proxy for MCP (Model Context Protocol) servers.**

Tollgate sits between AI agents and MCP servers, enforcing security policies before any tool is executed.

[![npm](https://img.shields.io/npm/v/@dotsetlabs/tollgate?style=flat-square&label=npm)](https://www.npmjs.com/package/@dotsetlabs/tollgate)
[![GitHub](https://img.shields.io/badge/source-dotsetlabs/tollgate-blue?style=flat-square)](https://github.com/dotsetlabs/tollgate)

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
| **Templates** | 50+ pre-built policy templates for popular MCP servers |
| **Audit Logging** | Every tool invocation logged to SQLite with PII redaction |
| **Compliance** | Export logs in JSON, CSV, SARIF, or CEF formats |

### Works With

- Claude Desktop
- Cursor
- Claude Code
- Any MCP-compatible AI agent

---

## Hardpoint

**Developer environment security scanner for the AI era.**

Hardpoint scans your development environment for threats that traditional security tools miss — malicious AI config files, prompt injection, hidden Unicode, and more.

[![GitHub](https://img.shields.io/badge/source-dotsetlabs/hardpoint-blue?style=flat-square)](https://github.com/dotsetlabs/hardpoint)

```bash
# Install via Homebrew
brew install dotsetlabs/tap/hardpoint

# Scan your environment
hardpoint scan

# Auto-fix certain issues
hardpoint fix AI-003 CLAUDE.md
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

### What It Catches

- Instruction overrides in AI config files
- Zero-width and invisible Unicode characters
- Hardcoded secrets and credentials
- Suspicious shell aliases and functions
- Malicious git hooks

---

## Trust & Security

**Your data never leaves your machine.** Both Tollgate and Hardpoint are 100% local — no cloud, no telemetry, no account required.

- [Tollgate source code](https://github.com/dotsetlabs/tollgate)
- [Hardpoint source code](https://github.com/dotsetlabs/hardpoint)

---

## Links

- [dotsetlabs.com](https://dotsetlabs.com) — Website
- [docs.dotsetlabs.com](https://docs.dotsetlabs.com) — Documentation
- [Tollgate GitHub](https://github.com/dotsetlabs/tollgate) — MCP security proxy
- [Hardpoint GitHub](https://github.com/dotsetlabs/hardpoint) — Dev environment scanner

<div align="center">

**Built for developers working with AI.**

</div>
