<div align="center">

# Dotset Labs LLC

**Shield your CI from secret leaks.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.dotsetlabs.com-10b981?style=flat-square)](https://docs.dotsetlabs.com)
[![npm](https://img.shields.io/badge/npm-@dotsetlabs/shield-red?style=flat-square)](https://www.npmjs.com/package/@dotsetlabs/shield)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## 🛡️ Dotset Shield

**Real-time secret protection for CI/CD build logs.**

Secrets leak in build logs every day. Debug statements, error messages, and verbose logging expose API keys, tokens, and credentials. GitHub's built-in masking can't catch everything. GitGuardian scans *after* the breach.

**Dotset Shield intercepts output streams and redacts secrets in real-time — before they're ever exposed.**

```bash
npm install -g @dotsetlabs/shield

# Zero migration — use your existing .env files
dotset run -- npm start
# 🛡️  shield | mode: redact | secrets: 5 | providers: dotenv
```

---

## ✨ Key Features

| Feature | Description |
|:--------|:------------|
| **Zero Migration** | Works with your existing `.env` files immediately |
| **Provider-Agnostic** | Aggregates secrets from dotenv, AWS Secrets Manager, environment variables |
| **Three Protection Modes** | **Detect** (audit), **Redact** (replace), or **Block** (suppress) |
| **Streaming Redaction** | Line-buffered detection catches secrets split across chunks |
| **Cloud Analytics** | Track protection events and exposure patterns in your dashboard |
| **Custom Patterns** | Define proprietary secret patterns (Business tier) |
| **Slack/Discord/Webhook Alerts** | Get notified when secrets are detected |

---

## 🔐 Protection Modes

```bash
# Default (redact) — replace secrets with [REDACTED]
dotset run -- npm start

# Detect mode — log exposures without modification
dotset run --mode detect -- npm test

# Block mode — suppress lines containing secrets
dotset run --mode block -- npm test
```

**Output with redact mode:**
```
🛡️  shield | mode: redact | secrets: 5 | providers: dotenv

Starting server...
Connecting to database: [REDACTED]
Using API key: [REDACTED]
Server running on port 3000

🛡️  shield | exit: 0 | exposures: 2
```

---

## 🚀 CI/CD Integration

### GitHub Actions

Use our official action to protect any step in your workflow:

```yaml
- name: Run Protected Tests
  uses: dotsetlabs/shield@v1
  with:
    command: npm test
    token: ${{ secrets.DOTSET_TOKEN }}
    project-id: ${{ vars.DOTSET_PROJECT_ID }}
```

### Other CI Providers

Shield works with any CI/CD provider — GitLab, CircleCI, Jenkins, and more. See our [Integration Guides](https://docs.dotsetlabs.com/guides).

---

## ☁️ Cloud Analytics

Connect to your dashboard for visibility into protection events:

```bash
# Link your project
dotset link <project-id> --token <api-token>

# Runs are automatically tracked
dotset run -- npm test

# View analytics at app.dotsetlabs.com
```

---

## 💰 Pricing

| Plan | Price | Projects | Team | Runs | Retention |
|:-----|:------|:---------|:-----|:-----|:----------|
| **Free** | $0 | 1 | 3 | 100/mo | 7 days |
| **Pro** | $15/mo | 5 | 10 | Unlimited | 90 days |
| **Business** | $39/mo | Unlimited | Unlimited | Unlimited | 1 year |

**Flat pricing, not per-seat.** A team of 10 on Business pays $39/month total.

---

## 🔒 Trust & Security

**Your secrets never leave your machine.** Shield processes secrets entirely locally. When you enable cloud analytics, we only send anonymous metadata (counts, not values).

- 📖 [Audit the open-source CLI](https://github.com/dotsetlabs/shield)
- 🚫 Use `--no-telemetry` to disable all cloud reporting
- 🔨 [Build from source](https://github.com/dotsetlabs/shield) instead of npm

---

## 🔗 Links

- 🌐 [dotsetlabs.com](https://dotsetlabs.com) — Marketing site
- 📖 [docs.dotsetlabs.com](https://docs.dotsetlabs.com) — Documentation
- 🖥️ [app.dotsetlabs.com](https://app.dotsetlabs.com) — Dashboard
- 💻 [Demos](https://github.com/dotsetlabs/demos) — Interactive examples

<div align="center">

**Built with ❤️ for developers who care about security.**

© 2024 Dotset Labs LLC

</div>
