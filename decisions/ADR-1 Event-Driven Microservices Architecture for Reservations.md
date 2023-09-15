# ADR 1: Event-Driven Microservices Architecture for Reservations

## Context

Road Warrior is a startup plannig to (quickly) scale to 15 million subscribed users and 2 million weekly active users. Works internationally. 

It can automatically scan users' emails to detect new travel reservations and will process a high volume of new reservations and updates to existing reservations at a relatively high frequency.

## Decision

We will use an event-driven microservices architecture for the Reservations subdomain. 

## Status

Proposed

## Consequences

Positive:
* Asynchronous communication (supports our principle)
* Highly scalable
* Performance
* Fault tolerant
* Domain separation 

Negative: 
* Not as simple as service-based but offers higher performance?

Neutral:

