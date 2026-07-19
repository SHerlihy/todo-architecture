ADR 0006: Right Request Database

## Status
Proposed | ~~Accepted~~ | ~~Superseded~~

## Context

Rights requests are time sensitive.
Rights requests can amend data so later requests need to respect previous requests.
The current architecture relies on manual ID verification.
This means Engineers need to be able to handle rights requests in order.

## Decision

Amazon Timestream

## Considerations

SQS has enough storage in messages for request data.
SQS does order requests.
SQS is an in memory store so not suitable for 2 week sorage of current architecture.

Time-series database can query data by time.
Time-series database is insert only.
Not in memoriy so is suitable for 2 week storage.

## Consequences
### Positive (Pros)

### Negative (Cons)
