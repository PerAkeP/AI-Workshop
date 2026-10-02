# Java examples

## Good

```java
log.info("Document import completed documentId={} outcome={}", document.id(), "accepted");
```

Stable event with safe structured context.

```java
catch (UnsupportedFormatException exception) {
    log.warn("Document import rejected: unsupported format");
    throw exception;
}
```

Handled outcome without document contents or submitted filename.

## Counterexamples

```java
log.info("Import request: " + request);
```

Object conversion may expose the complete payload.

```java
log.error("Import failed token={} because {}", request.token(), exception.getMessage(), exception);
```

Leaks authentication material and repeats exception text.
