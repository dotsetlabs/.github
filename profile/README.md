<div align="center">

# Dotset Labs

**Shield your CI from secret leaks.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.dotsetlabs.com-10b981?style=flat-square)](https://docs.dotsetlabs.com)
[![npm](https://img.shields.io/badge/npm-@dotsetlabs/shield-red?style=flat-square)](https://www.npmjs.com/package/@dotsetlabs/shield)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## 🛡️ dotset shield

**Real-time secret protection for CI/CD build logs.**

Secrets leak in build logs every day. Debug statements, error messages, and verbose logging expose API keys, tokens, and credentials. GitHub's built-in masking can't catch everything. GitGuardian scans *after* the breach.

**dotset shield intercepts output streams and redacts secrets in real-time — before they're ever exposed.**

```bash
npm install -g @dotsetlabs/shield

dotset init                             # Initialize encryption
dotset secrets set API_KEY "sk-..."     # Store encrypted secret
dotset run -- npm start                 # Run with protection (redact is default)
```

---

## ✨ Key Features

| Feature | Description |
|:--------|:------------|
| **Three Protection Modes** | **Detect** (audit), **Redact** (replace, default), or **Block** (suppress) |
| **AES-256-GCM Encryption** | Zero-knowledge secrets — we never see your values |
| **Scoped Secrets** | Separate development, staging, and production |
| **Cloud Analytics** | Track protection events in your dashboard |
| **Custom Patterns** | Define proprietary secret patterns (Business) |
| **Email & Webhook Alerts** | Get notified when secrets are blocked |

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
Connecting to database: [REDACTED]
Using API key: [REDACTED]
Server running on port 3000
```

---

## 🚀 Local CI

Run your GitHub Actions workflows locally:

```bash
dotset ci --list                  # See available jobs
dotset ci build test              # Run specific jobs
dotset ci --mode redact           # Run with protection
```

---

## 💰 Pricing

| Plan | Price | Projects | Runs | Retention |
|:-----|:------|:---------|:-----|:----------|
| **Free** | $0 | 1 | 100/month | 7 days |
| **Pro** | $15/mo | 5 | Unlimited | 90 days |
| **Business** | $39/mo | Unlimited | Unlimited | 1 year |

**Pro** adds email alerts and CI reports. **Business** adds custom patterns and webhook alerts.

---

## 🔗 Links

- 🌐 [dotsetlabs.com](https://dotsetlabs.com)
- 📖 [docs.dotsetlabs.com](https://docs.dotsetlabs.com)
- 🖥️ [app.dotsetlabs.com](https://app.dotsetlabs.com)
- 💻 [Demo](https://github.com/dotsetlabs/demos)

<div align="center">

**Built with ❤️ for developers who care about security.**

</div>
