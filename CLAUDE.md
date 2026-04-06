# KubeOrch — Organization Context

## What is KubeOrch?

KubeOrch is a visual Kubernetes orchestration platform that eliminates YAML through drag-and-drop workflows. Users design cluster topologies on an infinite canvas, and KubeOrch generates all Kubernetes manifests automatically.

## Organization

- **GitHub**: https://github.com/KubeOrch
- **Website**: https://kubeorch.dev
- **Docs**: https://docs.kubeorch.dev
- **Contact**: hi@kubeorch.dev
- **License**: Apache 2.0

---

## Repositories

### `core` — Orchestration Engine
- **Language**: Go 1.25
- **What**: Main backend — orchestration engine, API gateway, service topology manager
- **Deployment**: Docker (multi-stage Dockerfile, golang:1.22-alpine builder)
- **Docs**: https://docs.kubeorch.dev/reference/rest-api/

### `ui` — Web Interface
- **Language**: TypeScript (Next.js, React)
- **What**: Visual drag-and-drop workflow builder, component palette, canvas editor
- **Deployment**: Docker (node:20-alpine, multi-stage)
- **Key packages**: Next.js, React, shadcn/ui, Tailwind CSS

### `cli` — orchcli
- **Language**: Go 1.22
- **What**: CLI for initializing, deploying, and managing Kubernetes clusters from the terminal
- **Commands**: `orchcli init`, `orchcli start`, `orchcli stop`, `orchcli logs`
- **Docs**: https://docs.kubeorch.dev/architecture/cli/commands/

### `docs` — Documentation Site
- **Language**: TypeScript (Astro + Starlight)
- **What**: Guides, API reference, CLI reference, architecture docs
- **Deployment**: GitHub Pages (via GitHub Actions — `deploy.yml`)
- **URL**: https://docs.kubeorch.dev
- **Custom domain**: Configured via GitHub Pages settings

### `landing` — Marketing Site
- **Language**: TypeScript (Next.js 16, React 19)
- **What**: Landing page — hero, features, pricing, testimonials, FAQ, newsletter
- **Deployment**: Cloudflare Pages (auto-deploys from `main` branch)
- **URL**: https://kubeorch.dev
- **Key packages**: Tailwind CSS v4 (OKLCH colors), shadcn/ui, motion (Framer Motion), ogl, resend

### `community` — Governance & RFCs
- **What**: RFCs, architecture decisions, governance docs, roadmap, release process
- **No deployment** — reference only

### `.github` — Org Defaults
- **What**: Default community health files (CODE_OF_CONDUCT, CONTRIBUTING, SECURITY, etc.)

---

## Infrastructure & Services

### Domain: kubeorch.dev
- **Registrar/DNS**: Cloudflare
- **Email routing**: Cloudflare Email Routing (catch-all → personal email)
- **Contact email**: hi@kubeorch.dev (forwarded via Cloudflare)

### Hosting
| Service | Host | Deploy method |
|---------|------|---------------|
| Landing page (kubeorch.dev) | Cloudflare Pages | Auto-deploy from `main` on push |
| Docs (docs.kubeorch.dev) | GitHub Pages | GitHub Actions (`deploy.yml`) |
| Core API | Docker | Manual / CI |
| UI | Docker | Manual / CI |

### Email (Resend)
- **Service**: Resend (resend.com)
- **Usage**: Newsletter subscribe (welcome email) + broadcast templates
- **Audience**: Managed via Resend Audiences
- **Env vars needed on Cloudflare Pages**: `RESEND_API_KEY`, `RESEND_AUDIENCE_ID`
- **Sending domain**: kubeorch.dev (DNS records configured in Cloudflare)

### SEO
- **Sitemap**: Auto-generated at `/sitemap.xml` via Next.js
- **robots.txt**: Static file in `public/`
- **Structured data**: JSON-LD (Organization, SoftwareApplication, FAQPage)
- **OG image**: Static `public/og-image.png` (1200x630)
- **Google Search Console**: Needs setup — verify via Cloudflare DNS TXT record
- **Bing Webmaster Tools**: Not yet set up

---

## Tech Stack Summary

| Layer | Technology |
|-------|-----------|
| Backend | Go |
| Frontend (app) | Next.js, React, TypeScript, Tailwind CSS, shadcn/ui |
| Frontend (docs) | Astro + Starlight |
| Frontend (landing) | Next.js 16, React 19, Tailwind v4, shadcn/ui, Framer Motion |
| CLI | Go |
| Database | PostgreSQL (core) |
| Containerization | Docker |
| DNS/CDN | Cloudflare |
| Email | Resend + Cloudflare Email Routing |
| CI/CD | GitHub Actions |

---

## Design System (Landing Page)

- **Color system**: OKLCH (Tailwind v4)
- **Primary accent**: Green (`oklch(0.723 0.219 149.579)` / `#34d399`)
- **Dark mode**: Default and only theme
- **Heading font**: Bricolage Grotesque (via next/font/google, `--font-heading`)
- **Body font**: Inter
- **Mono font**: Geist Mono
- **Component library**: shadcn/ui (radix-luma style, stone base, green accent)
- **Animations**: tw-animate-css, Framer Motion, Magic UI Particles, React Bits (LightRays, BorderGlow, GradientText)

---

## Conventions

### Git Commits
All commits follow conventional commit format:
```
type(scope): short description
```
Types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `chore`

**Do NOT** add Claude attribution, co-author lines, or "Generated with Claude" messages.
**Do NOT** push unless explicitly asked.

### Pricing Tiers
- **Community**: Free, self-hosted, open source (Apache 2.0)
- **Pro**: $49/month, managed cloud hosting
- **Enterprise**: Custom pricing, AI optimization, on-prem, SLAs
