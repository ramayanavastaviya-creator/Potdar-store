---
name: Potdar Digital
colors:
  surface: '#fbf8ff'
  surface-dim: '#d9d9e7'
  surface-bright: '#fbf8ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f3f2ff'
  surface-container: '#ededfb'
  surface-container-high: '#e7e7f5'
  surface-container-highest: '#e1e1ef'
  on-surface: '#191b25'
  on-surface-variant: '#434656'
  inverse-surface: '#2e303a'
  inverse-on-surface: '#f0effe'
  outline: '#737688'
  outline-variant: '#c3c5d9'
  surface-tint: '#004ced'
  primary: '#003ec7'
  on-primary: '#ffffff'
  primary-container: '#0052ff'
  on-primary-container: '#dfe3ff'
  inverse-primary: '#b7c4ff'
  secondary: '#5f5e5e'
  on-secondary: '#ffffff'
  secondary-container: '#e5e2e1'
  on-secondary-container: '#656464'
  tertiary: '#4d4d56'
  on-tertiary: '#ffffff'
  tertiary-container: '#65656e'
  on-tertiary-container: '#e5e3ee'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dde1ff'
  primary-fixed-dim: '#b7c4ff'
  on-primary-fixed: '#001452'
  on-primary-fixed-variant: '#0038b6'
  secondary-fixed: '#e5e2e1'
  secondary-fixed-dim: '#c8c6c5'
  on-secondary-fixed: '#1c1b1b'
  on-secondary-fixed-variant: '#474646'
  tertiary-fixed: '#e3e1ec'
  tertiary-fixed-dim: '#c6c5cf'
  on-tertiary-fixed: '#1a1b22'
  on-tertiary-fixed-variant: '#46464e'
  background: '#fbf8ff'
  on-background: '#191b25'
  surface-variant: '#e1e1ef'
  potdar-blue: '#0052FF'
  loyalty-near-black: '#1A1B22'
  loyalty-muted: '#E8E7F1'
  surface-border: '#E4E4E7'
  surface-border-dark: '#27272A'
typography:
  display-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-lg-mobile:
    fontFamily: Plus Jakarta Sans
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  headline-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 28px
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '500'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.05em
  loyalty-balance:
    fontFamily: Plus Jakarta Sans
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 32px
    letterSpacing: -0.02em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit-xs: 4px
  unit-sm: 8px
  unit-md: 16px
  unit-lg: 24px
  unit-xl: 48px
  gutter: 24px
  margin-desktop: 64px
  margin-mobile: 20px
---

## Brand & Style

The design system is centered on a **Modern Minimalist** aesthetic, tailored for a premium grocery experience. It prioritizes clarity, efficiency, and a "utility-luxe" atmosphere that differentiates the product from high-clutter competitors. 

The brand personality is authoritative and sophisticated. Visual weight is managed through generous whitespace and a strict monochromatic foundation, allowing the user's focus to remain on product quality. The loyalty and rewards layer is integrated as a seamless extension of the utility, avoiding "gamified" or promotional aesthetics (no gold, purple, or gradients). Instead, rewards are treated as a premium financial asset, using subtle states and professional tones to evoke trust and exclusivity.

## Colors

The palette is strictly functional and avoids decorative flourishes. The primary **Potdar Blue (#0052FF)** is the surgical driver for conversion and interaction.

**Loyalty Palette**
To maintain a professional tone, loyalty elements use a refined grayscale hierarchy:
- **Balance Displays:** Use `loyalty-near-black` for text on light surfaces to ensure high legibility and a premium feel.
- **Empty/Muted States:** Use `loyalty-muted` for inactive progress bars or secondary reward information.
- **Contrast:** High-value rewards or "Elite" tiers are signaled through the use of pure black and white layouts rather than metallic colors.

**Color Mode: Light (Default)**
- **Background:** #FFFFFF
- **Surface:** #FFFFFF with 1px `surface-border` strokes.
- **Text:** #111111 (Primary), #71717A (Secondary).

## Typography

The system utilizes **Plus Jakarta Sans** for headlines and brand-heavy moments like loyalty balances. This provides a modern, geometric character that feels welcoming yet structured. **Inter** is the workhorse font for all body copy, metadata, and UI labels, chosen for its exceptional legibility at small scale.

**Loyalty Specifics:**
- Point balances and currency rewards use `loyalty-balance` to differentiate numerical data from standard body text.
- Reward descriptions use `body-md` for clarity.
- Tier status (e.g., "Silver Member") uses `label-sm` in all-caps with the specified 0.05em letter spacing to denote a "badge" feel without needing heavy graphic containers.

## Layout & Spacing

This design system uses a **12-column fluid grid** for desktop and a **4-column grid** for mobile. The spacing rhythm is based on an 8px scale.

- **Grid Logic:** Use `unit-xl` (48px) as the standard vertical rhythm between major page sections or reward categories to maintain an airy, premium feel. 
- **Loyalty Modules:** Reward "cards" or point trackers should span 4 columns on desktop (3 across) or 2 columns on mobile. 
- **Reflow:** On mobile, margins reduce to 20px with 16px gutters to maximize screen real estate for product imagery and point tracking bars.

## Elevation & Depth

Hierarchy is established through **Tonal Layering and Outlines** rather than traditional drop shadows.

- **Strokes:** The primary method of separation. All containers, including loyalty cards and reward vouchers, use a 1px solid border (`#E4E4E7`).
- **Interactive Depth:** When a reward is hovered or an item is selected, the border color transitions to Potdar Blue.
- **Elevated Surfaces:** Dropdowns and floating reward notifications use a pure white surface with a 2px border or a very soft, high-diffusion ambient shadow (5% opacity) to provide a subtle "lift" without appearing heavy or skeuomorphic.

## Shapes

The shape language is architectural and controlled. 
- **Standard UI:** Buttons, input fields, and loyalty cards use `rounded-lg` (16px) to soften the professional tone.
- **Small Elements:** Checkboxes, radio buttons, and category chips use `rounded` (8px).
- **Large Layouts:** Banners and point-summary containers use `rounded-xl` (24px).
- **Pill-shapes:** These are strictly avoided for buttons but may be used for "Status Chips" (e.g., "Active Reward") to provide a distinct visual silhouette from the rectangular action buttons.

## Components

### Loyalty & Reward Cards
Reward cards utilize the standard 1px border. The point value is displayed in `loyalty-balance` style at the top-left. Descriptions are bottom-aligned in `body-md`. The background remains white to signal utility rather than promotion.

### Progress Bars
Used for tier tracking. The track uses `loyalty-muted` (#E8E7F1) and the fill uses Potdar Blue (#0052FF). The height is fixed at 8px with `rounded-full` corners.

### Buttons
- **Primary:** Potdar Blue background, white text. No shadow. Used for "Redeem" or "Claim."
- **Secondary:** White background, 1px border, #111111 text. Used for "View History."
- **Disabled:** `loyalty-muted` background with gray text for rewards not yet earned.

### Input Fields
Forms for promo codes or loyalty ID entry use a 1px border with 16px horizontal padding. Focus states transition the border to 2px Potdar Blue.

### Status Chips
Small tags (e.g., "Expiring Soon") use a subtle gray background (#F4F4F5) with `label-sm` text. They do not have borders, keeping them visually secondary to the main reward content.