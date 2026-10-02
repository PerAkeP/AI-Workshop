# TypeScript examples

## Good

```typescript
logger.info({ orderId: order.id, outcome: "created" }, "Order creation completed");
```

Stable event with structured internal context.

```typescript
logger.warn("Login rejected", { reason: "invalid-credentials" });
```

Records a security outcome without credentials.

## Counterexamples

```typescript
logger.info(`Login for ${request.email}: ${request.password}`);
```

Leaks credentials and personal input.

```typescript
logger.error("Order failed", { request, error: error.message });
```

Logs a complete request and may duplicate sensitive exception text.
