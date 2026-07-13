# ADR 0002: Latency

## Status
Proposed | ~~Accepted~~ | ~~Superseded~~

## Context

User perception of app should be that it is quick.
Optimistic updates with quick error feeback is allowed for save function.
Require fast reads but are allowed slower writes.
There are no antagonistic requirements against minimal latency specified (i.e. cost).
Using MDN as guide to load times [MDN Load Times](https://developer.mozilla.org/en-US/docs/Web/Performance/Guides/How_long_is_too_long).

## Decision

Sub 1s latency for all functionaity

## Considerations

Application is simple so users would correctly expect low latency.
Mobile use occures in which users have a lower latency expectation.
