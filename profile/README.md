<div align="center">

# Dotset Labs

**Open-source developer tools for secure CI/CD and AI agent governance.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.dotsetlabs.com-10b981?style=flat-square)](https://docs.dotsetlabs.com)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## Mantle

**Free, open-source secret protection for CI/CD build logs.**

Mantle intercepts output streams and redacts secrets in real-time — before they're ever exposed in your logs.

[![npm](https://img.shields.io/npm/v/@dotsetlabs/mantle?style=flat-square&label=npm)](https://www.npmjs.com/package/@dotsetlabs/mantle)
[![GitHub](https://img.shields.io/badge/source-dotsetlabs/mantle-blue?style=flat-square)](https://github.com/dotsetlabs/mantle)

```bash
npm install -g @dotsetlabs/mantle

# Run with protection (zero config)
mantle run -- npm start
# mantle | mode: redact | secrets: 5 | providers: dotenv
```

### Key Features

| Feature | Description |
|:--------|:------------|
| **Zero Config** | Works with your existing `.env` files immediately |
| **Streaming Protection** | Line-buffered redaction catches secrets split across chunks |
| **Three Modes** | **Detect** (audit), **Redact** (replace), or **Block** (suppress) |
| **100+ Patterns** | AWS, GitHub, Stripe, OpenAI, and more built-in |
| **Compliance Reports** | Generate HTML/SARIF reports for audit trails |

### GitHub Action

```yaml
steps:
  - uses: dotsetlabs/mantle@v1
  - run: npm test
```

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

## Trust & Security

**Your data never leaves your machine.** Both Mantle and Tollgate are 100% local — no cloud, no telemetry, no account required.

- [Mantle source code](https://github.com/dotsetlabs/mantle)
- [Tollgate source code](https://github.com/dotsetlabs/tollgate)

---

## Links

- [dotsetlabs.com](https://dotsetlabs.com) — Website
- [docs.dotsetlabs.com](https://docs.dotsetlabs.com) — Documentation
- [Mantle GitHub](https://github.com/dotsetlabs/mantle) — Secret detection CLI
- [Tollgate GitHub](https://github.com/dotsetlabs/tollgate) — MCP security proxy

<div align="center">

**Built for developers who care about security.**

</div>
