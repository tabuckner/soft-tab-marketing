# Soft-TAB Marketing Website & Brand Package

> **Status**: Phase 3+4 — Design & Development (in progress: SEO, form backend)
> **Last Updated**: 2026-02-11
> **Owner**: Taylor Buckner

---

## Vision

Transform Soft-TAB, LLC from a solo-contractor presence into a professional software engineering consultancy brand. The website and brand should communicate: _"You're hiring a team of seasoned professionals who will build your software right."_

**Note**: The value prop above is a placeholder. Phase 0 will sharpen this into something outcome-driven and differentiated (e.g., "Ship production-ready apps in weeks, not months" or "Senior engineers who code like they own the product").

## Current State

- `soft-tab.com` redirects to `tabuckner.github.io` (personal portfolio, outdated)
- No formal brand guidelines exist
- No dedicated marketing presence

## Goals

1. **Professional marketing website** at `soft-tab.com`
2. **Cohesive brand package** (logo, colors, typography, voice)
3. **Zero hosting cost** (or as close to it as possible)
4. **Vanity URL**: `soft-tab.com` must be the canonical address

## Success Metrics

**Baseline**: Effectively zero (no marketing site exists today).

### 30-Day Post-Launch Targets
| Metric | Target | How Measured |
|---|---|---|
| Weekly unique visitors | 50+ | GA4 |
| Avg time on site | > 1 minute | GA4 |
| Contact form submissions | 3+ total | Formspree dashboard |
| Discovery calls booked | 1+ | Manual tracking |
| Bounce rate | < 60% | GA4 |
| Lighthouse performance score | > 90 | Lighthouse audit |

### 90-Day Targets
| Metric | Target | How Measured |
|---|---|---|
| Weekly unique visitors | 200+ | GA4 |
| Monthly form submissions | 5+ | Formspree |
| Discovery calls / month | 2-3 | Manual tracking |
| Proposals sent | 1+ | Manual tracking |
| Top 3 persona page traffic split | Even-ish distribution | GA4 page analytics |

### Ongoing Health Checks
- Which persona page gets the most traffic? (Signals market demand)
- What's the top referral source? (Where to invest outreach)
- Which CTA gets the most clicks? (What messaging resonates)

These are starting targets from zero — we'll recalibrate after 90 days of real data.

## Project Constraints

- **Budget**: $0 for hosting/infrastructure. Minimal spend elsewhere.
- **Resources**: Solo owner (Taylor). AI-assisted development and content.
- **Timeline**: TBD — to be estimated after Phase 0.

---

## Out of Scope for V1

These are explicitly deferred to post-launch iterations:

- Blog or content management system
- Client portal or login
- Individual service landing pages
- Newsletter/email subscription
- Advanced animations beyond basic transitions
- Paid analytics or marketing tools
- Extensive accessibility auditing (basics only for V1)

## Design Decisions

### Typography: Inter ✅ DECIDED

- **Wordmark**: Inter (Semibold 600 or Bold 700)
- **Headings**: Inter (Semibold 600)
- **Body**: Inter (Regular 400)
- **Mono/Code**: TBD (JetBrains Mono or Fira Code if needed)
- **Source**: Google Fonts (free, variable font)
- **Wordmark text treatment**: "Soft-TAB" as-is (mixed case, hyphenated)
- **Wordmark gradient vs solid**: Context-dependent. Gradient for hero/featured placements. Solid (white on dark, neutral-800 on light) for nav bar and small sizes.

### Theme: Light + Dark Mode with Toggle ✅ DECIDED

- **Default**: Respect `prefers-color-scheme` (OS-level preference) on first visit
- **Toggle**: Sun/moon icon in nav header for manual override
- **Persistence**: Store user preference in `localStorage`, override OS preference when set
- **Implementation**: Tailwind `dark:` variants + CSS custom properties. Build both modes inline as components are developed — not as a separate pass.
- **Priority order**: Light mode is the primary design target. Dark mode adapts from it.

