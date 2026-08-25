---
name: Potdar Precision
colors:
  surface: '#f7f9fb'
  surface-dim: '#d8dadc'
  surface-bright: '#f7f9fb'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f4f6'
  surface-container: '#eceef0'
  surface-container-high: '#e6e8ea'
  surface-container-highest: '#e0e3e5'
  on-surface: '#191c1e'
  on-surface-variant: '#434656'
  inverse-surface: '#2d3133'
  inverse-on-surface: '#eff1f3'
  outline: '#737688'
  outline-variant: '#c3c5d9'
  surface-tint: '#004ced'
  primary: '#003ec7'
  on-primary: '#ffffff'
  primary-container: '#0052ff'
  on-primary-container: '#dfe3ff'
  inverse-primary: '#b7c4ff'
  secondary: '#565e74'
  on-secondary: '#ffffff'
  secondary-container: '#dae2fd'
  on-secondary-container: '#5c647a'
  tertiary: '#3f4f65'
  on-tertiary: '#ffffff'
  tertiary-container: '#57677e'
  on-tertiary-container: '#d6e6ff'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dde1ff'
  primary-fixed-dim: '#b7c4ff'
  on-primary-fixed: '#001452'
  on-primary-fixed-variant: '#0038b6'
  secondary-fixed: '#dae2fd'
  secondary-fixed-dim: '#bec6e0'
  on-secondary-fixed: '#131b2e'
  on-secondary-fixed-variant: '#3f465c'
  tertiary-fixed: '#d3e4fe'
  tertiary-fixed-dim: '#b7c8e1'
  on-tertiary-fixed: '#0b1c30'
  on-tertiary-fixed-variant: '#38485d'
  background: '#f7f9fb'
  on-background: '#191c1e'
  surface-variant: '#e0e3e5'
typography:
  display-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 36px
    fontWeight: '700'
    lineHeight: 44px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 28px
    fontWeight: '700'
    lineHeight: 36px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 28px
  headline-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '600'
    lineHeight: 24px
  body-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  label-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 13px
    fontWeight: '600'
    lineHeight: 18px
    letterSpacing: 0.01em
  label-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 11px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.03em
  headline-lg-mobile:
    fontFamily: Plus Jakarta Sans
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 32px
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 8px
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  gutter: 20px
  margin: 24px
---

## Brand & Style

The design system is engineered for the **Potdar Store Admin**, a high-velocity purchase management environment. The brand personality is authoritative, precise, and operationally focused, prioritizing data density and clarity over decorative flair.

The design style follows a **Modern Corporate** aesthetic with a lean toward **Minimalism**. It utilizes a sophisticated grayscale foundation to allow functional color cues—like "Potdar Blue"—to stand out. The interface evokes a sense of reliability and institutional trust, ensuring that administrators can manage complex procurement workflows without visual fatigue. Key traits include expansive whitespace within data-heavy views, razor-sharp alignment, and subtle structural dividers.

## Colors

The palette is anchored by **Potdar Blue (#0052FF)**, used exclusively for primary actions, active states, and essential brand touchpoints. This high-energy blue is balanced by a deep Slate secondary color for text and iconography, ensuring high legibility and a premium feel.

- **Primary:** Potdar Blue (#0052FF) - The engine of the UI.
- **Secondary:** Slate 900 (#0F172A) - For primary headings and high-contrast text.
- **Neutral:** A refined range of cool grays. Backgrounds use Slate 50 (#F8FAFC) to differentiate from pure white (#FFFFFF) card surfaces.
- **Semantic:** Standard success (Green), warning (Amber), and error (Red) tones are desaturated slightly to maintain the sophisticated professional atmosphere.

## Typography

This design system exclusively uses **Plus Jakarta Sans** to provide a modern, geometric, and highly legible experience. 

- **Headlines:** Use Bold (700) or SemiBold (600) weights with slight negative letter-spacing for a compact, professional appearance in dashboard headers.
- **Body Text:** Set primarily in 14px (body-md) to maximize data density while maintaining readability.
- **Labels:** Small caps or bolded 11px/13px labels are used for table headers and form field captions to create clear hierarchy without occupying excessive vertical space.

## Layout & Spacing

The layout utilizes a **12-column fluid grid** for the main content area, with a fixed-width sidebar (240px) for navigation. 

- **Rhythm:** An 8px linear scale governs all spacing. Controls like buttons and inputs are strictly 40px (5x8) or 32px (4x8) in height.
- **Density:** High-density layouts are preferred for purchase tables. Use 8px (sm) for internal element padding and 16px (md) for container padding.
- **Breakpoints:** 
    - Desktop: 1280px+ (12 columns, 24px margins)
    - Tablet: 768px - 1279px (8 columns, 20px margins)
    - Mobile: Below 768px (4 columns, 16px margins, stacked forms)

## Elevation & Depth

Hierarchy is established through **Tonal Layers** and **Low-Contrast Outlines** rather than heavy shadows. 

- **Surface Levels:** The base background is Slate 50. Primary "work surfaces" (cards, tables, whiteboards) are Pure White (#FFFFFF).
- **Borders:** Use subtle 1px borders (#E2E8F0) to define elements. This "Ghost Border" technique keeps the UI feeling light despite high complexity.
- **Shadows:** When necessary (e.g., dropdowns or modals), use a single, highly-diffused "Ambient Shadow": `0 10px 15px -3px rgba(0, 0, 0, 0.05)`.
- **Interactive Depth:** On hover, primary cards can transition from a subtle border to a slightly more defined border color (Slate 300) rather than lifting off the page.

## Shapes

The shape language is consistently **Rounded**, reflecting a modern, accessible professional tool. 

- **Standard Elements:** Buttons, Input Fields, and Chips use a 0.5rem (8px) corner radius to match the 8px spacing rhythm.
- **Containers:** Large cards and modals use 1rem (16px) for a softer, more modern structural feel.
- **Consistency:** Avoid pill-shaped elements for primary actions to maintain the "Precision" brand narrative; keep the 8px radius standard across the dashboard.

## Components

- **Buttons:** Primary buttons are Solid Potdar Blue with White text. Secondary buttons are White with a Slate 200 border and Slate 900 text. Active/Pressed states should darken the blue by 10%.
- **Input Fields:** 40px height. 1px border (#E2E8F0). Focus state uses a 1px Potdar Blue border with a 3px soft blue outer glow (20% opacity).
- **Data Tables:** The core of the system. Use "Zebra Striping" with Slate 50 for alternate rows. Headers are 11px Bold (label-sm) in Slate 500.
- **Chips/Badges:** For status (e.g., "Pending", "Shipped"). Use soft tinted backgrounds (e.g., Blue 50 background with Blue 700 text) with 4px radius.
- **Cards:** White background, 1px Slate 200 border, no shadow for standard layout sections.
- **Purchase Controls:** Use "Step-style" progress indicators for procurement stages, using Potdar Blue for completed steps and Slate 200 for upcoming ones.