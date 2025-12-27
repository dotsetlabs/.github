<div align="center">

# dotset labs

**Simple, powerful security and workflow tools for modern developer teams.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.dotsetlabs.com-6366f1?style=flat-square)](https://docs.dotsetlabs.com)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

We build open-source tools and cloud services that help developers manage secrets, monitor runtime security, run local CI pipelines, and share development environments securely. Our ecosystem is designed for speed, security, and seamless integration.

## 🚀 Our Products

### 🔐 [Axion](https://github.com/dotsetlabs/axion) — Encrypted Secrets & SDK

**Never commit `.env` files again.** Axion provides zero-knowledge encryption for environment variables with seamless team sync and a native SDK.

| Feature | Description |
|:--------|:------------|
| **Zero-knowledge** | AES-256-GCM encryption locally — we never see your plain-text data |
| **Native SDK** | Type-safe secret loading for Node.js with built-in caching |
| **Tamper-Proof Audit** | SHA-256 hash chain audit logs covering all access (Pro/Business) |
| **RBAC & Scopes** | Role-based access with environment isolation |

```bash
npm install -g @dotsetlabs/cli
dotset secrets set DB_PASSWORD "secret123"   # Store encrypted secret
dotset run -- npm start                     # Inject secrets at runtime
```

---

### 🔬 [Gluon](https://github.com/dotsetlabs/gluon) — Runtime Protection & Security

**Stop leaks before they happen.** Gluon provides active protection for your secrets and deep telemetry for your application's behavior.

| Feature | Description |
|:--------|:------------|
| **Detection Modes** | **Detect**, **Redact**, or **Block** secret leaks in real-time |
| **Network Guard** | Monitor and restrict outbound connections |
| **Unified Audit** | Integrated security event tracking across the platform |
| **Security Dashboard** | Visual risk scores and leak timelines in the Cloud |

```bash
dotset run --mode block -- npm start  # Fail process on secret leak
dotset scan                           # Static analysis
```

---

### 🚀 [Hadron](https://github.com/dotsetlabs/hadron) — Local-First CI

**Fast, local CI with zero config.** Hadron runs your workflows locally first, providing identical environments from dev to prod.

| Feature | Description |
|:--------|:------------|
| **Local-First** | Run pipelines on your machine with instant feedback |
| **Axion Sync** | Push local CI results to the cloud with `--sync` |
| **Security Aware** | Built-in leak detection and dependency monitoring |
| **CI Dashboard** | Rich run history and log viewer in the Cloud |

```bash
dotset ci --list                      # List available CI workflows
dotset ci build test --sync           # Run and sync results to cloud
```

---



| Feature | Description |
|:--------|:------------|
| **Auth by Default** | Tunnels are private by default — no extra config needed |
| **Request Inspector** | View and replay captured requests (REST/WebSocket) |
| **SSO Protection** | Unified authentication with GitHub or Google |

```bash
dotset share 3000 --inspect          # Share and launch Request Inspector
```

---

## 📦 Unified CLI

The `dotset` CLI combines the entire ecosystem into a single tool.

```bash
npm install -g @dotsetlabs/cli

# Run Axion (secrets) + Gluon (protection) + Hadron (CI)
dotset run --scope prod --mode redact -- npm start
```

---

## 💰 Pricing

|:-----|:------|:------|:-------|:--------|
| **Free** | 2 projects | Local only | 1 project | 2 tunnels |
| **Pro** | Unlimited Cloud | 30-day History | 5 projects | 10 tunnels |
| **Business** | Audit Logs | Full SBOM | Unlimited | Dedicated IPs |

---

## 🔗 Links

- 🌐 [dotsetlabs.com](https://dotsetlabs.com)
- 📖 [docs.dotsetlabs.com](https://docs.dotsetlabs.com)
- 🖥️ [app.dotsetlabs.com](https://app.dotsetlabs.com)

<div align="center">

**Built with ❤️ for developers who care about security and speed.**

</div>
