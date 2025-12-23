<div align="center">

# dotset labs

**Developer security tools that just work.**

[![Website](https://img.shields.io/badge/website-dotsetlabs.com-blue?style=flat-square)](https://dotsetlabs.com)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](https://opensource.org/licenses/MIT)

</div>

---

We build open-source CLI tools and cloud services that help developers manage secrets, monitor runtime security, and share local development environments securely. Our tools are designed to integrate seamlessly into existing workflows with zero configuration overhead.

## 🚀 Our Products

### 🔐 Axion — Encrypted Secrets Management

**Never commit `.env` files again.** Axion provides zero-knowledge encryption for environment variables with seamless team sync.

| Feature | Description |
|:--------|:------------|
| **Zero-knowledge encryption** | Secrets encrypted locally before sync — we never see your data |
| **Scoped environments** | Separate secrets for development, staging, production |
| **Team collaboration** | Securely share secrets with fine-grained access control |
| **CI/CD integration** | Service tokens for automated pipelines |
| **Audit logging** | Track who accessed what and when |

```bash
npm install -g @dotsetlabs/axion

axn init                          # Initialize project
axn set API_KEY "sk_live_..."     # Store encrypted secret
axn run -- npm start              # Inject secrets at runtime
```

📦 **[GitHub](https://github.com/dotsetlabs/axion)** · 📖 **[Docs](https://dotsetlabs.com/axion)**

---

### 🔬 Gluon — Runtime Security Telemetry

**Know what your code is actually doing.** Gluon monitors secret access, network connections, and module loading in real-time — without changing your code.

| Feature | Description |
|:--------|:------------|
| **Secret exposure detection** | Alerts when secrets are logged, sent over network, or leaked |
| **Network monitoring** | Track all outbound connections your app makes |
| **Module tracking** | See every dependency loaded at runtime |
| **Runtime SBOM** | Generate accurate Software Bill of Materials from actual behavior |
| **Axion integration** | Enhanced tracking for Axion-managed secrets |

```bash
npm install -g @dotsetlabs/gluon

gln init                          # Initialize monitoring
gln run -- npm start              # Run with security telemetry
gln status                        # View telemetry summary
```

📦 **[GitHub](https://github.com/dotsetlabs/gluon)** · 📖 **[Docs](https://dotsetlabs.com/gluon)**

---

### ⚡ Tachyon — Zero-Trust Dev Tunnels

**Localhost sharing without the security headaches.** Tachyon provides instant tunnels with SSO authentication and closed-by-default access control.

| Feature | Description |
|:--------|:------------|
| **Zero-trust by default** | Tunnels are private — you explicitly allow access |
| **SSO authentication** | Google, GitHub, or email verification for viewers |
| **Webhook capture** | Inspect and replay incoming webhook requests |
| **Stable URLs** | Consistent subdomains across sessions |
| **Axion integration** | Tunnels automatically have access to your Axion secrets |

```bash
npm install -g @dotsetlabs/tachyon

tcn share 3000                    # Share localhost:3000
tcn share 3000 --public           # Public tunnel (no auth)
tcn status                        # View active tunnels
```

📦 **[GitHub](https://github.com/dotsetlabs/tachyon)** · 📖 **[Docs](https://dotsetlabs.com/tachyon)**

---

## 📦 Unified CLI

Install all three tools with a single package:

```bash
npm install -g @dotsetlabs/cli

# Now you have: axn, gln, tcn
```

📦 **[GitHub](https://github.com/dotsetlabs/cli)**

---

## 💰 Pricing

All products offer a **free tier** suitable for personal projects and small teams.

| Plan | Axion | Gluon | Tachyon |
|:-----|:------|:------|:--------|
| **Free** | 2 projects, 2 users | Local telemetry | 2 tunnels, 8hr sessions |
| **Pro** | Unlimited projects, 10 users | 30-day cloud history | 10 tunnels, 48hr sessions |
| **Business** | 50 users, webhooks, audit logs | Team dashboards, alerts | 20 tunnels, SSO, 7-day sessions |

---

## 🔗 Links

- 🌐 **Website:** [dotsetlabs.com](https://dotsetlabs.com)
- 📖 **Documentation:** [docs.dotsetlabs.com](https://docs.dotsetlabs.com)
- 🐙 **GitHub:** [github.com/dotsetlabs](https://github.com/dotsetlabs)

---

<div align="center">

**Built with ❤️ for developers who care about security.**

</div>
