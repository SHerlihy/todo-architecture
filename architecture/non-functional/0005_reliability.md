# ADR 0005: Reliability

## Status
Proposed | ~~Accepted~~ | ~~Superseded~~

## Context

Reliability is a success criterion of the business requirements.
Data should not be lost during normal operation, so all defined operation.
Saving a task is allowed to fail only if the failure is communicated to the user.

## Decision

An error feedback capability will need to be provisioned.
Focus on maximal reliabilty in viewing tasks.
Rely on error feedback to cover reliability issues in saving tasks.

Local storage is unacceptable to to highly variable reliability.

## Considerations

Use user on device storage:
- simplifies maintanance
- simplified GDPR
- user device reliabilty is highly variable so unsuitable

Zero failures:
- Eliminates need for error feedback mechanisms
- Not possible as there are no 100% SLAs

Same reliability for viewing tasks and saving tasks:
- The business requirements make no allowance for error in viewing tasks

## Consequences
### Positive (Pros)


### Negative (Cons)