---

## Project Phases

### Phase 0: Positioning & Strategy
> _Before we design anything, know who we're talking to and what we're saying._

- [x] Define Ideal Client Profile (ICP) — 3 persona archetypes ✅
  - Persona 1: Non-Technical Founder ("don't know where to start")
  - Persona 2: Overwhelmed CTO ("can't hire fast enough")
  - Persona 3: AI-Curious Leader ("need AI expertise")
- [x] Competitive research — 10 competitor consultancies analyzed ✅ → `docs/competitor-analysis.md`
- [x] Define positioning pillars ✅ (4 pillars: AI-Augmented, Senior Expertise, Flexible, Rescue)
- [x] Write positioning statement ✅
- [x] Define primary value proposition ✅
- [x] Define supporting value props with proof points ✅ (proof points still need real data)
- [x] Define AI philosophy (anti-hype stance) ✅
- [x] Define engagement models (4 models, structure only) ✅ → `docs/positioning.md`
- [x] Define engagement process (flexible 5-step framework + discovery details) ✅ → `docs/positioning.md`
- [x] Design persona-specific website messaging paths ✅ (dedicated persona pages + homepage routing cards)
- [x] Define success KPIs ✅ (30-day and 90-day targets defined)
- [x] **Decision gate**: Tech stack selection ✅ (Astro + Tailwind + TypeScript)

**Exit Criteria**: ICP documented, positioning statement approved, engagement models refined, tech stack chosen, at least 2 testimonials requested.

→ Deliverables: `docs/positioning.md`, `docs/messaging-framework.md`, `docs/competitor-analysis.md`

### Phase 1: Brand Foundation ✅ COMPLETE
> _Establish the visual and verbal identity._

- [x] Establish brand pillars (values, voice, personality) ✅ → 4 pillars in positioning.md
- [x] Research competitor/inspiration sites ✅ → 47 Dribbble designs collected, 7 favorites selected
- [x] Document voice guidelines ✅ → voice matrix in brand-guidelines.md
- [x] Document tone-by-page guidance ✅ → persona-specific adjustments in brand-guidelines.md
- [x] Select color palette ✅ → full 11-step scales (primary, accent, neutral, semantic) + dark mode
- [x] Select typography system ✅ → Inter (400/600/700), full type scale with responsive matrix
- [x] Define spacing scale ✅ → 4px base grid, 14 spacing tokens
- [x] Define border radii, shadow/elevation levels, transition defaults ✅ → M3-based easing
- [x] Choose iconography approach ✅ → Lucide (line icons, 2px stroke, tree-shakable)
- [x] Decide visual style direction ✅ → North stars: M8 (light), B11 (dark)
- [x] Design logo/wordmark lockup variants ✅ → horizontal, stacked, icon-only with color variants
- [x] Document brand guidelines ✅ → `docs/brand-guidelines.md` (12 sections)
- [x] Document visual "don'ts" ✅ → in inspiration.md + brand-guidelines.md
- [x] Define component states (buttons, inputs, links, focus rings) ✅ → design-tokens.md
- [x] Define layout grid (columns, gutters, breakpoints) ✅ → design-tokens.md
- [x] Define touch target minimums ✅ → 44x44px
- [x] Define primary vs accent color usage guidance ✅ → 80/20 rule
- [x] Scaffold Astro project ✅ → Astro 5.17 + Tailwind CSS v4 + TypeScript (strict)

**Exit Criteria**: ✅ Met. Brand guidelines complete and approved. Color, type, logo locked. Project scaffolded.

→ Deliverables: `docs/brand-guidelines.md`, `docs/color-system.md`, `docs/design-tokens.md`, `docs/inspiration.md`, `docs/logo-lockups.html`

### Phase 2: Content & Information Architecture ✅ COMPLETE
> _What pages exist, what they say, and how they guide visitors to contact you._

