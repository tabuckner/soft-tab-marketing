# Soft-TAB Color System

> **Status**: Approved
> **Last Updated**: 2026-02-10
> **Based on**: Logo colors Azure Blue (#0779E5) + Strong Cyan (#36D1DC)

---

## Brand Foundation

**Primary**: Azure Blue `#0779E5`
**Secondary**: Strong Cyan `#36D1DC`
**Brand Gradient**: `linear-gradient(135deg, #0779E5, #36D1DC)`

---

## Primary Palette (Azure Blue)

| Token | Hex | Usage |
|-------|-----|-------|
| `primary-50` | `#EBF5FE` | Hover states on light backgrounds, badges |
| `primary-100` | `#D6EBFD` | Light backgrounds, subtle highlights |
| `primary-200` | `#AED7FB` | Disabled states |
| `primary-300` | `#85C3F9` | Borders with color |
| `primary-400` | `#5DAFF7` | Lighter interactive elements |
| `primary-500` | `#0779E5` | **Main buttons, links, key CTAs** |
| `primary-600` | `#0661B7` | Hover state for primary |
| `primary-700` | `#044989` | Active states, darker accents |
| `primary-800` | `#03315B` | Dark accent text |
| `primary-900` | `#02192E` | Darkest shade |
| `primary-950` | `#010C17` | Near-black with blue tint |

## Secondary/Accent Palette (Strong Cyan)

| Token | Hex | Usage |
|-------|-----|-------|
| `accent-50` | `#EDFBFC` | Subtle accent backgrounds |
| `accent-100` | `#DBF7F9` | Light accent state |
| `accent-200` | `#B7EFF3` | Hover states |
| `accent-300` | `#93E7ED` | Borders, lighter elements |
| `accent-400` | `#6FDFE7` | Medium accents |
| `accent-500` | `#36D1DC` | **Accent CTAs, highlights** |
| `accent-600` | `#2BA7B0` | Hover state for accent |
| `accent-700` | `#207D84` | Active states |
| `accent-800` | `#165358` | Dark accent |
| `accent-900` | `#0B2A2C` | Darkest shade |
| `accent-950` | `#051516` | Near-black with cyan tint |

## Neutral Palette (Blue-Tinted)

Cool-toned neutrals that harmonize with the brand (not pure gray):

| Token | Hex | Usage |
|-------|-----|-------|
| `neutral-50` | `#F8FAFB` | Page background, card surfaces |
| `neutral-100` | `#F1F5F7` | Subtle backgrounds, hover states |
| `neutral-200` | `#E4EAF0` | Borders, dividers |
| `neutral-300` | `#CFD8E3` | Medium borders |
| `neutral-400` | `#A3B4C7` | Placeholder text, low-emphasis icons |
| `neutral-500` | `#6B7F96` | Secondary text |
| `neutral-600` | `#506176` | Body text |
| `neutral-700` | `#3C4D5E` | Primary text, headings |
| `neutral-800` | `#2A3745` | High-contrast text |
| `neutral-900` | `#1A232E` | Darkest text, emphasis |
| `neutral-950` | `#0F1419` | Near-black |

## Semantic Colors

| Token | Hex | Usage |
|-------|-----|-------|
| `success-50` | `#EEFBF4` | Success background |
| `success-500` | `#10B981` | Success states |
| `success-700` | `#047857` | Active success |
| `warning-50` | `#FFFBEB` | Warning background |
| `warning-500` | `#F59E0B` | Warning states |
| `warning-700` | `#B45309` | Active warning |
| `error-50` | `#FEF2F2` | Error background |
| `error-500` | `#EF4444` | Error states |
| `error-700` | `#B91C1C` | Active error |

## Surface Colors (Light Mode)

| Token | Value | Usage |
|-------|-------|-------|
| `surface-page` | `#FAFBFC` | Main page background |
| `surface-card` | `#FFFFFF` | Card backgrounds |
| `surface-elevated` | `#FFFFFF` | Modals, popovers (+ shadow) |
| `surface-overlay` | `rgba(26, 35, 46, 0.65)` | Modal overlays |
| `surface-subtle` | `#F1F5F7` | Table headers, subtle backgrounds |

## Text Colors (Light Mode)

| Token | Value | Contrast on White | Usage |
|-------|-------|-------------------|-------|
| `text-primary` | `#2A3745` | ~11.8:1 AAA | Body text |
| `text-secondary` | `#506176` | ~7.8:1 AAA | Descriptions |
| `text-tertiary` | `#6B7F96` | ~4.6:1 AA | Captions, metadata |
| `text-muted` | `#A3B4C7` | ~3.2:1 (large only) | Placeholder, disabled |
| `text-inverse` | `#FFFFFF` | — | On dark/colored backgrounds |
| `text-brand` | `#0779E5` | ~4.8:1 AA | Links, branded text |

## Gradients

```css
/* Primary brand gradient */
--gradient-brand: linear-gradient(135deg, #0779E5 0%, #36D1DC 100%);

/* Subtle (for light backgrounds) */
--gradient-subtle: linear-gradient(135deg, rgba(7,121,229,0.15) 0%, rgba(54,209,220,0.15) 100%);

/* Hero/section background */
--gradient-surface: linear-gradient(180deg, #F8FAFB 0%, #EBF5FE 100%);

/* Reverse (for variety) */
--gradient-brand-reverse: linear-gradient(135deg, #36D1DC 0%, #0779E5 100%);
```

## Dark Mode ✅ COMMITTED

Dark mode ships with V1. Built inline with each component using Tailwind `dark:` variants.

### Strategy
- **Default**: Respect `prefers-color-scheme` on first visit
- **Override**: Sun/moon toggle in nav, preference stored in `localStorage`
- **Elevation**: Lighter = more elevated in dark mode (opposite of light mode shadows)
- **Saturation**: Use 300-400 range of primary/accent instead of 500-600 (less harsh)
- **Borders**: `rgba(255, 255, 255, 0.1)` instead of neutral-200

### Surface Colors (Dark Mode)

| Token | Light Mode | Dark Mode |
|-------|------------|-----------|
| `surface-page` | `#FAFBFC` | `#0F1419` (neutral-950) |
| `surface-card` | `#FFFFFF` | `#1A232E` (neutral-900) |
| `surface-elevated` | `#FFFFFF` | `#2A3745` (neutral-800) |
| `surface-subtle` | `#F1F5F7` | `#1A232E` (neutral-900) |
| `surface-hover` | `#E4EAF0` | `#2A3745` (neutral-800) |
| `surface-overlay` | `rgba(26,35,46,0.65)` | `rgba(0,0,0,0.7)` |

### Text Colors (Dark Mode)

| Token | Light Mode | Dark Mode | Contrast on neutral-900 |
|-------|------------|-----------|------------------------|
| `text-primary` | `#2A3745` | `#F1F5F7` (neutral-100) | ~13.2:1 AAA |
| `text-secondary` | `#506176` | `#CFD8E3` (neutral-300) | ~8.1:1 AAA |
| `text-tertiary` | `#6B7F96` | `#A3B4C7` (neutral-400) | ~5.2:1 AA |
| `text-muted` | `#A3B4C7` | `#6B7F96` (neutral-500) | ~3.1:1 (large only) |
| `text-brand` | `#0779E5` | `#5DAFF7` (primary-400) | ~6.8:1 AA |

### Brand Gradient (Dark Mode)

```css
/* Lighter, less saturated for dark backgrounds */
--gradient-brand-dark: linear-gradient(135deg, #5DAFF7 0%, #6FDFE7 100%);

/* Subtle glow effect */
--gradient-surface-dark: linear-gradient(180deg, #0F1419 0%, #1A232E 100%);
```

### Implementation Pattern

```css
:root {
  --color-surface-page: #FAFBFC;
  --color-text-primary: #2A3745;
  --gradient-brand: linear-gradient(135deg, #0779E5, #36D1DC);
}

@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --color-surface-page: #0F1419;
    --color-text-primary: #F1F5F7;
    --gradient-brand: linear-gradient(135deg, #5DAFF7, #6FDFE7);
  }
}

[data-theme="dark"] {
  --color-surface-page: #0F1419;
  --color-text-primary: #F1F5F7;
  --gradient-brand: linear-gradient(135deg, #5DAFF7, #6FDFE7);
}
```

This approach:
1. Defaults to OS preference (`prefers-color-scheme`)
2. `data-theme="dark"` on `<html>` overrides when user manually toggles
3. `data-theme="light"` overrides dark OS preference when user manually selects light
4. No theme attribute = follow OS preference
