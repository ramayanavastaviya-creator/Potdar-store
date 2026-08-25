# Potdar Store - Design Audit & Production QA

## Visual Consistency Checklist

### 1. Typography
- **Primary Font**: Plus Jakarta Sans (Variable)
- **Scale**: Minor Third (1.200)
- **Hierarchy**:
  - Display: Black/Bold, tracking -1%
  - Headings: Bold/Medium
  - Body: Regular, 1.5 line-height for readability.

### 2. Color Palette (Tokens)
- **Primary**: `#0052FF` (Electric Blue) - Actions, selection, progress.
- **Surface (Light)**: `#FBF8FF` (Background), `#FFFFFF` (Card)
- **Surface (Dark)**: `#121212` (Background), `#1E1E1E` (Card)
- **Text**: `#0D0D0D` (High emphasis), `#666666` (Medium emphasis)

### 3. Layout & Components
- **Spacing**: 8px (unit) grid system. Gutter: 24px (Desktop), 16px (Mobile).
- **Radius**: `rounded-lg` (8px) for containers; `rounded-full` for pills/buttons where appropriate.
- **Button Sizing**: 48px height for primary mobile actions; 40px for desktop secondary.

### 4. Interactive States
- **Loading**: Skeleton loaders matching component wireframes.
- **Add to Cart**: Transitions from "Add" button to `[-] 1 [+]` quantity control in-situ.
- **Feedback**: Soft toasts for success (e.g., "Item added to cart") and clear red alerts for errors.

## Responsive Targets
- **Mobile Small**: 320px (iPhone SE) - Ensure no overlapping text.
- **Mobile Standard**: 390px-412px (iPhone/Pixel) - Optimized touch targets.
- **Tablet**: 768px (iPad) - Transition from 2-column to 3-column grids.
- **Desktop**: 1280px+ - Max container width 1440px.
