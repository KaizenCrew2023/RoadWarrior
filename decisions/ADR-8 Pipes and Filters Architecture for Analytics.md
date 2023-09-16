# ADR 8: Pipes and Filters Architecture for Analytics 

## Context

Road Warrior gathers analytical data from users' trips for various purposes such as travel trends, locations, airlines and hotel vendor preferences. It also analyses traveller behaviour including cancellation and update frequency.

## Decision

We will use a pipes and filters architecture for ingesting and processing data for analytics.

## Status

Accepted

## Consequences

Positive:

* **Modular** - data processing pipelines can be broken down into discrete components (filters). Filters are relatively easy to maintain and the pipeline can be easily extended to incorporate additional data processing requirements, such as data anonymisation and data cleansing. 
* **Scalable** - data processing can be parallelised and, as data volumes grow, individual filters can be scaled to handle increased load.
* **Separation of concerns** - enforces clear separation of concerns between different processing steps making it easier to understand and manage data processing workflows.
* **Fault tolerant** - can be designed to gracefully handle failures in individual filters without disrupting the entire pipeline. 

Negative:

* **Centralised** - as the system grows, centralised data pipelines may not adapt well to more complex systems with a large number of subdomains, potentially leading to issues with data ownership and insufficent domain expertise. As Road Warrior scales a distributed data mesh architecture may be more suitable. 
