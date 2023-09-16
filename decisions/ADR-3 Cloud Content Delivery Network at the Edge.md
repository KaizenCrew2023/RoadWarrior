# ADR-3: Cloud Content Delivery Network at the Edge 

## Context

Road Warrior must work internationally and deliver 300ms response times on the web and First Contentful Paint in under 1.4s in the mobile app regardless of users' location. 

## Decision

We will use a cloud content delivery network at the edge for serving content and APIs to the most suitable geo-location for the user.

## Status

Accepted

## Consequences

Positive:

* **Performance** - serving static and dynamic content via a content delivery network at the edge, closer to the user's device, will help lower latency and response times.

Negative:

 * **Cost** - multi-region deployments and cloud-based CDN/edge services are more expensive than single region deployments.
 * **Complexity** - multi-region deployments could be more complex to manage. Ease of implementation should be considered when selecting a cloud CDN. 

Alternatives considered:

* Single region hosting and accepting some regions have poorer performance due to latency.
