# ADR 1: Use Event-Driven Microservices Architecture
**Date:** 28/02/2024

## Status
Adopted

## Context
Performance, availability, data integrity, scalability and configuralibity have been identified as crucial architectural characteristics for the system. Performance, availability and data integrity as subset of the architecture characheristics, are determined as driving characteristics for the system.
Using the Architecture Styles Worksheet, the team choose the event-driven architecture as the best option.

The event-driven architecture style achieves a good separation of components in the application but its implementation can vary. For example, event-driven components might be integrated within a monolithic architecture or within a microservices architecture. Selecting the microservices approach helps the system scale up easily. This is a logical and beneficial extension of choosing the event-driven style.

## Decision
* We will use an event-driven architecture within our system.
* Event-consuming components will be developed as microservices

## Consequences
### Positive
* Scalability - easily scale horizontally to handle increased users and traffic.
* Extensible - relatively easy to add new services or integrate third-party services.
* Fault-tolerant - event-driven microservices are naturally robust and can handle faults.
* High Adaptability - new microservices can be easily added or removed  to handle different events or types of events.
* Monitoring -  track the path of events and observe how data is handled.
### Negative
* Complexity - rising complexity, leading to challenges in coordination, deployment, debugging and troubleshooting.
* High learning curve - might require the team to invest time and effort in understanding and mastering the concepts, tools, or practices.

