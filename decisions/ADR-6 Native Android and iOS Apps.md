# ADR 6: Native Android and iOS Apps 

## Context

Road Warrior have made a strategic decision to have the richest user experience possible across all deployment platforms, which includes Mobile apps.

## Decision

We will build native Mobile apps for both iOS and Android.

## Status

Accepted

## Consequences

Positive:
- **Separation of concerns** - Each operating system gets the richest UX for that platform
- **Flexibile/evolvable** - Dedicated app features can be built targetting the relevant device, without impactung the other device and/or web users.

Negative:
- **Cost** - each app will require dedicated development
  
Alternative Considered:
- Cross platform app - would not necessarily offer the richest experience on each mobile device type.
