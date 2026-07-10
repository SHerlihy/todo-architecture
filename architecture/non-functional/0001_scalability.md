# ADR 0001: Scalability

## Status
Proposed | ~~Accepted~~ | ~~Superseded~~

## Context

The product is solely accessed by users.
Each user only has access to their own data.
Users are all from the same timezone.
Users only access the product during business hours.
Increased usage is expected at the beginning and end of business hours.
Therefore, workload usage is predictable.

## Decision

Servers with automatic scaling and containerisation will be used.
Aligned with AWS BP 11.2

## Considerations

Serverless application:
Is able to service the identified spikes in utilisation.
Is able to service unpredictable utilisation, which is the current case.
Latency increased through cold starts.

Servers with automatic scaling and containerisation:
Exact utilisation is currently unknown.
However, utilisation can be predicted as supproted by the business requirements identifying a usage pattern.

## Consequences
### Positive (Pros)

Right sizing of provisioned capacity by using auto scaling.
Reserved instances for EC2 can be used once usage is establised for cost savings.
Latency is low for majority of users as will not need to wait for server to start.

### Negative (Cons)

Peak load times for users may be slower until enough usage data is collected to predict usage.
Unused capacity at servers will not be 100% utilised for performance sake.

### Note

I was initially considering serverless until I noted the usage is predictable and there is a business requirement for low latency.
