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
| **Secret Templating** | Dynamic values and complex JSON support |
| **Audit logging** | Track who accessed what and when (Business) |

```bash
npm install -g @dotsetlabs/axion
axn set DB_PASSWORD "secret123"   # Store encrypted secret
axn run -- npm start              # Inject secrets at runtime
```

---

### 🔬 [Gluon](https://github.com/dotsetlabs/gluon) — Runtime Protection & Security

**Stop leaks before they happen.** Gluon provides active protection for your secrets and deep telemetry for your application's behavior.

| Feature | Description |
|:--------|:------------|
| **Detection Modes** | **Detect**, **Redact**, or **Block** secret leaks in real-time |
| **Network Guard** | Monitor and restrict outbound connections |
| **Runtime SBOM** | Generate CycloneDX/SPDX materials from actual behavior |
| **Security Dashboard** | Visual risk scores and leak timelines in the Cloud |

```bash
npm install -g @dotsetlabs/gluon
gln run --mode block -- npm start  # Fail process on secret leak
gln sbom --static                 # Generate security bill of materials
```

---

### 🚀 [Hadron](https://github.com/dotsetlabs/hadron) — Local-First CI

**Fast, local CI with zero config.** Hadron runs your workflows locally first, providing identical environments from dev to prod.

| Feature | Description |
|:--------|:------------|
| **Local-First** | Run pipelines on your machine with instant feedback |
| **Zero-Config** | Auto-detects test suites and build steps |
| **Parallel Execution** | Dramatically speed up local builds and tests |
| **CI Dashboard** | Rich run history and log viewer in the Cloud |

```bash
npm install -g @dotsetlabs/hadron
hdn run                           # Run local CI workflow
hdn check                         # Validate workflow configurations
```

---

### ⚡ [Tachyon](https://github.com/dotsetlabs/tachyon) — Zero-Trust Dev Tunnels

**Localhost sharing with a built-in Inspector.** Tachyon provides instant tunnels with SSO and a powerful request inspector.

| Feature | Description |
|:--------|:------------|
| **Request Inspector** | View and replay captured requests (REST/WebSocket) |
| **Zero-trust** | Tunnels are private by default — authenticated via SSO |
| **Stable URLs** | Reserved subdomains that persist across sessions |

```bash
npm install -g @dotsetlabs/tachyon
tcn share 3000 --inspect          # Share and launch Request Inspector
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

| Plan | Axion | Gluon | Hadron | Tachyon |
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
