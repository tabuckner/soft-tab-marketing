# Soft-TAB Design Tokens

> **Status**: Approved
> **Last Updated**: 2026-02-11
> **Complements**: `color-system.md` (colors + dark mode), `inspiration.md` (visual direction)

---

## Spacing Scale

4px base grid. All spacing uses multiples of 4.

| Token | Value | Usage |
|-------|-------|-------|
| `space-0` | `0px` | Reset |
| `space-1` | `4px` | Tight inner padding (icon gaps, badge padding) |
| `space-2` | `8px` | Small gaps (between inline elements, input padding) |
| `space-3` | `12px` | Default inner padding (buttons, tags) |
| `space-4` | `16px` | Standard gap (form fields, card padding, list items) |
| `space-5` | `20px` | Medium padding |
| `space-6` | `24px` | Card padding, section inner spacing |
| `space-8` | `32px` | Large card padding, group spacing |
| `space-10` | `40px` | Section dividers |
| `space-12` | `48px` | Between content blocks |
| `space-16` | `64px` | Section padding (vertical) |
| `space-20` | `80px` | Large section padding |
| `space-24` | `96px` | Hero section padding |
| `space-32` | `128px` | Page-level vertical rhythm |

### Tailwind Mapping

These align with Tailwind's default spacing scale (`p-1` = 4px, `p-4` = 16px, `p-8` = 32px, etc.), so no custom config needed for most values.

---

## Typography Scale

Font: **Inter** (variable, Google Fonts)

| Token | Size | Line Height | Weight | Usage |
|-------|------|-------------|--------|-------|
| `text-xs` | `12px` | `16px` (1.33) | 400 | Captions, labels, metadata |
| `text-sm` | `14px` | `20px` (1.43) | 400 | Secondary text, descriptions |
| `text-base` | `16px` | `24px` (1.5) | 400 | Body text |
| `text-lg` | `18px` | `28px` (1.56) | 400 | Large body, lead paragraphs |
| `text-xl` | `20px` | `28px` (1.4) | 600 | Card titles, sub-headings |
| `text-2xl` | `24px` | `32px` (1.33) | 600 | Section sub-headings (h4) |
| `text-3xl` | `30px` | `36px` (1.2) | 600 | Section headings (h3) |
| `text-4xl` | `36px` | `40px` (1.11) | 600 | Page sub-headings (h2) |
| `text-5xl` | `48px` | `52px` (1.08) | 600 | Page headings (h1) |
| `text-6xl` | `60px` | `64px` (1.07) | 700 | Hero headline (desktop) |
| `text-7xl` | `72px` | `76px` (1.06) | 700 | Hero headline (large screens) |

### Font Weight Rules

Only 3 weights ship. No exceptions.

| Weight | Name | Usage |
|--------|------|-------|
| **400** | Regular | Body text, descriptions, captions, metadata — everything at `text-base` and below |
| **600** | Semibold | All headings (h1–h4), card titles, nav links, button text |
| **700** | Bold | Hero headlines only (`text-6xl` / `text-7xl`) |

Rule: No more than 2 font weights visible in any single section.

### Font Loading

```css
/* Google Fonts — only ship 3 weights */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap');

/* Fallback stack */
font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif;
```

### Responsive Type Strategy

| Breakpoint | Hero Headline | Page Heading (h1) | Section Heading (h3) |
|------------|---------------|--------------------|-----------------------|
| `< 640px` | `text-4xl` (36px) | `text-3xl` (30px) | `text-2xl` (24px) |
| `640–767px` | `text-4xl` (36px) | `text-4xl` (36px) | `text-2xl` (24px) |
| `768–1023px` | `text-5xl` (48px) | `text-4xl` (36px) | `text-3xl` (30px) |
| `1024–1279px` | `text-6xl` (60px) | `text-5xl` (48px) | `text-3xl` (30px) |
| `>= 1280px` | `text-7xl` (72px) | `text-5xl` (48px) | `text-3xl` (30px) |

Body text stays at `text-base` (16px) across all breakpoints.

---

## Border Radius

Clean and modern — not too sharp, not too rounded. Matches the M8/C8 visual direction.

| Token | Value | Usage |
|-------|-------|-------|
| `radius-none` | `0px` | Sharp edges (decorative) |
| `radius-sm` | `4px` | Tags, badges, small elements |
| `radius-md` | `8px` | Buttons, inputs, small cards |
| `radius-lg` | `12px` | Cards, modals, larger containers |
| `radius-xl` | `16px` | Featured cards, hero elements |
| `radius-2xl` | `24px` | Pills (e.g., status badges, nav pills) |
| `radius-full` | `9999px` | Circles (avatars, round buttons) |

