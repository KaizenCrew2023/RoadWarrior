# ADR 7: Backends for Frontends for Android and iOS Apps 

## Context

RoadWarrior has multiple different frontend applications, each with unique requirements and performance considerations. The traditional approach of having a single backend serving multiple frontends is not sufficient to meet the unique requirements of our mobile applications.

## Decision

We will have dedicated backend for frontend (BFF) service for our iOS and Android mobile applications.

## Status

Proposed

## Consequences

Positive:
- Improved user experience - optimizing data presentation and interactions to align with the specific needs and expectations of each mobile app user
- Performance optimization - backend services aligned with the specific performance requirements of each frontend
- Scalability - backend services can dynamically scale based on the load and traffic of each mobile frontend
- Flexibility for future evolving - new mobile frontens or updates to existing ones can be done with miminam disruption to the architecture

Negative:
- Single point of failure -  if the BFF service becomes unavailable, the mobile  app will not function
- Architectural complexity - multiply BFF increased the complexity, clear communication and documentation needed

Alternatives Considered:
- API Gateway to manage interactions between frontends and the backend
