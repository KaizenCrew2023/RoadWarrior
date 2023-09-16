# ADR 7: Backends for Frontends for Android and iOS Apps 

## Context

RoadWarrior has multiple different frontend applications, each with unique requirements and performance considerations. The traditional approach of having a single backend serving multiple frontends is not sufficient to meet the unique requirements of our mobile applications.

## Decision

We will have dedicated backend for frontend (BFF) service for our iOS and Android mobile applications.

## Status

Accepted

## Consequences

Positive:

* **Performance optimised** - backend services can easy align with the specific performance requirements of each frontend.
* **Scalable** - backend services can dynamically scale based on the load and traffic of each mobile frontend.
* **Flexibile/evolvable** - new mobile frontends or updates to existing ones can be done with miminam disruption to the architecture.

Negative:

- **Single point of failure** -  if the backend service becomes unavailable, the mobile app will not function.
- **Architectural complexity** - multiple backends for frontends increases complexity; clear communication and documentation are needed.

Alternatives Considered:
- API Gateway to manage interactions between frontends and the backend.