- [x] SEO keyword research ✅ → `docs/seo-keywords.md` (32 keywords mapped to pages)
  - 10 service keywords, 12 problem keywords, 6 technology keywords, 4 long-tail variations
  - Primary keyword + 2-3 secondaries assigned per page
  - Meta titles and descriptions drafted
- [x] Define site pages/sections (information architecture) ✅ → `docs/architecture.md` (7 pages, section-by-section)
- [x] Map target keywords to pages ✅ → covered in `docs/seo-keywords.md` (32 keywords assigned to pages)
- [x] Write messaging framework ✅ → `docs/messaging-framework.md`
  - Tagline finalists: "Engineering, Augmented." / "Build faster. Build smarter."
  - Elevator pitches (10s, 30s, 2min) ✅
  - Per-page messaging goals ✅
- [ ] Draft page copy — core pages:
  - [x] Homepage (hero, "Who We Help" cards, services overview, social proof, process, CTA) ✅ → `docs/copy/homepage.md`
  - [x] Services (engagement models, outcomes, rescue/modernization angle) ✅ → `docs/copy/services.md`
  - [x] About (story, team positioning, credibility, process overview) ✅ → `docs/copy/about.md`
  - [x] Contact (low-friction form, expectations for what happens next) ✅ → `docs/copy/contact.md`
- [x] Draft page copy — persona pages:
  - [x] /for-founders ✅ → `docs/copy/for-founders.md`
  - [x] /for-engineering-leaders ✅ → `docs/copy/for-engineering-leaders.md`
  - [x] /for-ai-adoption ✅ → `docs/copy/for-ai-adoption.md`
- [ ] Write 3 mini case studies (deferred to Phase 6: True Up)
- [x] Plan CTAs per page ✅ → defined inline in each page's copy doc
- [x] Define FAQ content ✅ → `docs/copy/faq.md` (16 Q&As mapped to pages)
- [x] Plan URL structure for SEO ✅ → `docs/url-structure.md` (URLs, breadcrumbs, anchors, redirects, sitemap, nav)

**Exit Criteria**: All page copy drafted and reviewed. Case studies written. IA finalized.

→ Deliverables: `docs/content.md`, `docs/architecture.md`

### Phase 3+4: Design & Development (Merged) ✅ COMPLETE
> _Design in code — built mobile-first, component by component._

- [x] Collect design inspiration ✅ → 47 references in `docs/inspiration.md`, 7 favorites selected
- [x] Define visual direction ✅ → North stars locked (M8 light, B11 dark)
- [x] Define design tokens ✅ → `docs/design-tokens.md` (spacing, type, radii, shadows, transitions, states, grid)
- [x] Define breakpoints ✅ → Standard Tailwind (640/768/1024/1280/1536)
- [x] Implement design tokens as CSS custom properties ✅ → `src/styles/global.css` (@theme + CSS vars + @utility)
- [x] Build component library ✅
  - **Atoms**: Button (primary/secondary/tertiary, 3 sizes), Container, Section
  - **Layout**: Header (sticky, dropdown, mobile nav), Footer, ThemeToggle, SkipToContent
  - **Blocks**: Hero, CTABlock, StatsRow, PersonaCard, ServiceCard, DifferentiatorBlock, ProcessStep, FAQAccordion, TestimonialCard, ContactForm, HeroGraphic
- [x] Build all 7 pages ✅
  - Homepage (hero, Who We Help, services overview, differentiators, social proof, process, CTA)
  - Services (service cards, engagement models, technologies, FAQ)
  - About (story + photo, values, credibility stats, FAQ)
  - Contact (form + sidebar with process steps)
  - /for-founders (persona layout)
  - /for-engineering-leaders (persona layout)
  - /for-ai-adoption (persona layout)