### Default by Component
- **Buttons**: `radius-md` (8px)
- **Input fields**: `radius-md` (8px)
- **Cards**: `radius-lg` (12px)
- **Modals/dialogs**: `radius-lg` (12px)
- **Badges/tags**: `radius-sm` (4px) or `radius-2xl` (24px) for pills
- **Avatar**: `radius-full`

---

## Shadows / Elevation

Subtle, cool-toned shadows that complement the blue-tinted neutral palette. No harsh black shadows.

### Light Mode

| Token | Value | Usage |
|-------|-------|-------|
| `shadow-xs` | `0 1px 2px rgba(26, 35, 46, 0.05)` | Subtle lift (buttons at rest) |
| `shadow-sm` | `0 1px 3px rgba(26, 35, 46, 0.08), 0 1px 2px rgba(26, 35, 46, 0.04)` | Cards, input focus |
| `shadow-md` | `0 4px 6px rgba(26, 35, 46, 0.07), 0 2px 4px rgba(26, 35, 46, 0.04)` | Hovered cards, dropdowns |
| `shadow-lg` | `0 10px 15px rgba(26, 35, 46, 0.08), 0 4px 6px rgba(26, 35, 46, 0.04)` | Modals, popovers |
| `shadow-xl` | `0 20px 25px rgba(26, 35, 46, 0.10), 0 8px 10px rgba(26, 35, 46, 0.04)` | Elevated overlays |
| `shadow-brand` | `0 4px 14px rgba(7, 121, 229, 0.25)` | Additive glow on primary CTA hover (used alongside color/transform changes) |

### Dark Mode

In dark mode, shadows are less visible. Elevation is communicated through **lighter surface colors** instead (per color-system.md). Shadows are reduced:

| Token | Dark Mode Value | Notes |
|-------|-----------------|-------|
| `shadow-xs` | `0 1px 2px rgba(0, 0, 0, 0.2)` | Barely visible |
| `shadow-sm` | `0 1px 3px rgba(0, 0, 0, 0.3)` | Subtle |
| `shadow-md` | `0 4px 6px rgba(0, 0, 0, 0.3)` | Cards |
| `shadow-lg` | `0 10px 15px rgba(0, 0, 0, 0.4)` | Modals |
| `shadow-brand` | `0 4px 14px rgba(93, 175, 247, 0.20)` | Uses primary-400 for glow |

---

## Transitions & Motion

Based on Material Design 3 easing principles. Subtle and quick — nothing flashy.

### Easing Functions

| Token | Curve | M3 Name | When to Use |
|-------|-------|---------|-------------|
| `ease-standard` | `cubic-bezier(0.4, 0.0, 0.2, 1)` | Standard / FastOutSlowIn | **Default.** Elements already on screen — hover states, color changes, transforms, card lifts |
| `ease-decelerate` | `cubic-bezier(0.0, 0.0, 0.2, 1)` | Decelerated / LinearOutSlowIn | Elements **entering** — dropdowns opening, modals appearing, content fading in, tooltips |
| `ease-accelerate` | `cubic-bezier(0.4, 0.0, 1.0, 1.0)` | Accelerated / FastOutLinearIn | Elements **leaving** — dropdown closing, toast dismissal, modal exit |

### Duration Scale

Aligned with M3 duration tokens.

| Token | Value | M3 Equivalent | Usage |
|-------|-------|---------------|-------|
| `duration-short` | `150ms` | Short2 | Color changes, opacity, icon swaps |
| `duration-medium` | `200ms` | Medium1 | Button hovers, card lifts, focus states |
| `duration-medium2` | `250ms` | Medium2 | Content entering (dropdowns, fade-ins) |
| `duration-long` | `300ms` | Long1 | Modals, overlays, accordions |

### Composed Transitions

| Token | Duration + Easing | Usage |
|-------|-------------------|-------|
| `transition-fast` | `150ms cubic-bezier(0.4, 0, 0.2, 1)` | Hover states, color changes, opacity |
| `transition-base` | `200ms cubic-bezier(0.4, 0, 0.2, 1)` | Button hovers, card lifts, focus rings |
| `transition-enter` | `250ms cubic-bezier(0, 0, 0.2, 1)` | Elements appearing (dropdown open, modal enter, fade-in) |
| `transition-exit` | `200ms cubic-bezier(0.4, 0, 1, 1)` | Elements leaving (dropdown close, toast dismiss) |
| `transition-slow` | `300ms cubic-bezier(0.4, 0, 0.2, 1)` | On-screen transitions (accordion expand, tab switch) |
| `transition-spring` | `300ms cubic-bezier(0.34, 1.56, 0.64, 1)` | Rare — toggle switches, playful micro-interactions only |

