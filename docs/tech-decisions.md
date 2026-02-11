# Tech Stack Decisions

> **Status**: Decided
> **Last Updated**: 2026-02-10

---

## Final Stack

| Layer | Choice | Rationale |
|---|---|---|
| **Framework** | Astro + TypeScript | Purpose-built for content/marketing sites. Zero JS shipped by default. Cloudflare-backed (acquired Jan 2026). Used by Visa, Microsoft, Adobe, NBC News. |
| **Styling** | Tailwind CSS | Utility-first — no pre-baked look. Design tokens map directly to `tailwind.config.ts`. Industry standard for modern marketing sites. |
| **Static Components** | Custom Astro components | `.astro` files for all static content (hero, cards, sections, footer). Simple, fast, no runtime overhead. |
| **Interactive Components** | Headless UI or Radix Primitives | Unstyled, accessible building blocks for dropdowns, tabs, mobile menu, dialogs. Skinned with Tailwind. No visual opinions to fight. |
| **Hosting** | GitHub Pages | Free. Custom domain support (`soft-tab.com` — not a redirect, real custom domain). Auto-HTTPS via Let's Encrypt. |
| **CI/CD** | GitHub Actions | Build Astro → deploy static output to GitHub Pages. Free for public repos. |
| **Forms** | Formspree (free tier) | 50 submissions/month. Spam filtering. No backend needed. Static-site compatible. |
| **Analytics** | Google Analytics 4 | Free. Basic traffic and conversion tracking. Set up once, check when curious. |
| **Scheduling** | Calendly (free tier) | Embedded or linked for direct call booking. Removes email back-and-forth. |

---

## Alternatives Considered

### Framework

| Option | Verdict | Why Not |
|---|---|---|
| **Next.js (static export)** | Rejected | Overkill. Ships React runtime to client for what's mostly static HTML. More complexity than needed. |
| **Hugo** | Rejected | Go templating is limiting. No TypeScript. Poor component model. |
| **11ty (Eleventy)** | Rejected | Smaller ecosystem. Less ergonomic than Astro for component-based development. |
| **SvelteKit** | Rejected | Good framework, but less marketing-site focused. Astro is purpose-built for this. |

### Styling

| Option | Verdict | Why Not |
|---|---|---|
| **MUI** | Rejected | Dated look. Heavy. Fights against custom brand design. React-only. |
| **shadcn/ui** | Rejected (for now) | Copy-paste components are nice but create a recognizable "shadcn look." Brand-first site needs to be unique. React-only. |
| **DaisyUI** | Rejected | Tailwind plugin with component classes. Better than MUI but still opinionated on visual design. |
| **Plain CSS / CSS Modules** | Rejected | Slower to build. No responsive utilities. Harder to maintain consistency. |

### Interactive Component Primitives

| Option | Best For | Notes |
|---|---|---|
| **Headless UI** (Tailwind Labs) | Astro + React islands | Built by the Tailwind team. React + Vue support. Dropdowns, dialogs, tabs, popovers. |
| **Radix Primitives** | React islands | More comprehensive primitive set. Excellent accessibility. |
| **Both are viable** | TBD | Final choice during development based on which components we actually need. |

---

## GitHub Pages Custom Domain Setup

When we reach Phase 5 (Infrastructure & Launch Prep):

1. **DNS**: Add CNAME record at domain registrar
   - `www.soft-tab.com` → `<username>.github.io`
   - Or A records pointing to GitHub's IPs for apex domain
2. **Repo**: Add `CNAME` file to repo root containing `soft-tab.com`
3. **GitHub Settings**: Enable custom domain in repo settings, enforce HTTPS
4. **Result**: `www.soft-tab.com` serves the site directly. `<username>.github.io` redirects TO the custom domain.

**Visitor experience**: Address bar always shows `soft-tab.com/...` for every route. GitHub is invisible.

---

## GitHub Actions CI/CD Pipeline

```yaml
# .github/workflows/deploy.yml (rough outline)
on:
  push:
    branches: [main]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: actions/setup-node@v4
      - run: npm install
      - run: npm run build
      - uses: actions/deploy-pages@v4
```

Astro has an official GitHub Pages deployment guide with a pre-built Action.

---

## Project Structure (Anticipated)

```
soft-tab.com/
├── src/
│   ├── components/       # Reusable Astro + React components
│   │   ├── ui/           # Atoms: Button, Link, Icon, Input
│   │   ├── layout/       # Header, Footer, Section, Container
│   │   └── blocks/       # Hero, FeatureCards, Testimonial, CTA
│   ├── layouts/          # Page layouts (BaseLayout, PersonaLayout)
│   ├── pages/            # File-based routing
│   │   ├── index.astro           # Homepage
│   │   ├── services.astro        # Services
│   │   ├── about.astro           # About
│   │   ├── contact.astro         # Contact
│   │   ├── for-founders.astro    # Persona: Founders
│   │   ├── for-engineering-leaders.astro  # Persona: CTOs
│   │   └── for-ai-adoption.astro # Persona: AI Leaders
│   └── styles/
│       └── global.css    # Tailwind directives + custom styles
├── public/               # Static assets (images, fonts, CNAME)
├── astro.config.mjs      # Astro configuration
├── tailwind.config.ts    # Tailwind + design tokens
├── tsconfig.json
└── package.json
```
