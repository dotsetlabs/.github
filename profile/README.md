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
| **At Install** | [Countersign](#countersign) | Verify package provenance before installation |
| **At Runtime** | [Tollgate](#tollgate) | Enforce policies on AI agent actions |
| **Detection** | [Deadfall](#deadfall) | Trap intruders with honeypots and canary tokens |

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

## Countersign

**Package provenance verification for MCP servers.**

Countersign verifies that MCP server packages are signed by trusted publishers, protecting you from supply chain attacks before installation.

[![GitHub](https://img.shields.io/badge/source-dotsetlabs/countersign-06b6d4?style=flat-square)](https://github.com/dotsetlabs/countersign)

```bash
# Install
go install github.com/dotsetlabs/countersign/cmd/countersign@latest

# Verify a package before installing
countersign verify @anthropic/mcp-server-filesystem

# Check trust level
countersign trust @modelcontextprotocol/server-postgres
```

### Key Features

| Feature | Description |
|:--------|:------------|
| **Signature Verification** | Cryptographically verify package signatures via Sigstore |
| **Trust Scoring** | 0-100 score based on provenance, publisher history, and audit status |
| **Publisher Reputation** | Track publisher history and detect account compromises |
| **npm Integration** | Seamless verification for npm-hosted MCP servers |
| **CI/CD Ready** | Integrate into pipelines with exit codes and JSON output |

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
| **Templates** | 50+ pre-built policy templates for popular MCP servers |
| **Audit Logging** | Every tool invocation logged to SQLite with PII redaction |
| **Compliance** | Export logs in JSON, CSV, SARIF, or CEF formats |
| **Approval Methods** | Terminal prompts, interactive web UI, or webhook integration |

### Works With

- Claude Desktop
- Cursor
- Claude Code
- Any MCP-compatible AI agent

---

## Deadfall

**AI agent honeypot and canary token generator.**

Deadfall generates deceptive artifacts — fake credentials, API keys, and MCP tools — to detect when AI agents or intruders access sensitive-looking resources.

[![GitHub](https://img.shields.io/badge/source-dotsetlabs/deadfall-f59e0b?style=flat-square)](https://github.com/dotsetlabs/deadfall)

```bash
# Install
go install github.com/dotsetlabs/deadfall/cmd/deadfall@latest

# Initialize in your project
deadfall init

# Generate canary files
deadfall generate env .env.production
deadfall generate mcp .mcp-admin.json

# Watch for access
deadfall watch
```

### Key Features

| Feature | Description |
|:--------|:------------|
| **Canary Tokens** | Generate fake `.env`, SSH keys, AWS credentials, and more |
| **MCP Honeypots** | Fake MCP tool configs that attract malicious agents |
| **File Watching** | Real-time alerts when canaries are accessed |
| **Webhook Alerts** | Send notifications to Slack, email, or custom endpoints |

---

## Trust & Security

**Your data never leaves your machine.** All Dotset Labs tools are 100% local — no cloud, no telemetry, no account required.

- [Hardpoint source code](https://github.com/dotsetlabs/hardpoint)
- [Countersign source code](https://github.com/dotsetlabs/countersign)
- [Tollgate source code](https://github.com/dotsetlabs/tollgate)
- [Deadfall source code](https://github.com/dotsetlabs/deadfall)

---

## Links

- [dotsetlabs.com](https://dotsetlabs.com) — Website
- [docs.dotsetlabs.com](https://docs.dotsetlabs.com) — Documentation
- [Hardpoint GitHub](https://github.com/dotsetlabs/hardpoint) — Dev environment scanner
- [Countersign GitHub](https://github.com/dotsetlabs/countersign) — Package provenance verification
- [Tollgate GitHub](https://github.com/dotsetlabs/tollgate) — MCP security proxy
- [Deadfall GitHub](https://github.com/dotsetlabs/deadfall) — Honeypot and canary tokens

<div align="center">

**Built for developers working with AI.**

</div>