- [x] PersonaLayout shared template for all 3 persona pages ✅
- [x] Implement responsive design ✅ → mobile-first, tested at standard breakpoints
- [x] Implement dark mode ✅ → CSS custom properties, OS preference + localStorage toggle
- [x] Basic accessibility ✅ → semantic HTML, alt text, focus-visible, skip-to-content
- [x] Design polish ✅ → animated gradient borders, hero graphic, scroll reveal, dot grid pattern, view transitions
- [x] SEO: Meta tags and OG tags per page ✅ → BaseLayout with title, description, canonical, OG/Twitter
- [x] SEO: robots.txt ✅ → `public/robots.txt`
- [x] SEO: XML sitemap ✅ → `@astrojs/sitemap` integration
- [x] SEO: Schema.org structured data ✅ → Organization, Service, FAQ, BreadcrumbList (JSON-LD)
- [x] SEO: OG default image ✅ → `public/og-default.png` (1200×630 branded image for social sharing)
- [x] Performance optimization (Lighthouse > 90) ✅ → All 7 pages score 99-100 across all categories
- [x] Set up GA4 (free) for basic analytics ✅ → Measurement ID G-11B3WEL5RN in BaseLayout
- [x] Contact form backend (Formspree free tier) ✅ → fetch-based submission, branded success/error states
- [x] Calendly booking link wired up ✅ → `https://calendly.com/taylor-soft-tab/30min`

**Exit Criteria**: All pages built, responsive, Lighthouse > 90, form working.

### Phase 5: Infrastructure & Launch Prep
> _DNS, hosting, and go-live readiness._

- [ ] Configure GitHub Pages with custom domain (`soft-tab.com`)
- [ ] Configure DNS (CNAME → GitHub Pages)
- [ ] Verify HTTPS via GitHub Pages
- [ ] Cross-browser testing (Chrome, Safari, Firefox — desktop + mobile)
- [ ] Test contact form end-to-end
- [ ] Verify analytics tracking
- [ ] Submit sitemap to Google Search Console
- [ ] Plan DNS cutover (document rollback plan)
- [ ] Add day-job unavailability blocks to Calendly (manually input recurring work hours to prevent conflicts)

**Exit Criteria**: Site accessible at `soft-tab.com`, all tests pass, analytics verified.

### Phase 6: True Up
> _Replace every placeholder with real data before going live._

- [ ] Verify homepage stats (years experience, projects delivered, speed multiplier)
- [ ] Source 2-3 real client testimonials (with name, title, company)
- [ ] Secure client logo permissions for logo strip
- [ ] Finalize tagline selection ("Engineering, Augmented." vs "Build faster. Build smarter.") against live mockups
- [ ] Audit all page copy for placeholder text (search for "TBD", "placeholder", "when available")
- [ ] Confirm all claims and numbers are accurate and defensible
- [ ] Write 3 mini case studies with real metrics (problem → solution → results)
- [ ] Finalize "About" page bio / founding story with owner
- [ ] Review FAQ answers for accuracy
- [ ] Final tone/voice pass — read every page aloud, flag anything that doesn't sound like Soft-TAB

**Exit Criteria**: Zero placeholder content remains. All stats verified. Testimonials and case studies are real.

### Phase 7: Launch & Iterate
> _Go live, then improve based on data._

**Pre-Launch**:
- [ ] Gather social proof — reach out to past clients for 2-3 testimonials
- [ ] Audit past projects for case study candidates (3 minimum, include rescue stories)
- [ ] Integrate testimonials and case studies into site

**Soft Launch** (MVP):
- [ ] Go live: point `soft-tab.com` to new site
- [ ] Verify everything works in production
- [ ] Post to LinkedIn, notify network

**Post-Launch**:
- [ ] Monitor analytics for first 2 weeks
- [ ] Gather feedback from trusted contacts
- [ ] Post-launch polish based on feedback
- [ ] Plan ongoing iteration cadence:
  - Add new case studies quarterly as projects complete
  - Refresh service descriptions as offerings evolve
  - Update testimonials as they come in
  - Consider blog addition in future phase

