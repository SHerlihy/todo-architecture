# ADR 0003: Security

## Status
Proposed | ~~Accepted~~ | ~~Superseded~~

## Context

Users are only permitted to access user data.
Users can supply strings to save to database.
Software product is for United Kingdom region so subject to GDPR.
There is no expectation for data supplied to be subject to regulation.
Data supplied may be subject to trade secret level security.
Business requirements call for end to end encryption.

## Decision

Create a GDPR compliance system then create the software product.

Comply with GDPR.
Provide automated capabilities to service GDPR rights.
Ensure infrastructure provisioned is in EEA and UK area.
Have a data rention policy.
There are mounting data access requirements for users and non-users to access PII data, will have a separate self-service system.

## Considerations

What happens when a user is unable to access their data?
What happens when a third party claims we have their personal data and they want to see it?
How are users identified for login?
What happens if non-user exercises right to be forgotten on user data?

Can I use a 3rd party SaaS for GDPR compliance?
- there are offerings but they look out of scope of architecture

## Consequences
### Positive (Pros)

### Negative (Cons)

