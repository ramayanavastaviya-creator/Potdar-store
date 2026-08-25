# Potdar Store - Production Security & Hardening Specification

## 1. Zero-Trust Architecture
- **Browser is Untrusted**: Every value originating from the frontend (price, stock, discount, customerId) is treated as potentially malicious user-controlled input.
- **Server-Side Truth**: The backend is the sole authority for financial calculations, inventory state, and authorization.

## 2. Authorization & Access Control
- **Object-Level Authorization (BOLA)**: Every request verifies that the authenticated `userId` owns the requested resource (Order, Address, Wishlist).
- **Admin RBAC**: Strict role-based access control enforced at the API middleware level. Frontend visibility does not equate to permission.
- **Session Governance**: HttpOnly, Secure, and SameSite cookies. Session revocation occurs immediately upon admin account deactivation.

## 3. Transactional Integrity & Concurrency
- **Inventory Locks**: Database-level pessimistic locking or atomic increments prevent over-selling during race conditions.
- **Financial Exactness**: Use of Decimal/Numeric types for all currency. Floating-point arithmetic is strictly forbidden for money.
- **Idempotency**: `X-Idempotency-Key` implementation for Checkout, Payments, and Refunds to prevent duplicate records from network retries or double-clicks.

## 4. Payment & Refund Security
- **Server-to-Server Verification**: Payment status is verified directly with the provider API using secure webhooks and signatures.
- **Refund Constraints**: Logic-gate prevents refunds exceeding the original captured amount. Every refund requires explicit `refund.manage` permission and creates an immutable audit log.

## 5. Input & File Security
- **Schema Validation**: Zod/Joi validation on all API inputs (Strings, Numbers, Enums, Dates).
- **File Hardening**: Magic-byte validation for all uploads (Logos, Reviews). Files are stored in secure buckets with restricted public access and no execution permissions.

## 6. Audit & Traceability
- **Append-Only Ledger**: The Audit Log system is immutable. No user, regardless of role, can modify historical audit records.
- **Request Correlation**: Traceable request IDs link API calls to resulting Order, Payment, and Inventory movement events.

## 7. Error Handling & Logging
- **Safe Failures**: Internal stack traces, SQL errors, and file paths are never exposed to the client. Concise, production-safe error codes are returned.
- **Sensitive Data Masking**: Passwords, CVVs, and secrets are automatically filtered from all system logs.