### Default by Interaction
- **Hover states** (color, shadow): `transition-fast`
- **Card hover lift**: `transition-base`
- **Focus rings**: `transition-fast`
- **Dropdown/accordion open**: `transition-enter`
- **Dropdown/accordion close**: `transition-exit`
- **Modal enter**: `transition-enter`
- **Modal exit**: `transition-exit`
- **Tab switching**: `transition-slow`
- **Page transitions**: None (Astro handles with view transitions if desired)

### Reduced Motion

```css
@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

Users who prefer reduced motion get instant state changes. No opt-out needed.

---

## Color Usage: Primary vs Accent

| | Primary (Azure Blue) | Accent (Strong Cyan) |
|---|---|---|
| **Base** | `#0779E5` | `#36D1DC` |
| **Role** | Action & authority | Highlight & energy |
| **Use for** | Primary CTAs, links, focus rings, active states, nav indicators | Secondary CTAs, decorative highlights, gradient endpoint, hover accents, tags/badges |
| **Buttons** | Solid primary button (`bg-primary-500 text-white`) | Outline or ghost secondary button (`border-accent-500 text-accent-600`) |
| **Text** | Links, branded text (`text-brand`) | Not used for body text — decorative only |
| **Gradient** | Starts the brand gradient | Ends the brand gradient |
| **Dark mode** | `primary-400` (#5DAFF7) | `accent-400` (#6FDFE7) |
| **Frequency** | 80% of colored elements | 20% of colored elements |

### Gradient Usage Guide

| Gradient | When to Use |
|----------|-------------|
| `--gradient-brand` | Hero headline text (`background-clip: text`), logo overlays, featured section accents |
| `--gradient-subtle` | Light section background washes (very subtle, 15% opacity) |
| `--gradient-surface` | Hero/section background fills (light mode only, neutral tones) |
| `--gradient-brand-reverse` | Decorative variety — use sparingly for visual interest on secondary elements |

---

## Touch Targets

Minimum interactive area: **44 x 44px** (WCAG 2.5.5).

| Element | Minimum Height | How to Achieve |
|---------|---------------|----------------|
| **Text buttons** | `44px` | `py-3` (12px top + 12px bottom) + `text-base` (16px) + border = 44px |
| **Icon-only buttons** | `44 x 44px` | 24px icon + `p-2.5` (10px padding each side) = 44px |
| **Nav links** | `44px` tap target | Padding expands hit area even if text is smaller |
| **Form inputs** | `44px` | `py-3` + `text-base` + border |

---

## Component States

### Buttons

**Primary** (solid):
| State | Background | Text | Shadow | Other |
|-------|-----------|------|--------|-------|
| Default | `primary-500` | `white` | `shadow-xs` | |
| Hover | `primary-600` | `white` | `shadow-brand` | |
| Active | `primary-700` | `white` | none | scale 0.98 |
| Focus | `primary-500` | `white` | `shadow-xs` | 2px `primary-300` ring, 2px offset |
| Disabled | `neutral-200` | `neutral-400` | none | `cursor-not-allowed`, 60% opacity |

**Secondary** (outline):
| State | Background | Border | Text |
|-------|-----------|--------|------|
| Default | transparent | 1.5px `primary-500` | `primary-500` |
| Hover | `primary-50` | 1.5px `primary-600` | `primary-600` |
| Active | `primary-100` | 1.5px `primary-700` | `primary-700` |
| Focus | transparent | 1.5px `primary-500` | `primary-500` + 2px ring |
| Disabled | transparent | 1.5px `neutral-300` | `neutral-400` |

**Tertiary** (ghost/link-style):
| State | Background | Text | Other |
|-------|-----------|------|-------|
| Default | transparent | `primary-500` | underline optional |
| Hover | `primary-50` | `primary-600` | |
| Active | `primary-100` | `primary-700` | |

**Button Sizes**:
| Size | Height | Padding | Font |
|------|--------|---------|------|
| `sm` | `36px` | `py-2 px-4` | `text-sm` (14px) |
| `md` | `44px` | `py-3 px-6` | `text-base` (16px) |
| `lg` | `52px` | `py-3.5 px-8` | `text-lg` (18px) |

### Form Inputs

| State | Border | Background | Other |
|-------|--------|-----------|-------|
| Default | 1px `neutral-300` | `white` | |
| Hover | 1px `neutral-400` | `white` | |
| Focus | 1.5px `primary-500` | `white` | `shadow-sm` |
| Error | 1.5px `error-500` | `error-50` | Error message in `error-600` below |
| Disabled | 1px `neutral-200` | `neutral-100` | `cursor-not-allowed`, muted text |

Dark mode inputs: border `rgba(255,255,255,0.1)`, background `neutral-900`, focus border `primary-400`.

Input height: `44px` (`py-3` + `text-base` + border).
Label: Above input, `text-sm`, `text-secondary`, `mb-1.5`.

### Links

| State | Color | Other |
|-------|-------|-------|
| Default | `primary-500` | Underline on hover (not at rest) |
| Hover | `primary-600` | Underline |
| Active | `primary-700` | |
| Visited | `primary-500` | No color change (keeps brand consistency) |

### Focus Rings

Global standard for all interactive elements:

```css
/* Light mode */
outline: 2px solid var(--color-primary-500);
outline-offset: 2px;

/* Dark mode */
outline: 2px solid var(--color-primary-400);
outline-offset: 2px;
```

Transition: `transition-fast` on outline.

---

## Layout Grid

| Breakpoint | Columns | Gutter | Side Padding |
|------------|---------|--------|-------------|
| `< 640px` | 4 | `16px` (space-4) | `16px` (space-4) |
| `640–767px` | 4 | `24px` (space-6) | `24px` (space-6) |
| `768–1023px` | 8 | `24px` (space-6) | `32px` (space-8) |
| `1024–1279px` | 12 | `24px` (space-6) | `32px` (space-8) |
| `>= 1280px` | 12 | `32px` (space-8) | Auto (centered) |

### Container
- Max width: `1280px` (`max-w-7xl`)
- Centered with auto margins
- Side padding included at each breakpoint above

### Section Vertical Padding
- Desktop (1024px+): `space-20` (80px) top and bottom
- Tablet (768px): `space-16` (64px)
- Mobile (<768px): `space-12` (48px)

### Content Width Limits
- **Full-bleed**: Hero, partner logos, footer — edge to edge
- **Container**: Most content — max `1280px`
- **Narrow**: Text-heavy blocks (about, long-form) — max `768px` (`max-w-3xl`)

---

## Breakpoints

Standard Tailwind defaults — no custom breakpoints needed.

| Token | Value | Usage |
|-------|-------|-------|
| `sm` | `640px` | Large phones |
| `md` | `768px` | Tablets |
| `lg` | `1024px` | Small laptops |
| `xl` | `1280px` | Desktops |
| `2xl` | `1536px` | Large screens |

---

## Z-Index Scale

| Token | Value | Usage |
|-------|-------|-------|
| `z-base` | `0` | Default |
| `z-raised` | `10` | Cards on hover, sticky elements |
| `z-dropdown` | `20` | Dropdowns, popovers |
| `z-sticky` | `30` | Sticky nav header |
| `z-overlay` | `40` | Modal backdrop |
| `z-modal` | `50` | Modal content |
| `z-toast` | `60` | Toast notifications |

---

## Iconography

**Approach**: Line icons, consistent stroke weight, matching the clean/minimal visual direction.

**Recommended Library**: [Lucide](https://lucide.dev)
- Open source (ISC license)
- 1400+ icons, actively maintained
- Consistent 24px grid, 2px stroke
- Tree-shakable — only ship icons we use
- Works with Astro (SVG imports or `astro-icon` integration)
- Same icon set used by shadcn/ui, so familiar to the ecosystem

**Style Rules**:
- Default size: `24px` (can scale to 20px for small, 32px for large)
- Stroke width: `2px` at 24px size (scale proportionally)
- Color: Inherit from parent text color (no fixed icon colors)
- No filled icons — line style only for consistency
- No multi-color icons

**Usage by Context**:
| Context | Size | Example |
|---------|------|---------|
| Inline with text | `16–20px` | Arrow in links, checkmarks in lists |
| Card/feature icons | `24px` | Service cards, process steps |
| Hero/section accents | `32–40px` | Large feature highlights |
| Navigation | `20–24px` | Mobile menu, theme toggle |
