# URL Structure & SEO Routing — soft-tab.com

> **Status**: Draft — needs owner review
> **Last Updated**: 2026-02-11

---

## URL Map

| URL | Page | H1 Keyword Focus | Notes |
|-----|------|-------------------|-------|
| `/` | Homepage | AI-augmented software development | Root. All roads lead here and back. |
| `/services` | Services | Fractional software development services | Full service catalog + engagement models |
| `/about` | About | AI-assisted software development company | Story, values, credibility |
| `/contact` | Contact | Software development consultant contact | Form + Calendly. Conversion page. |
| `/for-founders` | For Founders | Software developer for non-technical founder | Persona page. Warm, reassuring tone. |
| `/for-engineering-leaders` | For Engineering Leaders | Team augmentation for overwhelmed CTO | Persona page. Peer-to-peer, technical. |
| `/for-ai-adoption` | For AI Adoption | AI training for software development teams | Persona page. Anti-hype, authoritative. |

**Total**: 7 pages.

---

## URL Conventions

- **Lowercase, hyphenated slugs**: `/for-founders`, not `/ForFounders` or `/for_founders`
- **No trailing slashes**: Astro default. Configure in `astro.config.mjs` if needed.
- **No file extensions**: `/services`, not `/services.html`
- **Descriptive and short**: Slugs match the page's purpose, not the H1 verbatim
- **Persona prefix**: `/for-` groups persona pages visually in analytics and sitemaps

---

## Breadcrumb Structure

Flat hierarchy. All pages are one level deep from root.

| Page | Breadcrumb |
|------|------------|
| Homepage | *(none, it's root)* |
| Services | Home > Services |
| About | Home > About |
| Contact | Home > Contact |
| For Founders | Home > For Founders |
| For Engineering Leaders | Home > For Engineering Leaders |
| For AI Adoption | Home > For AI Adoption |

Implement with `BreadcrumbList` schema markup on every page except the homepage.

---

## Anchor Links (In-Page Sections)

Some pages have sections that other pages link to directly.

| Anchor | Page | Purpose |
|--------|------|---------|
| `/services#engagement-models` | Services | Linked from About page |
| `/services#technologies` | Services | Linked from About page |
| `/#how-we-work` | Homepage | Linked from hero secondary CTA |

Keep anchor IDs stable. If section headings change, update anchors across all linking pages.

---

## Canonical URLs

Every page should include a `<link rel="canonical">` tag pointing to itself.

```
https://soft-tab.com/
https://soft-tab.com/services
https://soft-tab.com/about
https://soft-tab.com/contact
https://soft-tab.com/for-founders
https://soft-tab.com/for-engineering-leaders
https://soft-tab.com/for-ai-adoption
```

No www. HTTPS only. Redirect `www.soft-tab.com` to `soft-tab.com` at the DNS/hosting level.

---

## Redirect Plan

### From Old Site
The current `soft-tab.com` redirects to `tabuckner.github.io` (personal portfolio). At launch:

1. Remove the redirect from `soft-tab.com` to `tabuckner.github.io`
2. Point `soft-tab.com` DNS to GitHub Pages (new marketing site)
3. Keep `tabuckner.github.io` live as-is (personal portfolio, separate concern)

No page-to-page redirects needed since the old site has no indexed pages under the `soft-tab.com` domain.

### Future-Proofing
If URLs ever change, implement 301 redirects from old to new. Never let a published URL return a 404.

---

## Sitemap

Generate `sitemap.xml` automatically via Astro's sitemap integration.

```xml
<url><loc>https://soft-tab.com/</loc></url>
<url><loc>https://soft-tab.com/services</loc></url>
<url><loc>https://soft-tab.com/about</loc></url>
<url><loc>https://soft-tab.com/contact</loc></url>
<url><loc>https://soft-tab.com/for-founders</loc></url>
<url><loc>https://soft-tab.com/for-engineering-leaders</loc></url>
<url><loc>https://soft-tab.com/for-ai-adoption</loc></url>
```

Submit to Google Search Console after launch.

---

## robots.txt

```
User-agent: *
Allow: /
Sitemap: https://soft-tab.com/sitemap.xml
```

All pages are public and crawlable. No pages to block.

---

## Navigation Mapping

### Desktop Nav
```
[Logo]  Services  Who We Help ▾  About  [Contact - button]
                  ├── For Founders
                  ├── For Engineering Leaders
                  └── For AI Adoption
```

### Mobile Nav (Hamburger)
```
Services
Who We Help
  For Founders
  For Engineering Leaders
  For AI Adoption
About
Contact
```

### Footer Links
```
Services  |  About  |  Contact  |  For Founders  |  For Engineering Leaders  |  For AI Adoption
```

Plus: copyright, social links (LinkedIn at minimum).
