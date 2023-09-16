# ADR-2: Micro Frontends

## Context

Road Warrior has made a strategic design decision to separate its core subdomians from supporting subdomains to enable it to outsource supporting subdomains where required.

## Decision

We will build micro-front ends for the web application.

## Status

Accepted

## Consequences

Positive:

- Enables each micro front end to be for distinct subdomains 
- Enables outsourcing of the development of supporting subdomains
- Each front-end could be owned by independent teams as the application scales in size
- The technology choices in the future can evolve without needing that 'major' rewrite

Negative:

- Each team could diverge technology or framework for their front-end resulting in Micro Frontends Anarchy. 
- Needs co-ordination between teams for style and layout consistency

Alternatives considered:

- Single page app for the entire application - hard to develop / maintain across teams and far harder to outsource. Single page apps can effectively become their own monolith.


