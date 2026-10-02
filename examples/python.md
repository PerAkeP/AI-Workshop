# Python examples

## Good

```python
logger.info("payment submission completed", extra={"payment_id": payment.id, "outcome": "accepted"})
```

Stable event and safe internal correlation value.

```python
except PaymentRejected:
    logger.warning("payment submission rejected")
    raise
```

Handled outcome without card data or command object.

## Counterexamples

```python
logger.info(f"paying with card {request.card_number}")
```

Exposes payment data in a constructed message.

```python
logger.exception("submission failed for %r", request)
```

The object representation may contain secrets or sensitive payload values.
