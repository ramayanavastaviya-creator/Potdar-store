# Potdar Store - Interaction & Component Behavior System

## 1. Button System (State Hierarchy)
| State | Primary (#0052FF) | Secondary (Outline) | Destructive (Red) |
| :--- | :--- | :--- | :--- |
| **Default** | Solid blue, white text | Transparent, gray-300 border | Solid red, white text |
| **Hover** | Background-lighten 10% | Surface-container-low, gray-900 border | Red-darken 10% |
| **Pressed** | Scale 0.98, opacity 0.9 | Scale 0.98, bg-surface-dim | Scale 0.98, opacity 0.9 |
| **Focus** | 2px ring-offset-2 ring-primary | 2px ring-offset-2 ring-outline | 2px ring-offset-2 ring-error |
| **Loading** | Label hidden, 20px spinner shown | Label hidden, 20px spinner shown | Label hidden, 20px spinner shown |
| **Disabled** | Grayscale, opacity 0.4, cursor-not-allowed | Grayscale, opacity 0.4, cursor-not-allowed | Grayscale, opacity 0.4, cursor-not-allowed |

## 2. Product Card States
- **Desktop Hover**: Subtle shadow elevation (shadow-md), slightly darker "Add" button.
- **Add to Cart Interaction**: On click, button width expands/shrinks to accommodate `[-] 1 [+]` quantity controls.
- **Out of Stock**: Image grayscale (60%), 0.5 opacity, badge "Out of Stock", button disabled with label "Unavailable".

## 3. Feedback & Messaging
- **Toasts**: Fixed bottom-center (Mobile) or bottom-right (Desktop). Slide-up entrance, 3s duration.
- **Empty States**: Centered illustration-icon (48px), Headline-sm, Body-md, and one Primary CTA.
- **Skeletons**: Shimmer effect (linear-gradient pulse) matching the layout of the final content (Cards, Lists, Filters).

## 4. Mobile Layouts
- **Bottom Sheets**: max-height 90vh, rounded-t-2xl, drag handle (32x4px), fixed action footer.
- **Search**: Full-screen overlay on focus with category pills and recent searches list.

## 5. Motion Guidelines
- **Durations**: Transitions: 150ms. Entrances: 300ms.
- **Easings**: `cubic-bezier(0.4, 0, 0.2, 1)` (Standard).
- **Constraints**: No bounce, no scale > 1.02, no continuous loops.