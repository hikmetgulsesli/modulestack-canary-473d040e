---
name: ModuleStack Canary
colors:
  surface: '#16130a'
  surface-dim: '#16130a'
  surface-bright: '#3c392e'
  surface-container-lowest: '#100e06'
  surface-container-low: '#1e1c12'
  surface-container: '#222016'
  surface-container-high: '#2d2a1f'
  surface-container-highest: '#38352a'
  on-surface: '#e9e2d2'
  on-surface-variant: '#cec6ad'
  inverse-surface: '#e9e2d2'
  inverse-on-surface: '#333026'
  outline: '#97917a'
  outline-variant: '#4b4734'
  surface-tint: '#e2c62d'
  primary: '#fffcff'
  on-primary: '#393000'
  primary-container: '#fde047'
  on-primary-container: '#726300'
  inverse-primary: '#6d5e00'
  secondary: '#b7c8e1'
  on-secondary: '#213145'
  secondary-container: '#3a4a5f'
  on-secondary-container: '#a9bad3'
  tertiary: '#f4ffff'
  on-tertiary: '#003739'
  tertiary-container: '#3bf7ff'
  on-tertiary-container: '#006e72'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#ffe24c'
  primary-fixed-dim: '#e2c62d'
  on-primary-fixed: '#211b00'
  on-primary-fixed-variant: '#524600'
  secondary-fixed: '#d3e4fe'
  secondary-fixed-dim: '#b7c8e1'
  on-secondary-fixed: '#0b1c30'
  on-secondary-fixed-variant: '#38485d'
  tertiary-fixed: '#59f8ff'
  tertiary-fixed-dim: '#00dce4'
  on-tertiary-fixed: '#002021'
  on-tertiary-fixed-variant: '#004f52'
  background: '#16130a'
  on-background: '#e9e2d2'
  surface-variant: '#38352a'
typography:
  display-sm:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.02em
  headline-sm:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: -0.01em
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
    letterSpacing: 0em
  body-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '400'
    lineHeight: 16px
    letterSpacing: 0em
  data-mono:
    fontFamily: JetBrains Mono
    fontSize: 13px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: -0.01em
  label-xs:
    fontFamily: JetBrains Mono
    fontSize: 11px
    fontWeight: '700'
    lineHeight: 12px
    letterSpacing: 0.05em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 4px
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  gutter: 12px
  margin: 16px
---

## Brand & Style

The design system is engineered for high-stakes operational environments where data density and clarity are paramount. The brand personality is **technical, deterministic, and utilitarian**, eschewing decorative flair in favor of functional precision. It is designed for engineers, system administrators, and operators who require a "single pane of glass" view into complex systems.

The visual style is **Corporate / Modern** with a lean toward **Technical Minimalism**. It utilizes a "Compact Browser App" aesthetic: maximizing screen real estate, using tight spacing scales, and ensuring every pixel serves a data-driven purpose. The emotional response should be one of confidence, stability, and immediate situational awareness.

## Colors

The palette is optimized for long-duration monitoring in low-light environments. 
- **Core Background:** A deep charcoal (#0F172A) provides the foundation, minimizing eye strain.
- **Accents:** 'Canary Yellow' (#FDE047) is used sparingly for primary actions and active states to ensure high visibility against the dark backdrop.
- **Semantic Logic:** Success, Error, and Warning colors follow standard industry conventions but are tuned for high chrominance to stand out in dense data tables.
- **Borders & Dividers:** Slate-gray (#334155) is used for structural definition, maintaining a crisp "grid" feel without creating visual noise.

## Typography

Typography is treated as a functional tool for information hierarchy. 
- **Inter** is the workhorse for the UI, chosen for its exceptional legibility at small sizes.
- **JetBrains Mono** is utilized for all technical data points, logs, IDs, and metrics to ensure characters are distinct (especially 0/O and 1/l/I).
- **Tracking:** Headlines use tight tracking (-0.01em to -0.02em) to maintain a compact feel, while monospaced labels use slightly increased tracking for readability at microscopic sizes.
- **Hierarchy:** Use font weight rather than size to differentiate information in high-density views.

## Layout & Spacing

This design system employs a **Fixed/Fluid Hybrid Grid** optimized for 1440p displays. 
- **Spacing Scale:** A strict 4px baseline grid ensures alignment.
- **Density:** We prioritize content over whitespace. Sidebars and headers are collapsed to the minimum functional width/height.
- **Breakpoints:**
  - **Desktop (1280px+):** 12-column grid, 12px gutters.
  - **Tablet (768px-1279px):** 8-column grid, 12px gutters.
  - **Mobile (Below 768px):** Single column stack, 16px margins.
- **Reflow:** On dashboard views, cards should use a CSS Grid `auto-fill` pattern to maximize the number of visible metrics without vertical scrolling.

## Elevation & Depth

Depth is conveyed through **Tonal Layering** rather than traditional shadows.
- **Level 0 (Background):** #0F172A - The lowest layer for the app canvas.
- **Level 1 (Cards/Panels):** #1E293B - Used for content containers.
- **Level 2 (Modals/Popovers):** #334155 - Elevated surfaces with a subtle 1px stroke in a lighter slate (#475569).
- **Interactivity:** Elements do not "lift" on hover; instead, they receive a subtle inner glow or a border color change to 'Canary Yellow' to indicate focus. 
- **Status Glows:** High-priority alerts may use a diffused outer glow (8px blur, 20% opacity) in the semantic color (Red or Yellow) to draw attention in the periphery.

## Shapes

The shape language is **Soft (0.25rem)** to maintain a balance between the precision of a technical tool and the modern feel of a web application. 
- Standard buttons and inputs use a 4px radius.
- Large containers and cards use a 4px or 8px radius.
- Status badges use a 2px radius for a "blocky" technical appearance.
- Avoid completely round (pill) shapes unless used for specialized toggle switches.

## Components

- **Data Tables:** Zebra-striping is avoided; use 1px borders (#334155). Rows should be compact (32px height). Column headers are `label-xs` with a subtle background tint.
- **Status Badges:** Compact, rectangular shapes. Use a "subtle glow" approach: a background tint at 10% opacity of the semantic color, with a solid 1px border and high-contrast text.
- **Metric Cards:** Should feature a `data-mono` primary value and a small sparkline. Sparklines should use the primary accent color.
- **Buttons:** 
  - *Primary:* Canary Yellow background with Slate-900 text.
  - *Secondary:* Ghost style with Slate-gray borders.
- **Form Fields:** Inputs use #1E293B background. Focus state is a 1px solid Canary Yellow border. Error states replace the border with Alert Red and include a trailing icon.
- **Terminal/Log Component:** Fixed-width container using JetBrains Mono, #020617 background, and no-wrap text for system output.