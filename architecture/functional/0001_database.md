# ADR 0001: Database

## Status
Proposed | ~~Accepted~~ | ~~Superseded~~

## Context

Users are only allowed to access their own data.
Data stored is taks data and well defined.
Read speed is a critical factor.

## Decision

DynamoDB

## Considerations

Database ACID vs BaSE:
Isolation supports the 1 to 1 data to user relation.
Consistency is supported as reads should be correct but writes are allowed errors.
BaSE characteristics not supported as users want to see tasks at a glance.
Choosing ACID.

Data is well defined, suitable for table.
Relationships between data are simple.

## Consequences
### Positive (Pros)

Single digit millisecond performance.
Severless.
Fully managed.
Pay per use pricing supports daily spikes.

### Negative (Cons)

Brittle to future changes to how data can be used.
Could always migrate.
