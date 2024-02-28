# ADR 2: Micro Frontends
**Date:** 28/02/2024

## Status
Adopted

## Context
Micro Frontends is an architectural pattern that decomposes a user interface into smaller, independent, and loosely-coupled components that can be developed, deployed, and scaled independently. This allows teams to work on different parts of the application simultaneously, reduces the complexity of the development process enabaling  greater flexibility, scalability, and maintainability in user interface development.

## Decision
We will build micro-front ends for the web applications.

## Consequences
### Positive
* Component Isolation - Micro Frontends enable component isolation, each front-end could be owned by independent teams, allowing teams to work  on different parts of the application. This results in faster development and deployment cycles.
*  Development  freedom - Teams can choose the most suitable technologies for their micro frontend, fostering innovation and flexibility.
*  Independent Deployment -  Each micro frontend can be deployed independently, enabling continuous delivery.
*  Enhanced Scalability - Horizontal scaling can be done by deploying instances of individual micro frontends, enabaling  scalability.

### Negative
*  Complexity of Orchestration - Communication between micro frontends adds an additional layer of complexity and  co-ordination  between teams is needed for style and layout consistency.
*  Micro Frontends Anarchy - Each team could diverge technology or framework for their front-end.

### Alternatives considered
Single Page Application (SPA) - Hard to be developed and maintained across teams, complexity increases as the application grows.
