<div align="center">

# Dotset Labs

**Open-source developer tools for secure CI/CD.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.dotsetlabs.com-10b981?style=flat-square)](https://docs.dotsetlabs.com)
[![npm](https://img.shields.io/badge/npm-@dotsetlabs/cli-red?style=flat-square)](https://www.npmjs.com/package/@dotsetlabs/cli)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

## 🛡️ Dotset Shield

**Free, open-source secret protection for CI/CD build logs.**

Shield intercepts output streams and redacts secrets in real-time — before they're ever exposed in your logs.

```bash
npm install -g @dotsetlabs/cli

# Run with protection (zero config)
dotset shield run -- npm start
# 🛡️  shield | mode: redact | secrets: 5 | providers: dotenv
```

---

## ✨ Key Features

| Feature | Description |
|:--------|:------------|
| **Zero Config** | Works with your existing `.env` files immediately |
| **Streaming Protection** | Line-buffered redaction catches secrets split across chunks |
| **Three Modes** | **Detect** (audit), **Redact** (replace), or **Block** (suppress) |
| **22+ Patterns** | AWS, GitHub, Stripe, OpenAI, and more built-in |
| **Compliance Reports** | Generate HTML/SARIF reports for audit trails |

---

## 🚀 GitHub Action

Use our official action to protect your workflows:

```yaml
steps:
  - uses: dotsetlabs/cli@v1
  - run: npm test
```

That's it. All output from subsequent steps is protected.

---

## 🔒 Trust & Security

**Your secrets never leave your machine.** Shield is 100% local — no cloud, no telemetry, no account required.

- 📖 [View the source code](https://github.com/dotsetlabs/cli)
- 🔨 [Build from source](https://github.com/dotsetlabs/cli) if you prefer

---

## 🔗 Links

- 🌐 [dotsetlabs.com](https://dotsetlabs.com) — Website
- 📖 [docs.dotsetlabs.com](https://docs.dotsetlabs.com) — Documentation
- 💻 [GitHub](https://github.com/dotsetlabs/cli) — Source code

<div align="center">

**Built with ❤️ for developers who care about security.**

© 2025 Dotset Labs

</div>
