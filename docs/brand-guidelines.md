# Soft-TAB Brand Guidelines

> **Status**: Approved — V1 Complete
> **Last Updated**: 2026-02-11
> **Source Documents**: `color-system.md`, `design-tokens.md`, `inspiration.md`, `positioning.md`, `messaging-framework.md`

This is the single reference for anyone building, designing, or writing for Soft-TAB. If this document and a source document disagree, this document wins.

---

## 1. Brand Overview

**Company**: Soft-TAB, LLC
**Type**: Software engineering consultancy
**Founded by**: Taylor Buckner
**Website**: soft-tab.com

### Positioning Statement

Soft-TAB is the engineering partner that founders, CTOs, and technology leaders call when they need senior talent that ships fast. We combine deep engineering expertise with AI-augmented development workflows to deliver outcomes that would normally require a much larger, more expensive team.

### Tagline Finalists (final selection against mockups)

1. **"Engineering, Augmented."**
2. **"Build faster. Build smarter."**

### Four Pillars

1. **AI-Augmented Delivery** — AI is how we work, not what we sell
2. **Senior Expertise** — Every engagement led by experienced engineers
3. **Flexible by Design** — Project, fractional, advisory, training
4. **The Rescue Factor** — We thrive where others have failed

---

## 2. Logo

### The Mark

A stylized "S" with tab/arrow motifs on a blue→cyan gradient background. Rounded square format (app icon style).

**File**: `docs/logo.png`

### Lockup Variants

| Variant | Usage | Reference |
|---------|-------|-----------|
| **Horizontal** | Nav headers, email signatures, invoices, partner rows | Primary lockup — icon left, "Soft-TAB" right |
| **Stacked** | Loading screens, centered layouts, social profiles, presentations | Icon on top, "Soft-TAB" below |
| **Icon only** | Favicon, browser tab, mobile icon, social avatar, small UI | Logo mark without text |

**Preview**: `docs/logo-lockups.html`

### Wordmark Treatment

- **Font**: Inter, 600 weight (semibold)
- **Text**: "Soft-TAB" (capital S, lowercase oft, hyphen, all-caps TAB)
- **Letter spacing**: -0.02em
- **Solid colors**: `neutral-800` (#2A3745) on light, `neutral-100` (#F1F5F7) on dark
- **Gradient text**: Brand gradient (`#0779E5 → #36D1DC`) for hero/featured placements
- **Dark mode gradient**: Lighter variant (`#5DAFF7 → #6FDFE7`)
- **Monochrome**: `primary-500` (#0779E5) when solid brand color is needed

### Logo Rules

- **Clear space**: Minimum padding around any lockup = 1x the icon height
- **Minimum sizes**: Horizontal 120px wide, stacked 80px wide, icon 16px (favicon) / 32px (UI)
- **Icon border radius**: ~20% of icon width (32px icon = 7px radius, 48px = 10px, 64px = 14px)
- **Never**: Alter the icon's gradient, rotate the icon, add effects/shadows to the icon, place on busy backgrounds without sufficient contrast

---

## 3. Color

Full palette in `docs/color-system.md`. Key values below.

### Brand Colors

| Name | Hex | Role |
|------|-----|------|
| **Azure Blue** | `#0779E5` | Primary — actions, authority, CTAs, links, focus rings |
| **Strong Cyan** | `#36D1DC` | Accent — secondary CTAs, highlights, decorative, gradient endpoint |

**Usage ratio**: Primary 80%, Accent 20%.

### Brand Gradient

```css
/* Light mode */
linear-gradient(135deg, #0779E5 0%, #36D1DC 100%)

/* Dark mode (lighter, less saturated) */
linear-gradient(135deg, #5DAFF7 0%, #6FDFE7 100%)
```

**Use for**: Hero headline text (background-clip), logo overlays, featured section accents.
**Don't**: Fill entire backgrounds with the gradient. Use `--gradient-subtle` (15% opacity) for background washes.

### Primary vs Accent: When to Use Which

| | Primary (Azure Blue) | Accent (Strong Cyan) |
|---|---|---|
| Buttons | Solid primary button | Outline/ghost secondary button |
| Text | Links, branded text | Decorative only — not for body text |
| UI | Focus rings, active states, nav indicators | Tags, badges, hover accents |
| Gradient | Starts the gradient | Ends the gradient |
| Frequency | 80% of colored elements | 20% of colored elements |

### Neutral Palette

Cool-toned (blue-tinted), not pure gray. Key values:

- **Page background**: `#FAFBFC` (light) / `#0F1419` (dark)
- **Card background**: `#FFFFFF` (light) / `#1A232E` (dark)
- **Body text**: `#2A3745` (light) / `#F1F5F7` (dark)
- **Secondary text**: `#506176` (light) / `#CFD8E3` (dark)
- **Borders**: `#E4EAF0` (light) / `rgba(255, 255, 255, 0.1)` (dark)

### Semantic Colors

| State | Color | Background |
|-------|-------|------------|
| Success | `#10B981` | `#EEFBF4` |
| Warning | `#F59E0B` | `#FFFBEB` |
| Error | `#EF4444` | `#FEF2F2` |

---

## 4. Typography

### Typeface

**Inter** — variable font from Google Fonts.

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap');
font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif;
```

### Weight Rules

Only 3 weights. No exceptions.

| Weight | Name | Usage |
|--------|------|-------|
| **400** | Regular | Body text, descriptions, captions, metadata |
| **600** | Semibold | All headings (h1–h4), card titles, nav links, button text |
| **700** | Bold | Hero headlines only (text-6xl / text-7xl) |

**Rule**: No more than 2 font weights visible in any single section.

### Type Scale

| Token | Size | Usage |
|-------|------|-------|
| `text-xs` | 12px | Captions, labels |
| `text-sm` | 14px | Secondary text |
| `text-base` | 16px | Body text |
| `text-lg` | 18px | Lead paragraphs |
| `text-xl` | 20px | Card titles |
| `text-2xl` | 24px | Section sub-headings (h4) |
| `text-3xl` | 30px | Section headings (h3) |
| `text-4xl` | 36px | Page sub-headings (h2) |
| `text-5xl` | 48px | Page headings (h1) |
| `text-6xl` | 60px | Hero headline (desktop) |
| `text-7xl` | 72px | Hero headline (large screens) |

### Responsive Headlines

| Breakpoint | Hero | h1 | h3 |
|------------|------|----|----|
| < 640px | 36px | 30px | 24px |
| 768px | 48px | 36px | 30px |
| 1024px | 60px | 48px | 30px |
| >= 1280px | 72px | 48px | 30px |

Body text stays at 16px across all breakpoints.

---

## 5. Dark Mode

**Strategy**: Ship both light and dark. Default to OS preference (`prefers-color-scheme`). User can override via toggle. Preference stored in `localStorage`.

### Implementation

```css
:root { /* light mode tokens */ }

@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) { /* dark mode tokens */ }
}

