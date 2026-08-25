# Potdar Store - SEO & Production Specification

## 1. SEO Architecture & Metadata
| Page Type | Title Pattern | Meta Description Strategy |
| :--- | :--- | :--- |
| **Homepage** | Potdar Store \| Daily groceries and essentials | Concise summary of premium local grocery service. |
| **Category** | {Category Name} \| Potdar Store | Dynamic generation based on category slug. |
| **Product** | {Product Name} - {Brand} \| Potdar Store | Includes price, availability, and high-quality image alt. |

## 2. Structured Data (JSON-LD)
Implementation of Schema.org vocabularies:
- **Organization/LocalBusiness**: Store address, contact, and hours.
- **Product & Offer**: Price, currency (INR), availability, and SKU.
- **BreadcrumbList**: Hierarchical navigation path for search crawlers.

## 3. Performance & Web Vitals
- **LCP Optimization**: Priority loading for hero images and Plus Jakarta Sans font weights (400, 500, 700).
- **CLS Prevention**: Explicit width/height attributes for all product images and skeleton loaders that match final UI dimensions.
- **Image Strategy**: WebP/AVIF formats with responsive srcset and lazy-loading for below-the-fold content.

## 4. Accessibility (A11y)
- **Interactive States**: Visible focus rings (2px Potdar Blue) for all keyboard-navigable elements.
- **Screen Readers**: Aria-labels for icon-only buttons (Cart, Search, Wishlist).
- **Touch Targets**: Minimum 44x44px for all mobile interactive elements.

## 5. Security & Indexing
- **Robots.txt**: Disallow `/admin`, `/account`, `/cart`, `/checkout`, and `/orders`.
- **Canonicalization**: Enforced single-source URLs to prevent duplicate content from filters/tracking params.
- **Security Headers**: Production-ready CSP, Referrer-Policy, and HSTS.