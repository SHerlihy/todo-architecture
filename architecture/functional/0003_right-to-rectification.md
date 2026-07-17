# ADR 0003: Right to Rectification

## Status
Proposed | ~~Accepted~~ | ~~Superseded~~

## Context

Users are able to input PII of themselves or other people into the application.
Users are able to input PII of other users into the application.

Should anyone request their PII we need to supply it within 1 month after identity verification.

PII includes IP addresses.
PII includes activity logs.

Scenario:
User enters task "add details for John Walker to form 16 gardens road 02/15/3093"
Should John Walker want to amend these details, it has a right to.

## Decision

Provision a central store of data that all potential PII data is replicated into.
Use AWS Macie to identify PII.
Use api operations to amend details.
Have a super user do these operations.

## Considerations

Can I run Macie on DynamoDB?
- No, S3 only

Can I use S3 as data store for DRY?
- Yes can do
- DRY is not greater that separation of concerns
- Having an S3 replica for Macie does separate concerns

Can I isolate PII to user account as access is 1 to 1?
- No, admin AWS account will have access to all data

## Consequences
### Positive (Pros)

### Negative (Cons)

