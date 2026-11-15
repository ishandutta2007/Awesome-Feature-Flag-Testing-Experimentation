# Awesome-Feature-Flag-Testing-Experimentation

# Top Feature Flag Testing & Experimentation Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Progressive Delivery, A/B Testing & Self-Hosted Flag Management*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Feature Flag Testing & Experimentation**. These tools help teams decouple deployment from release—enabling gradual rollouts, kill switches, and data-driven experiments without redeploying code. The category spans **flag-first platforms** built for operational control (LaunchDarkly, Unleash, Flagsmith) and **experimentation-first platforms** where flags are the delivery mechanism for statistical analysis (Statsig, GrowthBook, Optimizely) [citation:6].

**Examples** include LaunchDarkly, Statsig, Unleash, Flagsmith, GrowthBook, Split (Harness), Optimizely, PostHog, and Flipt (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted flag management, open-source experimentation engines, and community-driven progressive delivery—ideal for teams seeking data sovereignty and avoiding per-seat or per-MTU SaaS pricing. The open-source landscape is genuinely mature: **Unleash** is battle-tested at scale (used by Visa) with the largest SDK ecosystem and a real free self-hosted edition , **Flagsmith** offers deployment flexibility including air-gapped on-prem with vendor-maintained OpenFeature providers [citation:6], and **GrowthBook** brings warehouse-native statistical rigor to open-source experimentation [citation:6].

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[LaunchDarkly](https://launchdarkly.com/)** | **The enterprise feature management standard.** Most mature platform with SDKs for every major language, sophisticated targeting, and scale to billions of evaluations. **Experimentation features require higher plans**—it is flag-first, not experiment-first [citation:10][citation:14]. | Foundation: **~$10/seat/month**; Enterprise: custom [citation:10] | **No free tier**; 14-day free trial only [citation:10] |
| **[Statsig](https://statsig.com/)** | **Experimentation-first platform founded by ex-Facebook infrastructure engineers.** Every flag evaluation is an experiment opportunity with automatic metric impact detection and guardrail alerts. Bundles flags, A/B testing, analytics, and session replay in one API [citation:10][citation:14]. | Usage-based (free up to **1M events/month**); Pro: usage-based [citation:10] | **Free**: up to 1M events/month [citation:10] |
| **[Optimizely Feature Experimentation](https://www.optimizely.com/)** | **Enterprise-grade full-stack experimentation** (formerly Optimizely Full Stack). Deepest statistical engine alongside Statsig, with mature governance for regulated buyers. Distinct from Optimizely Web (client-side A/B testing) [citation:14]. | Custom pricing only (enterprise-only) [citation:10] | **No free tier** [citation:10] |
| **[Split (Harness)](https://www.split.io/)** | **Data-driven feature delivery with automatic metric attribution.** Correlates flag changes with metric movements automatically. Acquired by Harness in 2024—**standalone customers report slower velocity** and pricing is now tied to Harness platform deals [citation:10][citation:14]. | Free tier available; Team/Enterprise: custom [citation:10] | **Free tier** with generous limits [citation:10] |
| **[PostHog](https://posthog.com/)** | **Flags + product analytics + session replay in one platform.** Strong for product-driven teams wanting consolidated tooling at transparent pricing. Not pure flag infrastructure—analytics-heavy [citation:10]. | Free tier available; usage-based beyond [citation:10] | **Free**: usage-based tier with generous limits [citation:10] |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Unleash](https://github.com/Unleash/unleash)** | [![Stars](https://img.shields.io/github/stars/Unleash/unleash?style=social&color=white)](https://github.com/Unleash/unleash/stargazers) | **The leading open-source flag platform with the largest SDK ecosystem.** Apache-2.0 core (open-core). **Used in production by Visa**—data sovereignty and compliance aren't optional for those buyers . **Progressive rollouts, kill switches, custom activation strategies, and segments** for targeting. **Official server SDKs** (Node, Java, Go, Python, .NET, Ruby, PHP, Rust) and **client SDKs** (JS, React, Vue, Svelte, Next.js, React Native, Android, iOS, Flutter). **Unleash Edge** for low-latency, resilient evaluation at scale. **Trade-offs**: **open-source edition limited to 2 environments and 1 project**; advanced RBAC, SSO, SCIM, and 2-year audit logs require paid plans. **No native OpenFeature providers**—community-maintained only [citation:6]. **Best for regulated industries needing self-hosted flags with enterprise-grade security** [citation:9]. |
| **[Flagsmith](https://github.com/Flagsmith/flagsmith)** | [![Stars](https://img.shields.io/github/stars/Flagsmith/flagsmith?style=social&color=white)](https://github.com/Flagsmith/flagsmith/stargazers) | **The most deployment-flexible open-source flag platform—SaaS, private cloud, or fully air-gapped on-prem.** BSD-3 core (open-core). **Independently owned**—not consolidated into a larger platform bet . **Flags + remote configuration** in one dashboard, reducing tool sprawl. **Boolean and multivariate flags, segments, percentage rollouts, scheduled flags**. **Vendor-maintained OpenFeature providers**—a differentiator vs. Unleash [citation:6]. **Edge API replicated across 8 AWS regions** for low-latency delivery [citation:9]. **Trade-offs**: **A/B testing leans on integrations rather than a built-in stats engine**; self-hosting requires PostgreSQL. **SAML, RBAC, change requests, and audit logs on Scale-Up**; unlimited audit history and Okta/ADFS/LDAP on Enterprise [citation:9]. **Best for security-conscious teams needing deployment flexibility** with official OpenFeature support [citation:6]. |
| **[GrowthBook](https://github.com/growthbook/growthbook)** | [![Stars](https://img.shields.io/github/stars/growthbook/growthbook?style=social&color=white)](https://github.com/growthbook/growthbook/stargazers) | **The open-source experimentation platform with warehouse-native statistics.** MIT core with commercially-licensed directories (open-core). **Your data warehouse is the source of truth**—nothing leaves it for analysis . **Bayesian and frequentist engines, CUPED, sequential testing, and multi-armed bandits** on Pro . **Flags are the delivery mechanism**—the real value is rigorous statistical analysis tied to your warehouse metrics. **Official OpenFeature providers** (Go, Java, Python, .NET, Web/React) [citation:6]. **Trade-offs**: **Flag management is one part of a larger experimentation product**; self-hosting requires MongoDB; governance features sit in commercial tiers [citation:6]. **Best for data teams and engineers wanting experimentation built into release workflows** with full control over data [citation:6]. |
| **[Flipt](https://github.com/flipt-io/flipt)** | [![Stars](https://img.shields.io/github/stars/flipt-io/flipt?style=social&color=white)](https://github.com/flipt-io/flipt/stargazers) | **Open-source flag service with Git-backed storage option.** GPL-3.0. **Supports segments, multiple variations, and percentage thresholds** for rollouts. **Store flags in Git—no database required** for simpler deployments . **Open-source edition is free**; Pro ($200/month) adds Git provider integrations, PRs from UI, and secrets management . **Best for teams wanting GitOps-native flag management** without database infrastructure. |
| **[FeatBit](https://github.com/featbit/featbit)** | [![Stars](https://img.shields.io/github/stars/featbit/featbit?style=social&color=white)](https://github.com/featbit/featbit/stargazers) | **Self-hosted flag and A/B testing tool built for scale.** **Foundation tier free with no limits on seats, MAUs, or projects**—includes flags, targeting, audit logs, and experimentation . **Enterprise ($3,999/year)** adds SSO, Terraform/GitOps, flag change approvals, and shareable segments . **Handles 1M+ simultaneous online users**; Helm/Terraform/OpenTelemetry support . **Best for teams wanting a feature-rich self-hosted tool with a generous free tier** . |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Flipper](https://github.com/flippercloud/flipper)** | [![Stars](https://img.shields.io/github/stars/flippercloud/flipper?style=social&color=white)](https://github.com/flippercloud/flipper/stargazers) | **The best flag tool for Ruby on Rails teams.** Rebuilt from GitHub's internal flag platform by ex-GitHub engineers. **Ruby-only** (other languages planned). **Open-source gem free with unlimited flags**; Flipper Cloud free tier (2 seats, 5 flags) with fixed-price tiers ($49–$299/month) . **Best for Rails teams** wanting exceptional developer experience. |
| **[GO Feature Flag (GOFF)](https://github.com/thomaspoignant/go-feature-flag)** | [![Stars](https://img.shields.io/github/stars/thomaspoignant/go-feature-flag?style=social&color=white)](https://github.com/thomaspoignant/go-feature-flag/stargazers) | **Lightweight, open-source flag evaluation for Go and beyond.** Configuration-file-based with **experimentation rollout dates** (start/end) built in [citation:8]. **No external dependencies**—flags live in YAML/JSON/TOML. Pairs A/B rollouts with data exporters for analysis in your own stack [citation:6]. **Best for teams wanting simple, dependency-free flag evaluation** without a management UI. |

**Frameworks for building custom systems**: Choose **Unleash** for battle-tested self-hosted flags with the largest SDK ecosystem , **Flagsmith** for deployment flexibility and vendor-maintained OpenFeature support , or **GrowthBook** for warehouse-native experimentation rigor —all without per-seat or per-MTU SaaS fees that compound at scale. For GitOps-native simplicity, **Flipt** stores flags in Git without a database .

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Feature flag platforms control production code paths; **flag evaluation errors can either expose unfinished features or hide working ones**. Enforce server-side evaluation for security-sensitive paths, default to disabled (fail closed), and wrap flag checks once at the request boundary rather than scattering them through business logic [citation:1][citation:5].
- **Open-source flag tooling has different trade-offs and licensing nuances.** **Unleash's open-source edition limits you to 2 environments and 1 project**—advanced RBAC, SSO, and audit logs require paid plans [citation:9]. **Flagsmith's A/B testing is integration-based**, not a built-in stats engine . **GrowthBook is experimentation-first**—flag management is one part of a larger product, and self-hosting requires MongoDB [citation:6]. **Unleash has no native OpenFeature providers** (community-maintained only); **Flagsmith and GrowthBook maintain official providers** [citation:6]. **Commercial pricing varies**: LaunchDarkly starts at ~$10/seat/month with **no free tier** , Statsig offers a **free tier to 1M events/month** , and Optimizely is **enterprise-only with no free tier** [citation:10]. **Validate whether you need flag-first operational control (Unleash, Flagsmith) or experimentation-first statistical rigor (GrowthBook, Statsig)** before committing.

---

**Made for platform engineers, product teams, and developers building progressive delivery infrastructure.**  
Let's make feature flag testing and experimentation more open, governed, and data-driven.
