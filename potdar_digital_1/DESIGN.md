---
name: Potdar Digital
colors:
  surface: '#fbf8ff'
  surface-dim: '#dad9e3'
  surface-bright: '#fbf8ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f4f2fd'
  surface-container: '#eeedf7'
  surface-container-high: '#e8e7f1'
  surface-container-highest: '#e3e1ec'
  on-surface: '#1a1b22'
  on-surface-variant: '#434656'
  inverse-surface: '#2f3038'
  inverse-on-surface: '#f1effa'
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
  tertiary: '#4c4e4f'
  on-tertiary: '#ffffff'
  tertiary-container: '#656666'
  on-tertiary-container: '#e4e5e5'
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
  tertiary-fixed: '#e2e2e2'
  tertiary-fixed-dim: '#c6c6c7'
  on-tertiary-fixed: '#1a1c1c'
  on-tertiary-fixed-variant: '#454747'
  background: '#fbf8ff'
  on-background: '#1a1b22'
  surface-variant: '#e3e1ec'
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
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  container-max: 1280px
  gutter: 24px
  margin-desktop: 64px
  margin-mobile: 20px
  unit-xs: 4px
  unit-sm: 8px
  unit-md: 16px
  unit-lg: 24px
  unit-xl: 48px
---

## Brand & Style

This design system is built for a premium grocery e-commerce experience that prioritizes clarity, efficiency, and a high-end retail feel. The aesthetic leans heavily into **Modern Minimalism** with a focus on structured layouts and a "utility-luxe" atmosphere.

The brand personality is authoritative yet accessible, positioning the local store as a sophisticated digital destination. The visual language avoids the clutter typical of grocery apps, opting instead for generous whitespace and a strict monochromatic foundation. A single, high-energy accent color is used surgically to guide the user toward conversion points without breaking the refined composure of the interface.

## Colors

The palette is strictly functional. The primary **Electric Blue (#0052FF)** is reserved exclusively for interactive elements like primary buttons, active states, and cart notifications. 

**Light Mode (Default):**
- **Background:** #FFFFFF (Pure White)
- **Surface:** #FFFFFF with 1px #E4E4E7 (Zinc-200) borders.
- **Primary Text:** #111111 (Near-Black)
- **Secondary Text:** #71717A (Muted Gray)

**Dark Mode:**
- **Background:** #09090B (Zinc-950)
- **Surface:** #18181B (Zinc-900) with 1px #27272A (Zinc-800) borders.
- **Primary Text:** #FAFAFA
- **Secondary Text:** #A1A1AA

Avoid using gradients or drop shadows to define depth; use the 1px border system to delineate surfaces.

## Typography

The system utilizes **Plus Jakarta Sans** for headlines to provide a modern, slightly geometric character that feels welcoming. **Inter** is used for body copy and labels to ensure maximum legibility at small sizes, particularly for product descriptions and pricing.

Use a strict hierarchy: product names should always use `headline-md`, while prices use `body-lg` with a semi-bold weight. `label-sm` is intended for metadata such as weight (e.g., "500g") or category tags.

## Layout & Spacing

The layout follows a **12-column fluid grid** for desktop and a **4-column grid** for mobile. 

- **Desktop:** 64px outer margins, 24px gutters. Product grids should typically span 3 columns (4 items per row) or 4 columns (3 items per row) for premium featured items.
- **Mobile:** 20px outer margins, 16px gutters. Product grids use a 2-column layout.

Spacing follows an 8px base unit. Use `unit-xl` (48px) to separate major sections like "Fresh Vegetables" and "Bakery" to maintain the premium, airy feel.

## Elevation & Depth

This design system rejects traditional shadows in favor of **Tonal Layering and Outlines**.

Depth is communicated through:
1.  **Stroke:** All cards and containers use a 1px solid border (#E4E4E7 in light, #27272A in dark).
2.  **Surface Contrast:** Modals and dropdowns use a slightly elevated surface color (White in light mode) but are primarily distinguished by a thicker 2px border or a very soft, high-diffusion "ambient" shadow (0px 4px 20px rgba(0,0,0,0.05)) to prevent them from feeling "flat" against the background.
3.  **Active State:** When an item is hovered or selected, the border color shifts to the Primary Electric Blue.

## Shapes

The shape language is controlled and architectural. 
- **Small Components:** Checkboxes and small tags use `rounded` (8px).
- **Standard Components:** Buttons, input fields, and product cards use `rounded-lg` (16px) to soften the professional tone.
- **Large Components:** Promotional banners or bottom sheets use `rounded-xl` (24px) on relevant corners.

Avoid using pill-shapes for buttons; the `rounded-lg` provides a more structured, premium look suitable for high-end retail.

## Components

### Buttons
- **Primary:** Solid #0052FF background, White text. High-contrast, no shadow.
- **Secondary:** White background, 1px #E4E4E7 border, #111111 text.
- **Ghost:** Transparent background, #111111 text, used for "See All" or secondary actions.

### Product Cards
Cards are the heart of the experience. They feature a 1:1 (square) aspect ratio for the product image on a light gray (#F4F4F5) background. Product info is left-aligned below the image. The "Add to Cart" action is a primary-style button that only appears on hover for desktop, or remains a fixed icon-button for mobile.

### Inputs & Form Fields
Fields use a 1px border and 16px horizontal padding. The label sits above the field in `label-md` style. Focus states must use a 2px #0052FF border.

### Chips & Tags
Used for categories (e.g., "Organic", "Vegan"). Use a subtle #F4F4F5 background with #71717A text. No borders.

### Cart Drawer
A right-aligned slide-out panel that uses the full height of the viewport. It maintains the white surface and uses a "Sticky Bottom" section for the checkout total and primary call-to-action button.