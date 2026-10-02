# Safe logging standard

## Purpose

Logs must support operation, diagnosis and security monitoring without unnecessarily exposing information.

## Rules

### SL-1: Never log secrets

Do not log passwords, private keys, access or refresh tokens, session identifiers, API keys, authorization headers or other authentication material.

### SL-2: Minimize sensitive data

Do not log full national identifiers, payment data, health data, precise addresses or complete user-provided objects. Prefer an approved non-sensitive internal identifier. Masking is only acceptable when explicitly defined by the domain.

### SL-3: Use structured, stable events

Use stable event descriptions and separate named properties rather than building messages from untrusted values. Structured logging does not make a sensitive value safe.

### SL-4: Log outcomes, not payloads

Record the operation and outcome. Do not log request bodies, DTOs, domain objects or serialized payloads by default.

### SL-5: Handle exceptions carefully

Log an exception at the layer responsible for handling or terminating the operation. Avoid logging the same exception at every layer. Do not copy potentially sensitive exception messages into extra fields.

### SL-6: Preserve useful context

Where appropriate, include safe context such as operation name, internal entity ID, existing request or trace ID, outcome and duration. Do not invent a reversible substitute for sensitive data.

### SL-7: Choose an appropriate level

- Information: expected lifecycle and business-operation outcomes.
- Warning: unexpected but handled situations.
- Error: failed operations requiring investigation.
- Debug or trace: detailed diagnostics, but still never secrets.

## Priority when rules conflict

1. Prevent disclosure of secrets and sensitive data.
2. Preserve application correctness.
3. Retain the minimum necessary operational context.
4. Improve readability and style.

## Out of scope

This standard does not select a logging library or define retention, platform access control or every domain-sensitive field. If sensitivity is unknown, omit the value or request domain guidance rather than assuming it is safe.
