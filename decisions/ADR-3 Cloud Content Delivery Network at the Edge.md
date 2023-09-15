# ADR-3: Cloud Content Delivery Network at the Edge 

## Context

Road Warrior require their app to be international and be performant regardless of worldwide location. 

## Decision

We will use a cloud content delivery network at the edge for serving content and APIs to the most suitable geo-location for the user.

## Status

Proposed

## Consequences

Positive:
- App performance is not compromised due to geo-location.

Negative:
- Cost - all apps and services require multi geo-location deployments
- App deployment updates / rollout becomes more complex

Alternatives considered:
- Single region hosting and accepting some regions have poorer performance due to latency
