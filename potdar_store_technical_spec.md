# Potdar Store - Technical Specification & API Architecture

## 1. System Overview
Potdar Store is a premium grocery e-commerce platform built on a "Mobile-First, Content-Centric" architecture. The frontend is designed to interface with a Next.js / Node.js backend using TypeScript for end-to-end type safety.

## 2. Core Data Entities (Prisma/PostgreSQL Schema)

### Users & Auth
- **User**: Identity provider (Email/Mobile, Password Hash, Role: CUSTOMER | ADMIN).
- **CustomerProfile**: Extends User with loyalty points, preferences, and default settings.
- **AdminUser**: Staff-specific metadata and permission levels.
- **Address**: Polymorphic (User-owned). Fields: `street`, `landmark`, `city`, `pincode`, `isDefault`.

### Catalog
- **Category**: `name`, `slug`, `imageURL`, `displayOrder`.
- **Subcategory**: Parent-child relationship with Category.
- **Product**: `name`, `brand`, `description`, `slug`, `basePrice`, `mrp`, `discount%`, `isActive`.
- **ProductVariant**: `productId`, `weight/volume`, `priceMultiplier`, `sku`, `barcode`.
- **Inventory**: `variantId`, `currentStock`, `lowStockThreshold`.

### Sales & Operations
- **Cart / CartItem**: Server-side persisted for cross-device continuity.
- **Wishlist / WishlistItem**: Simple mapping of User to Product.
- **Order**: `userId`, `totalAmount`, `status`, `paymentId`, `deliveryAddressId`.
- **OrderItem**: Snapshot of product name and price at time of purchase.
- **Payment**: `orderId`, `transactionId`, `provider` (UPI|CARD|COD), `status`.
- **Delivery**: `orderId`, `type` (ASAP|SCHEDULED), `timeSlot`, `status`.

## 3. API Service Abstractions (Frontend Implementation)

The frontend should utilize a `Service` layer to abstract API calls:

```typescript
// Example Service Pattern
const ProductService = {
  getProductsByCategory: async (slug: string) => fetch(`/api/v1/products?category=${slug}`),
  getDetail: async (id: string) => fetch(`/api/v1/products/${id}`),
  search: async (query: string) => fetch(`/api/v1/search?q=${query}`)
};
```

## 4. Security & Logic Constraints

- **Pricing Authority**: The server is the SOLE authority for pricing. The frontend sends `variantId` and `quantity`; the backend returns the calculated `Subtotal`, `Tax`, `DeliveryFee`, and `FinalTotal`.
- **RBAC (Role-Based Access Control)**: Middleware must protect all `/admin` routes. Admin JWTs should contain scoped permissions.
- **Validation**: Zod or Joi schemas must validate all inputs on the server before database persistence.

## 5. Performance Optimization (Indian Market)

- **Images**: Use Next.js `<Image />` component for automatic WebP conversion and lazy loading.
- **State**: React Query or SWR for caching and optimistic UI updates (e.g., adding to cart).
- **Network**: Minimal JS bundles; prioritize server-side rendering (SSR) for SEO-sensitive pages (Homepage, Category).

## 6. SEO & Accessibility

- **Structured Data**: JSON-LD for Products and LocalBusiness on every page.
- **A11y**: Semantic HTML, ARIA labels for quantity controls, and 44px+ touch targets for mobile.
