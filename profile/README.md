<div align="center">

# dotset labs

**Simple, powerful security tools for modern developer teams.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![Documentation](https://img.shields.io/badge/docs-docs.dotsetlabs.com-6366f1?style=flat-square)](https://docs.dotsetlabs.com)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

We build open-source CLI tools and cloud services that help developers manage secrets, monitor runtime security, and share local development environments securely. Our tools are designed to integrate seamlessly into existing workflows with zero configuration overhead.

## 🚀 Our Products

### 🔐 Axion — Encrypted Secrets & SDK

**Never commit `.env` files again.** Axion provides zero-knowledge encryption for environment variables with seamless team sync and a native SDK for type-safe secret access.

| Feature | Description |
|:--------|:------------|
| **Zero-knowledge encryption** | AES-256-GCM encryption locally before sync — we never see your data |
| **Native SDK** | Type-safe secret loading for Node.js with built-in caching |
| **Secret Templating** | Use `{{KEY}}` syntax for dynamic values and complex JSON configs |
| **Scoped environments** | Separate secrets for development, staging, production |
| **Audit logging** | Track who accessed what and when (Pro/Business) |

```bash
npm install -g @dotsetlabs/axion

axn set DB_PASSWORD "secret123"   # Store encrypted secret
axn set CONFIG --json '{"port": 80}' # Store complex JSON
axn run -- npm start              # Inject secrets at runtime
```

📦 **[GitHub](https://github.com/dotsetlabs/axion)** · 📖 **[Quickstart](https://docs.dotsetlabs.com/axion/quickstart)** · 📖 **[SDK Reference](https://docs.dotsetlabs.com/axion/sdk)**

---

### 🔬 Gluon — Runtime Protection & Telemetry

**Stop leaks before they happen.** Gluon provides active protection for your secrets and generates deep telemetry for your application's runtime behavior.

| Feature | Description |
|:--------|:------------|
| **Protection Modes** | Choose to **Detect**, **Redact**, or **Block** secret leaks in real-time |
| **Secret Exposure Detection** | Real-time monitoring of stdout/stderr and network calls |
| **Network Monitoring** | Track all outbound connections your app makes |
| **Runtime SBOM** | Generate CycloneDX/SPDX materials from actual runtime behavior |
| **Axion integration** | Automatic protection for Axion-managed secrets |

```bash
npm install -g @dotsetlabs/gluon

gln run -- npm start              # Run with active leak protection
gln run --mode block -- npm start  # Fail process on secret leak
gln sbom --static                 # Generate security bill of materials
```

📦 **[GitHub](https://github.com/dotsetlabs/gluon)** · 📖 **[Quickstart](https://docs.dotsetlabs.com/gluon/quickstart)** · 📖 **[Monitoring Guide](https://docs.dotsetlabs.com/gluon/runtime-monitoring)**

---

### ⚡ Tachyon — Zero-Trust Dev Tunnels

**Localhost sharing with a built-in Inspector.** Tachyon provides instant tunnels with SSO authentication and a powerful web-interface for inspecting traffic.

| Feature | Description |
|:--------|:------------|
| **Request Inspector** | Embedded web UI to view and replay captured requests (REST/WebSocket) |
| **Zero-trust by default** | Tunnels are private — authenticated via Google, GitHub, or Email |
| **Unified Auth** | Shares identity with Axion and Gluon for seamless workflow |
| **Stable URLs** | Reserved subdomains that persist across sessions (Pro/Business) |
| **Webhook capture** | Inspect and debug internal/external webhooks locally |

```bash
npm install -g @dotsetlabs/tachyon

tcn share 3000 --inspect          # Share and launch Request Inspector
tcn projects create my-app        # Organize tunnels by project
tcn status                        # View active connections
```

📦 **[GitHub](https://github.com/dotsetlabs/tachyon)** · 📖 **[Quickstart](https://docs.dotsetlabs.com/tachyon/quickstart)** · 📖 **[Inspector Guide](https://docs.dotsetlabs.com/tachyon/inspector)**

---

## 📦 Unified CLI

The `dotset` CLI brings the entire ecosystem together. Use `dotset run` to combine secrets injection with runtime monitoring in a single command.

```bash
npm install -g @dotsetlabs/cli

# Axion (secrets) + Gluon (protection) in one go
dotset run --scope prod --mode redact -- npm start
```

📦 **[GitHub](https://github.com/dotsetlabs/cli)** · 📖 **[Unified CLI Reference](https://docs.dotsetlabs.com/cli/unified-cli)**

---

## 💰 Pricing

All products offer a **free tier** suitable for personal projects and small teams. Use them separately or together.

| Plan | Axion | Gluon | Tachyon |
|:-----|:------|:------|:--------|
| **Free** | 2 projects, local only | Local telemetry | 2 tunnels, 8hr sessions |
| **Pro** | Unlimited projects, Cloud Sync | 30-day history, alerting | 10 tunnels, Stable URLs |
| **Business** | Webhooks, RBAC, Audit Logs | Team dashboards, SBOM auto-sync | SSO, 7-day sessions, Dedicated IPs |

---

## 🔗 Links

- 🌐 **Website:** [dotsetlabs.com](https://dotsetlabs.com)
- 📖 **Documentation:** [docs.dotsetlabs.com](https://docs.dotsetlabs.com)
- 🐙 **GitHub:** [github.com/dotsetlabs](https://github.com/dotsetlabs)
- 🖥️ **Dashboard:** [app.dotsetlabs.com](https://app.dotsetlabs.com)

---

<div align="center">

**Built with ❤️ for developers who care about security.**

</div>
