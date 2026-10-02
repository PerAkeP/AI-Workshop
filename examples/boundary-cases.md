# Boundary cases

## Is an email address always forbidden?

Not necessarily, but it is personal data and is often unnecessary. Prefer an internal user ID. An approved audit requirement is a domain decision outside this exercise.

## Is hashing sensitive data enough?

Not automatically. Stable hashes of guessable values may still enable identification. Do not invent hashing as a universal solution.

## Is structured logging always safe?

No. Structured properties can expose exactly the same sensitive values as formatted strings.

## May debug logs contain secrets in development?

No. Development logs are copied and shared. The prohibition applies to every level and environment.

## Should every caught exception be logged?

No. Log at the layer that handles the failure or terminates the operation. Logging at every layer creates duplication and increases disclosure.

## What if no safe identifier exists?

Record operation and outcome without the sensitive identifier. Do not manufacture a reversible substitute.
