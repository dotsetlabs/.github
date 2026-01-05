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

---

## Hardpoint

**Developer environment security scanner for the AI era.**

Hardpoint scans your development environment for threats that traditional security tools miss — malicious AI config files, prompt injection, hidden Unicode, and more.

[![GitHub](https://img.shields.io/badge/source-dotsetlabs/hardpoint-10b981?style=flat-square)](https://github.com/dotsetlabs/hardpoint)

```bash
# Install via Homebrew
brew install dotsetlabs/tap/hardpoint

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

[![npm](https://img.shields.io/npm/v/@anthropic/mcp-server-filesystem?style=flat-square&label=example%20package)](https://www.npmjs.com/package/@anthropic/mcp-server-filesystem)
[![GitHub](https://img.shields.io/badge/source-dotsetlabs/countersign-06b6d4?style=flat-square)](https://github.com/dotsetlabs/countersign)

```bash
# Install globally
npm install -g @dotsetlabs/countersign

# Verify a package before installing
countersign verify @anthropic/mcp-server-filesystem

# Check trust level
countersign trust @modelcontextprotocol/server-postgres

# Install automatic verification hooks
countersign hook install --min-score 80
```

### Key Features

| Feature | Description |
|:--------|:------------|
| **Signature Verification** | Cryptographically verify package signatures via Sigstore |
| **Trust Scoring** | 0-100 score based on provenance, publisher history, and audit status |
| **Publisher Reputation** | Track publisher history and detect account compromises |
| **npm Integration** | Seamless verification for npm-hosted MCP servers |
| **CI/CD Ready** | Integrate into pipelines with exit codes and JSON output |
| **Offline Support** | Cache verification results for air-gapped environments |

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

## Trust & Security

**Your data never leaves your machine.** All Dotset Labs tools are 100% local — no cloud, no telemetry, no account required.

- [Hardpoint source code](https://github.com/dotsetlabs/hardpoint)
- [Countersign source code](https://github.com/dotsetlabs/countersign)
- [Tollgate source code](https://github.com/dotsetlabs/tollgate)

---

## Links

- [dotsetlabs.com](https://dotsetlabs.com) — Website
- [docs.dotsetlabs.com](https://docs.dotsetlabs.com) — Documentation
- [Hardpoint GitHub](https://github.com/dotsetlabs/hardpoint) — Dev environment scanner
- [Countersign GitHub](https://github.com/dotsetlabs/countersign) — Package provenance verification
- [Tollgate GitHub](https://github.com/dotsetlabs/tollgate) — MCP security proxy

<div align="center">

**Built for developers working with AI.**

</div>
