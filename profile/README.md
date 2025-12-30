<div align="center">

# Dotset Labs LLC

**Unified secret protection and infrastructure validation.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.dotsetlabs.com-10b981?style=flat-square)](https://docs.dotsetlabs.com)
[![npm](https://img.shields.io/badge/npm-@dotsetlabs/cli-red?style=flat-square)](https://www.npmjs.com/package/@dotsetlabs/cli)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## 🛡️ Dotset Shield

**Real-time secret protection for CI/CD build logs.**

Shield intercepts output streams and redacts secrets in real-time — before they're ever exposed.

```bash
npm install -g @dotsetlabs/cli

# 1. Link your project (Unified)
dotset link <project-id> --token <token>

# 2. Run with protection (Zero migration)
dotset shield run -- npm start
# 🛡️  shield | mode: redact | secrets: 5 | providers: dotenv
```

---

## 🔍 Dotset Preflight

**Active infrastructure validation for modern dev teams.**

Preflight ensures your services (DBs, Caches, APIs) are reachable *before* your app starts.

```bash
# Validate your local environment connectivity
dotset preflight check

# Upload your schema to the cloud
dotset preflight push

# 🔍 Preflight Check
# 📡 Running Active Probes...
#   • DATABASE_URL (postgres)... PASSED
#   • REDIS_URL (redis)... PASSED
```

---

## ✨ Key Features

| Feature | Description |
|:--------|:------------|
| **Zero Migration** | Works with your existing `.env` files immediately |
| **Active Probes** | Validate Postgres, Redis, MongoDB, AWS, and HTTP connectivity |
| **Streaming Protection** | Line-buffered redaction catches secrets split across chunks |
| **Three Protection Modes** | **Detect** (audit), **Redact** (replace), or **Block** (suppress) |
| **Cloud Analytics** | Track protection events and exposure patterns in your dashboard |
| **Unified CLI** | One package for both Shield and Preflight: `@dotsetlabs/cli` |

---

## 🚀 CI/CD Integration

### GitHub Actions

Use our official actions to protect and validate your workflows:

```yaml
- name: Preflight Check
  uses: dotsetlabs/cli/actions/preflight@v1

- name: Run Protected Tests
  uses: dotsetlabs/cli/actions/shield@v1
  with:
    command: npm test
    token: ${{ secrets.DOTSET_TOKEN }}
    project-id: ${{ vars.DOTSET_PROJECT_ID }}
```

---

## 💰 Pricing

| Plan | Price | Projects | Team | Runs | Retention |
|:-----|:------|:---------|:-----|:-----|:----------|
| **Free** | $0 | 1 | 3 | 100/mo | 7 days |
| **Pro** | $15/mo | 5 | 10 | Unlimited | 90 days |
| **Business** | $39/mo | Unlimited | Unlimited | Unlimited | 1 year |

---

## 🔒 Trust & Security

**Your secrets never leave your machine.** Shield processes secrets entirely locally. When you enable cloud analytics, we only send anonymous metadata (counts, not values).

- 📖 [Audit the open-source CLI](https://github.com/dotsetlabs/cli)
- 🚫 Use `--no-telemetry` to disable all cloud reporting
- hammer [Build from source](https://github.com/dotsetlabs/cli) instead of npm

---

## 🔗 Links

- 🌐 [dotsetlabs.com](https://dotsetlabs.com) — Marketing site
- 📖 [docs.dotsetlabs.com](https://docs.dotsetlabs.com) — Documentation
- 🖥️ [app.dotsetlabs.com](https://app.dotsetlabs.com) — Dashboard
- 💻 [Demos](https://github.com/dotsetlabs/demos) — Interactive examples

<div align="center">

**Built with ❤️ for developers who care about security.**

© 2025 Dotset Labs LLC

</div>