[data-theme="dark"] { /* dark mode tokens (manual override) */ }
```

### Dark Mode Principles

- **Elevation**: Lighter = more elevated (opposite of light mode shadows)
- **Brand colors**: Use 300–400 range instead of 500–600 (less harsh)
- **Borders**: `rgba(255, 255, 255, 0.1)` instead of neutral-200
- **Gradient text**: Use lighter variant (`#5DAFF7 → #6FDFE7`)
- **Shadows**: Reduced opacity — elevation communicated through surface color, not shadow

---

## 6. Visual Direction

### North Stars

- **Light mode**: M8 (ECI corporate) — premium, generous whitespace, strong type hierarchy, real photography
- **Dark mode**: B11 (Buildly) — deep navy, ultra-clean, centered hero, gradient text, maximum confidence

### Recurring Patterns

- Bold hero headlines (large, confident, not decorative)
- Stats/trust rows (number callouts as social proof)
- Real photography (professional, not stock-feeling)
- Structured grid sections (service cards in clean rows)
- Generous whitespace (content breathes, nothing cramped)
- Partner/client logos (logo strip for credibility)
- Strategic blue accents (CTAs and highlights only)

### Visual "Don'ts"

- No busy/cluttered layouts
- No heavy gradient backgrounds or floating blobs
- No illustration-heavy aesthetics
- No rounded "friendly SaaS" style (bubble buttons, playful colors)
- No neon/glow effects
- No isometric devices, circuit boards, or AI-generated imagery
- No generic stock photography
- No more than 2 font weights visible in any single section

### Photography Guidelines

- **Subject**: Office environments, architecture, clean workspaces, team collaboration
- **Style**: High-contrast, slightly desaturated, professional/editorial feel
- **Avoid**: Posed handshakes, overly staged group shots, people pointing at screens, whiteboards with buzzwords
- **Treatment**: Dark gradient overlay on hero images for text contrast
- **Sources**: Unsplash (curated), custom photography preferred

---

## 7. Spacing & Layout

### Spacing Scale

4px base grid. All spacing uses multiples of 4. Aligns with Tailwind defaults.

Key values: 4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 80 / 96 / 128px.

### Layout Grid

| Breakpoint | Columns | Gutter |
|------------|---------|--------|
| < 640px (mobile) | 4 | 16px |
| 768px (tablet) | 8 | 24px |
| 1024px+ (desktop) | 12 | 24–32px |

**Container**: Max 1280px, centered.
**Narrow content**: Max 768px (text-heavy blocks).
**Full-bleed**: Hero, partner logos, footer.

### Section Vertical Padding

- Desktop: 80px top and bottom
- Tablet: 64px
- Mobile: 48px

---

## 8. Components

### Border Radius

- **Buttons / Inputs**: 8px
- **Cards / Modals**: 12px
- **Featured cards**: 16px
- **Pills / Badges**: 24px
- **Avatars**: Full circle

### Shadows (Light Mode)

Subtle, cool-toned (using `rgba(26, 35, 46, ...)` — not black).

