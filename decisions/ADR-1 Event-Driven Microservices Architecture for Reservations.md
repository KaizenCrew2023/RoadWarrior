# ADR 1: Event-Driven Microservices Architecture for Reservations

## Context

Road Warrior is a startup plannig to quickly scale to 15 million subscribed users and 2 million weekly active users, distributed globally.

It can automatically scan users' emails to detect new travel reservations and will process a high volume of new reservations and updates to existing reservations at a relatively high frequency.

## Decision

We will use an event-driven microservices architecture for the Reservations subdomain. 

## Status

Accepted

## Consequences

Services in the reservation management context will comminicate with each other through events published to an event broker.

Positive:

* **Loosely coupled** - facilitates loose coupling between microservices. Services, therefore, can remain independent and are easier to modify or replace services without affecting the entire system. It also supports clear domain separation.
* **Extensible** - event-driven systems are relatively easy to add new services or integrate third-party services.
* **Highly scalable** - services can be deployed and scaled independently based on the volume of events they need to process. This enables more efficient resource utilisation and better performance as the system grows. 
* **Asynchronous communication** - services can publish events and continue their work without waiting for a response. This can improve system responsiveness and overall perforamnce.
* **Fault tolerant** - event-driven microservices are inherently resilient and fault tolerant. If a service is unavailable, events can be buffered in the event broker. Once the service is restored, it can catch up on missed messages, ensuring (eventual) data consistency and system reliability.   
* **Monitoring** - event-driven architectures make it easier to trace the flow of events and monitor how data is processed. 

Negative: 
* **Complexity** - event-driven architectures are more complex to implement and manage than alternatives considered, such as modular monolith or service-based architecture. Managing event broker clusters, monitoring message queues and nsuring high availability of the event broker infrastructure can be operationally complex.

Neutral:

* **Eventual consistency** - relies on eventual consistency (although we consider this architecture suitable to satisfy the requirement to process reservation updates within 5 minutes of receipt)
* **Flexible** - many of the systems subdomains have a partnership-type relationship lending themselves to the flexibility of loosely defined message interfaces early on in development and evolving to stricter, more clearly defined schemas as the system matures.
