# ADR 0004: GDPR Rights

## Status
Proposed | ~~Accepted~~ | ~~Superseded~~

## Context

GDPR rights requests need to be serviced within 1 month.

PII includes IP addresses.
PII includes activity logs.

## Decision

Queue rights requests with id validation information.
Go through requests in serial to avoid amend conflicts.
Do this every 2 weeks to give enough time for issues to be communicated.

online portal for rights requests, public access
to
key-value DynamoDB
API to view request
ID verification happens
rights request is fulfilled
through use of provided APIs
database value is archived then deleted

## Considerations

Servicing rights on an ad hoc basis.
- May be possible if usage was known
- but is not

Servicing rights on an interval:
- time to wait does cut into 1 month timeframe

How to handle id verification?
- again ad hoc/serial is inefficient
- can queue up to avoid conflicts in amendment
- should verification fail, notify requester

An automated system is important as should the 2 engineers get a few rights requests they will spend a long time servicing without any tools to help.

2 weeks is a long time so in memory queue is not suitable

How is verification information being viewed?

## Consequences
### Positive (Pros)

### Negative (Cons)