---

## Key Decisions

### Hosting: GitHub Pages ✅ DECIDED

**Decision**: GitHub Pages with custom domain.
**Why**: Free, reliable, supports custom domains with auto-HTTPS, works with any static site generator, already familiar with GitHub workflow.

**Setup**: Add CNAME record pointing `soft-tab.com` → GitHub Pages. GitHub auto-provisions HTTPS.

### Tech Stack ✅ DECIDED

```
Framework:    Astro + TypeScript
Styling:      Tailwind CSS (brand tokens in tailwind.config.ts)
Static UI:    Custom Astro components (hero, cards, sections, footer)
Interactive:  Headless UI or Radix Primitives (dropdown, tabs, mobile menu)
                → skinned with Tailwind, fully accessible
Hosting:      GitHub Pages (custom domain: soft-tab.com)
CI/CD:        GitHub Actions (build Astro → deploy to Pages)
Forms:        Formspree (free tier)
Analytics:    GA4 (free)
Scheduling:   Calendly (free tier, embedded)
```

**Why Astro**: Purpose-built for content/marketing sites. Ships zero JS by default. First-class TypeScript. Acquired by Cloudflare (Jan 2026). Used by Visa, Microsoft, Adobe, NBC News. 113 releases in 2025. Rock solid.

**Why Tailwind (no full UI library)**: Brand-first site needs to look like Soft-TAB, not like a template. Tailwind provides utilities; we compose the brand visually. Headless primitives handle accessible interactive pieces (dropdowns, tabs, dialogs) without imposing visual opinions.

**Why not Next.js**: Overkill. Ships a React runtime for a site that's mostly static HTML.
**Why not MUI/shadcn**: Pre-built component look conflicts with unique brand goals.

See `docs/tech-decisions.md` for full rationale.

### Domain / DNS

- `soft-tab.com` is already owned (currently redirecting)
- **Action needed**: Confirm which registrar manages the domain
- DNS change: Add CNAME record pointing to `<username>.github.io`
- Backup: Keep old redirect working until new site is verified

### Contact Form (Static Site Compatible)

| Option | Cost | Features |
|---|---|---|
| **Formspree** | Free (50 submissions/mo) | Simple, reliable, spam filtering |
| Calendly embed | Free tier | Direct call booking, removes email back-and-forth |
| Google Forms embed | Free | Works but looks unprofessional |
| mailto: link | Free | Zero friction but no tracking |

**Recommendation**: Formspree for form + optional Calendly link for direct booking.

---

## Risk Register

| ID | Risk | Probability | Impact | Mitigation |
|---|---|---|---|---|
| R1 | Tech stack decision paralysis | Medium | High | Default to Astro if no clear winner by end of Phase 0 |
| R2 | Brand direction changes mid-development | Medium | High | Lock brand guidelines with approval gate before Phase 3 |
| R3 | DNS issues during cutover | Medium | Medium | Test with staging subdomain first. Document rollback. |
| R4 | Content bottleneck (single owner) | High | Medium | Use AI-assisted drafting. Set "good enough" threshold for V1. |
| R5 | Scope creep (blog, animations, extra pages) | High | High | Enforce Out of Scope list. Defer to post-launch. |
| R6 | Contact form needs backend | Medium | Medium | Decide Formspree/Calendly in Phase 0, validate early. |
| R7 | Old site conflicts during cutover | Low | Low | Plan redirect strategy before DNS change. |

---

## Brand Direction (Working Notes)

### What We Know
- Name: **Soft-TAB, LLC**
- Industry: Software Engineering Services (Contract)
- Positioning: Professional consultancy (not a freelancer)
- Reality: Solo practitioner with subcontractors, presenting as a team
- Tone: Confident, technical, approachable but not casual

### Voice Guidelines (Draft)

