# Potdar Store - Data Integrity & Backend Architecture Specification

## 1. Authoritative Single Source of Truth (SSOT)
Every core business entity is managed by a dedicated service to prevent data duplication and synchronization errors.
- **Catalog**: `Product` and `Category` entities are the sole authority for names, slugs, and active states.
- **Inventory**: The `InventoryTransaction` ledger is the only source for `currentStock`. Aggregated counts in `Product` or `Dashboard` views are read-only caches.
- **Finance**: The `Order` and `Payment` services handle all currency calculations. The frontend is forbidden from submitting totals.
- **Loyalty**: The `LoyaltyLedger` records every point earned or redeemed; balances are derived from these immutable events.

## 2. Relational Integrity & Constraints
- **Foreign Key Enforcement**: Mandatory relationships (e.g., `Order` -> `Customer`, `PurchaseLine` -> `ProductVariant`) are enforced at the database level to prevent orphaned records.
- **Soft Delete/Archival**: Destructive `DELETE` operations are replaced with `isArchived` or `status` flags (e.g., `Archived`, `Inactive`) for any entity referenced by historical `Orders`, `Purchases`, or `AuditLogs`.
- **Uniqueness**: Slugs (products/categories), SKUs, Transaction IDs, and Order IDs are protected by unique constraints to prevent duplication.

## 3. Transactional Consistency & Concurrency
- **Atomic Operations**: Critical workflows (Checkout, Receiving Goods, Refunds) execute within strict database transaction boundaries. If any step fails, the entire operation rolls back.
- **Race Condition Protection**: Pessimistic locking or atomic increments are used during stock consumption to ensure `UnitsSold` never exceeds `CurrentStock` during concurrent orders.
- **Idempotency**: All financial and state-changing endpoints (Payments, Refunds, Webhooks) require an `Idempotency-Key` to prevent duplicate processing from network retries.

## 4. Reconciliation & Auditing
- **Inventory Reconciliation**:
  `OpeningStock + ReceivedPurchases - ConfirmedSales +/- ManualAdjustments = CurrentStock`
- **Financial Reconciliation**:
  `OrderTotal = Σ(ItemPrice * Qty) - Discounts + DeliveryFee`. Verified server-side against the `Payment` capture.
- **Audit Traceability**: Every administrative action generates an immutable record in the `AuditLog`, linking the `Actor`, `Action`, `Resource`, and `Timestamp`.

## 5. Operational Logic Constraints
- **Purchase Lifecycle**: State transitions are strictly enforced (`Draft` -> `Approved` -> `Ordered` -> `Received`). A `Cancelled` PO cannot be `Received`.
- **Refund Logic**: `TotalRefunds` can never exceed the `CapturedAmount` of the original payment.
- **Restocking**: Recommendations are derived dynamically from `Inventory`, `LeadTime`, and `SalesVelocity`. They are advisory and do not modify database state until a `PurchaseOrder` is explicitly approved.

## 6. Performance & Scale
- **Server-Side Pagination**: All large collections (Orders, Logs, Customers) use cursor-based or offset pagination to ensure fast response times.
- **Indexing**: Targeted indexes on `slug`, `status`, `customerId`, and `supplierId` optimize frequent query patterns without bloating storage.
