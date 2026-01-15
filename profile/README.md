<div align="center">

# Dotset Labs

**Developer tools for AI-assisted development.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-0f172a?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.bellwether.sh-0f5132?style=flat-square)](https://docs.bellwether.sh)
[![License](https://img.shields.io/badge/license-MIT-22c55e?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## Our Products

We build tools that help developers work safely and confidently with AI assistants. From behavioral documentation to security scanning, our products provide visibility and control over AI-powered workflows.

| Layer | Tool | Purpose |
|:------|:-----|:--------|
| **DOCUMENT** | [Bellwether](#bellwether) | Behavioral documentation and drift detection for MCP servers |
| **SCAN** | [Hardpoint](#hardpoint) | Detect Rules File Backdoor attacks in AI configs |
| **CONTROL** | [Overwatch](#overwatch) | MCP security proxy with tool shadowing detection |

---

## Bellwether

**The Missing Docs for Every MCP Server**

Interview your MCP servers with AI to generate behavioral documentation. Know what tools actually do before you trust them with your workflows.

[![Website](https://img.shields.io/badge/bellwether.sh-0f5132?style=flat-square)](https://bellwether.sh)
[![npm](https://img.shields.io/npm/v/@dotsetlabs/bellwether?style=flat-square&label=npm)](https://www.npmjs.com/package/@dotsetlabs/bellwether)
[![GitHub](https://img.shields.io/badge/source-dotsetlabs/bellwether-0f5132?style=flat-square)](https://github.com/dotsetlabs/bellwether)

```bash
# Interview any MCP server
npx @dotsetlabs/bellwether interview

# Upload baselines to track drift
bellwether upload
```

### Features

| Feature | Description |
|:--------|:------------|
| **AGENTS.md Generation** | Comprehensive behavioral docs from AI-powered interviews |
| **Multi-Persona Testing** | Test from 4 perspectives: Technical Writer, Security Tester, QA Engineer, Novice User |
| **Drift Detection** | Track changes over time with baseline comparisons and alerts |
| **Security Analysis** | Identify potential vulnerabilities and data access patterns |
| **CI/CD Integration** | Block deployments when behavioral drift is detected |

### Cloud Platform

The open-source CLI works standalone. The optional [cloud platform](https://dashboard.bellwether.sh) adds:
- Baseline storage and version history
- Team collaboration
- Webhook notifications
- Verification badges

---

## Hardpoint

**AI Configuration Security Scanner**

Detects the Rules File Backdoor attack — where AI config files contain hidden malicious instructions invisible to human review.

[![GitHub](https://img.shields.io/badge/source-dotsetlabs/hardpoint-0f5132?style=flat-square)](https://github.com/dotsetlabs/hardpoint)

```bash
# Install
go install github.com/dotsetlabs/hardpoint/cmd/hardpoint@latest

# Scan AI config files
hardpoint scan

# Trust verified configs with HMAC-SHA256
hardpoint trust CLAUDE.md
```

### Detection Rules

| Rule | Category | Description |
|:-----|:---------|:------------|
| **AI-008** | Semantic Hijacking | Hidden instructions in comments/structure (80+ patterns) |
| **AI-005** | MCP Injection | Command injection in MCP configurations |
| **AI-004** | Encoded Content | Malicious patterns in Base64/encoded content |
| **GIT-001–006** | Git Security | Malicious hooks, credential exfiltration, suspicious remotes |

### AI Config Files Scanned

`.cursorrules` • `CLAUDE.md` • `AGENTS.md` • `mcp.json` • `.github/copilot-instructions.md` • `.windsurfrules` • `.aider*`

### Commands

`scan` • `fix` • `ignore` • `trust` • `verify` • `rules` • `init` • `hook` • `doctor`

---

## Overwatch

**MCP Security Proxy with Tool Shadowing Detection**

Intercept and control AI tool operations through the Model Context Protocol. Detect when malicious servers impersonate trusted tools.

[![npm](https://img.shields.io/npm/v/@dotsetlabs/overwatch?style=flat-square&label=npm)](https://www.npmjs.com/package/@dotsetlabs/overwatch)
[![GitHub](https://img.shields.io/badge/source-dotsetlabs/overwatch-0f5132?style=flat-square)](https://github.com/dotsetlabs/overwatch)

```bash
# Install
npm install -g @dotsetlabs/overwatch

# Wrap any MCP server with policy enforcement
overwatch wrap npx @modelcontextprotocol/server-postgres

# Initialize configuration
overwatch init
```

### Core Features

| Feature | Description |
|:--------|:------------|
| **Tool Shadowing Detection** | Schema hashing, collision detection, mutation monitoring (CVE-2025-6514) |
| **Policy Engine** | Declarative YAML policies with allow/deny/prompt actions |
| **Session Approvals** | Time-limited grants: once, 5 minutes, or session-based |
| **Path-Based Rules** | Restrict filesystem access by glob patterns |
| **Audit Logging** | Complete trail with JSON, CSV, CEF export for SIEM |

### Commands

`wrap` • `start` • `sessions` • `logs` • `stats` • `init` • `policies` • `doctor`

### Works With

Claude Desktop • Cursor • Any MCP-compatible AI agent

---

## Trust & Security

**Your data stays on your machine.** Hardpoint and Overwatch are 100% local — no cloud, no telemetry, no account required. Bellwether's CLI works offline; the cloud platform is optional.

| Tool | Language | License | Cloud Required |
|:-----|:---------|:--------|:---------------|
| Bellwether | TypeScript | MIT | Optional |
| Hardpoint | Go | MIT | No |
| Overwatch | TypeScript | MIT | No |

---

## Links

- [dotsetlabs.com](https://dotsetlabs.com) — Company Website
- [bellwether.sh](https://bellwether.sh) — Bellwether Product Site
- [docs.bellwether.sh](https://docs.bellwether.sh) — Documentation

<div align="center">

**Built for developers working with AI.**

*Washington, D.C.*

</div>
