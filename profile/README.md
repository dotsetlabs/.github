<div align="center">

# dotset labs

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

dotset init                                    # Initialize encryption
dotset secrets set API_KEY "sk-..."            # Store encrypted secret
dotset run --mode redact -- npm start          # Run with protection
```

---

## ✨ Key Features

| Feature | Description |
|:--------|:------------|
| **Three Protection Modes** | **Detect** (audit), **Redact** (replace), or **Block** (suppress) |
| **AES-256-GCM Encryption** | Zero-knowledge secrets — we never see your values |
| **Scoped Secrets** | Separate development, staging, and production |
| **Local CI Runner** | Run GitHub Actions workflows locally with protection |
| **Team Sync** | Share encrypted secrets across your team via cloud |

---

## 🔐 Protection Modes

```bash
# Detect mode — log exposures without modification
dotset run --mode detect -- npm test

# Redact mode (recommended) — replace secrets with [REDACTED]
dotset run --mode redact -- npm start

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

| Plan | Projects | Secrets | Audit Logs |
|:-----|:---------|:--------|:-----------|
| **Free** | 5 | 100/project | 7 days |
| **Pro** | 25 | Unlimited | 90 days |
| **Business** | Unlimited | Unlimited | 365 days |

---

## 🔗 Links

- 🌐 [dotsetlabs.com](https://dotsetlabs.com)
- 📖 [docs.dotsetlabs.com](https://docs.dotsetlabs.com)
- 🖥️ [app.dotsetlabs.com](https://app.dotsetlabs.com)
- 💻 [Demo](https://github.com/dotsetlabs/demos)

<div align="center">

**Built with ❤️ for developers who care about security.**

</div>
