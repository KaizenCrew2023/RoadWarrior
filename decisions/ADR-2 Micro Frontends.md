# ADR 2: Micro Frontends

## Context

Web browser users of the Road Warrior app should experience as rich a UI as possible. 
Speed to delivery of change will be key to be a leading player in this domain for the start up company.


This section describes the forces at play, including technological, political, social, and project local. These forces are probably in tension, and should be called out as such. The language in this section is value neutral. It is simply describing facts.

## Decision

The web/browser based front end will be composed of micro-front ends. 

## Status

Proposed

## Consequences

Positive:

- Enables each micro front end to be for a distinct area of business. 
- Each front-end could be owned by independent teams as the application scales in size
- The technology choices in the future can evolve without needing that 'major' rewrite

Negative:

- Each team could diverge technology or framework for their front-end resulting in Micro Frontends Anarchy. 


Alternatives considered:

- single page app for the entire application - can lead to development and deployment bottlenecks/conflicts resulting in slower to deliver enhancements. Single page apps can effectivey become their own monolith

