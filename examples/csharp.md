# C# examples

## Good

```csharp
logger.LogInformation("User registration completed for {UserId}", user.Id);
```

Stable event, structured internal identifier, no submitted payload.

```csharp
catch (DuplicateUserException)
{
    logger.LogWarning("User registration rejected because the account already exists");
    throw;
}
```

Handled outcome without email, password or command object.

## Counterexamples

```csharp
logger.LogInformation("Registering {Email} with {Password}", request.Email, request.Password);
```

Leaks a secret and unnecessary personal data.

```csharp
logger.LogError(exception, "Failed: {Message}; {@Request}", exception.Message, request);
```

Duplicates exception text and destructures a potentially sensitive request.
