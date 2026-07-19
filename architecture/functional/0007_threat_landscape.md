# ADR 0007: Threat Landscape

## Status
Proposed | ~~Accepted~~ | ~~Superseded~~

## Context

Users and anyone (given the GDPR rights stuff) are able to input any string data.
Data has to be subject to end to end encryption.
Data has to be subject to encryption at rest.

## Decision

Protect against users and rights request abuse.
- Injection attacks
- Dencryption attempts
Not protecting against the team of 2 engineers, just prevent accidents.

## Considerations

Treating user data supplied as requiring high security due to PII and business secrets.

Maintance engineers are a team of 2.

## Consequences
### Positive (Pros)

### Negative (Cons)
