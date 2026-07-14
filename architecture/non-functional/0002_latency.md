# ADR 0002: Latency

## Status
Proposed | ~~Accepted~~ | ~~Superseded~~

## Context

User perception of app should be that it is quick.
Optimistic updates with quick error feeback is allowed for save function.
Require fast reads but are allowed slower writes.
There are no antagonistic requirements against minimal latency specified (i.e. cost).
Using MDN as guide to load times [MDN Load Times](https://developer.mozilla.org/en-US/docs/Web/Performance/Guides/How_long_is_too_long).

Network coverage: https://www.ons.gov.uk/explore-local-statistics/indicators/5g-coverage
5G coverage on 73% in UK

https://www.ons.gov.uk/explore-local-statistics/indicators/4g-coverage
4G 96.2%

3G is deprecated

## Decision

Sub 1s latency for all functionality.
Can rely on 5G network speed.

## Considerations

Application is simple so users would correctly expect low latency.
Mobile use occures in which users have a lower latency expectation.

Are we happy for no 5G coverage in Breacon Becons and around Scottish boarder?
Yes, after business chat requirements state most usage from London or Manchester.
