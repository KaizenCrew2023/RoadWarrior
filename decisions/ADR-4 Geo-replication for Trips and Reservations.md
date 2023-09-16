# ADR 4: Geo-replication for Trips and Reservations 

## Context

Road Warrior require their app to be international and be performant regardless of worldwide location.

## Decision

We will implement a multi region/geography write database solution for the Trips and Reservations database 

## Status

Proposed

## Consequences

Positive:
- **Performance** - Enables the geo-located reservation and trip services to access their databases 'locally' with performance being comparable across all regions.
- **Data consistency** - PaaS database will automatically replicate worldwide to ensure data consistency across regions
  
Negative:
- **Cost** - Worldwide replicate will cost, but is accepted for the benefit it provides. 

Alternatives:
- Geo-replication with single region write, multi region read. Updates will incur more latency but app performance for viewing reservation information will not be impacted. Thus notifcations of updates could be slower.
- Data segmentation by region of the user - the nature of the app implies users will use the app in multiple regions themselves, thereby will experience greater latency when travelling in other regions.