| Level | Usage |
|-------|-------|
| `shadow-xs` | Buttons at rest |
| `shadow-sm` | Cards, input focus |
| `shadow-md` | Hovered cards, dropdowns |
| `shadow-lg` | Modals, popovers |
| `shadow-brand` | Primary CTA hover glow (blue-tinted) |

Dark mode: Shadows reduced. Elevation communicated through lighter surface colors.

### Buttons

**Three tiers:**

| Tier | Style | Usage |
|------|-------|-------|
| **Primary** | Solid blue (#0779E5), white text | Main CTA — "Book a Call", "Get Started" |
| **Secondary** | Blue outline, transparent background | Supporting action — "View Services", "Learn More" |
| **Tertiary** | Text-only, blue | Low-emphasis — inline links, "Read more" |

**Three sizes**: sm (36px), md (44px), lg (52px). Default is md.

**States**: Default → Hover (darker + shadow-brand) → Active (darkest + scale 0.98) → Focus (2px ring) → Disabled (grayed out, 60% opacity)

### Form Inputs

- Height: 44px
- Border: 1px neutral-300 (light), rgba(255,255,255,0.1) (dark)
- Focus: 1.5px primary-500 border + shadow-sm
- Error: 1.5px error-500 border + error-50 background
- Label: Above input, text-sm, secondary color

### Focus Rings

All interactive elements: 2px solid primary-500, 2px offset.
Dark mode: 2px solid primary-400, 2px offset.

### Touch Targets

Minimum 44 x 44px for all interactive elements (buttons, icon buttons, nav links, inputs).

---

## 9. Motion

Based on Material Design 3 easing principles. Subtle and quick.

### Easing Functions

| Function | Curve | When |
|----------|-------|------|
| **Standard** | `cubic-bezier(0.4, 0, 0.2, 1)` | Default. On-screen transitions (hover, color, transform) |
| **Decelerate** | `cubic-bezier(0, 0, 0.2, 1)` | Elements entering (dropdowns, modals, fade-in) |
| **Accelerate** | `cubic-bezier(0.4, 0, 1, 1)` | Elements leaving (dropdown close, toast dismiss) |

### Durations

| Speed | Duration | Usage |
|-------|----------|-------|
| Short | 150ms | Color changes, opacity, hover |
| Medium | 200ms | Button hovers, card lifts, focus |
| Medium2 | 250ms | Content entering |
| Long | 300ms | Modals, accordions |

### Reduced Motion

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## 10. Iconography

**Library**: [Lucide](https://lucide.dev) (open source, 1400+ icons, tree-shakable)

- **Style**: Line icons only, 2px stroke at 24px
- **Sizes**: 16–20px inline, 24px default, 32–40px feature accents
- **Color**: Inherit from parent text — no fixed icon colors
- **No**: Filled icons, multi-color icons, mixing icon libraries

---

## 11. Voice & Tone

### Brand Voice

| Attribute | What it means | What it doesn't mean |
|-----------|---------------|----------------------|
| **Confident** | We know our craft and aren't afraid to say so | Not arrogant or dismissive |
| **Direct** | Clear language, no fluff, say what we mean | Not blunt or cold |
| **Technical** | We speak the language of engineers | Not jargon-heavy for non-technical audiences |
| **Human** | Relatable, occasionally witty, never robotic | Not overly casual or meme-y |

### Writing Rules

- Use "we" (not "I") — present as a team
- Lead with outcomes, not features
- Short sentences. Short paragraphs. Let content breathe.
- No buzzwords without substance ("leverage", "synergize", "disrupt")
- AI references: practical, grounded, anti-hype ("We don't vibe-code your app")
- CTAs are specific: "Book a discovery call" not "Contact us"

### Persona-Specific Tone Adjustments

| Audience | Adjust toward |
|----------|---------------|
| Non-technical founders | Warmer, more reassuring, less jargon |
| CTOs / engineering leaders | More technical, peer-to-peer, respect their expertise |
| AI-curious leaders | Educational but not patronizing, practical over theoretical |

---

## 12. File Index

| File | Contents |
|------|----------|
| `docs/brand-guidelines.md` | This document — master reference |
| `docs/color-system.md` | Full color palette with all hex values, contrast ratios, dark mode |
| `docs/design-tokens.md` | Spacing, typography, radii, shadows, transitions, states, layout grid |
| `docs/inspiration.md` | Visual direction, Dribbble references, north stars, don'ts |
| `docs/positioning.md` | ICP, personas, competitive landscape, pillars, engagement models |
| `docs/messaging-framework.md` | Taglines, elevator pitches, page-by-page value props, objection handling |
| `docs/competitor-analysis.md` | 10 competitor firms analyzed, market gaps, positioning map |
| `docs/architecture.md` | Site map, page-by-page section outlines, navigation structure |
| `docs/tech-decisions.md` | Tech stack rationale, alternatives considered, project structure |
| `docs/logo.png` | Logo mark (stylized S on gradient) |
| `docs/logo-lockups.html` | Interactive preview of horizontal, stacked, icon-only lockups |
| `docs/wordmark-preview.html` | Font comparison preview (Inter selected) |
| `docs/inspiration-gallery.html` | Interactive gallery of 47 Dribbble references |