| Attribute | We Are | We Are Not | Example |
|---|---|---|---|
| Technical | Precise, uses proper terminology | Jargon-heavy, condescending | "We architect scalable microservices" not "We leverage bleeding-edge paradigms" |
| Confident | Decisive, opinionated, experienced | Arrogant, dismissive | "We recommend PostgreSQL for this use case" not "Only amateurs use X" |
| Approachable | Clear, conversational, human | Overly casual, unprofessional | "Let's talk through your project" not "Yo, hit us up!" |
| Client-Focused | Outcomes first, tech second | Technology-obsessed | "We'll cut your deploy time from weeks to hours" not "We use CI/CD with containerized workflows" |

### What We Need to Define (Phase 0-1)
- Ideal Client Profile
- Positioning statement
- Logo / wordmark treatment
- Primary + secondary color palette
- Typography (heading + body fonts)
- Spacing scale, shadows, radii, transitions
- Iconography approach
- Visual style (real photos + line illustrations + subtle abstract)

---

## Inspiration & Research

> To be populated during Phase 0-1. See `docs/inspiration.md` when created.

---

## File Index

| File | Purpose | Status |
|---|---|---|
| `PROJECT.md` | Master plan and status tracker | Active |
| `docs/brand-guidelines.md` | **Master brand reference** — 12 sections covering all brand decisions | ✅ Complete |
| `docs/color-system.md` | Full color palette — primary, accent, neutral, semantic, dark mode | ✅ Complete |
| `docs/design-tokens.md` | Spacing, typography, radii, shadows, transitions, component states, layout grid | ✅ Complete |
| `docs/inspiration.md` | 47 Dribbble references, 7 favorites, visual direction locked | ✅ Complete |
| `docs/positioning.md` | ICP, personas, competitive landscape, pillars, engagement models | ✅ Complete |
| `docs/messaging-framework.md` | Taglines, elevator pitches, page-by-page value props, objection handling | ✅ Complete |
| `docs/competitor-analysis.md` | 10 competitor firms analyzed, market gaps, positioning map | ✅ Complete |
| `docs/architecture.md` | Site map, 7 page-by-page section outlines, navigation structure | ✅ Complete |
| `docs/tech-decisions.md` | Tech stack rationale, alternatives, project structure | ✅ Complete |
| `docs/logo.png` | Logo mark (stylized S on gradient) | ✅ Asset |
| `docs/logo-lockups.html` | Interactive preview — horizontal, stacked, icon-only lockups | ✅ Complete |
| `docs/wordmark-preview.html` | Font comparison preview (Inter selected) | ✅ Archive |
| `docs/inspiration-gallery.html` | Interactive gallery of 47 Dribbble references | ✅ Archive |
| `docs/seo-keywords.md` | 32 target keywords mapped to pages, meta titles/descriptions, content strategy | ✅ Complete |
| `docs/copy/homepage.md` | Homepage copy — 7 sections | Draft (Phase 2) |
| `docs/copy/services.md` | Services page copy — 5 sections | Draft (Phase 2) |
| `docs/copy/about.md` | About page copy — 6 sections | Draft (Phase 2) |
| `docs/copy/contact.md` | Contact page copy — 4 sections | Draft (Phase 2) |
| `docs/copy/for-founders.md` | For Founders persona page copy — 7 sections | Draft (Phase 2) |
| `docs/copy/for-engineering-leaders.md` | For Engineering Leaders persona page copy — 7 sections | Draft (Phase 2) |
| `docs/copy/for-ai-adoption.md` | For AI Adoption persona page copy — 7 sections | Draft (Phase 2) |
| `docs/copy/faq.md` | FAQ content — 16 Q&As mapped to pages | Draft (Phase 2) |
| `docs/url-structure.md` | URL structure, breadcrumbs, anchors, redirects, sitemap, nav | Draft (Phase 2) |
| `src/` | Astro project source | Scaffolded |
