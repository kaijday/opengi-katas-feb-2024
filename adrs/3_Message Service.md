# ADR 0: Use Message Service for Event Driven Architecture
**Date:** 28/02/2024

## Status
Adopted

## Context
In [ADR 1](./1_Architecture.md) we have decided to use an event-driven approach, with micro-services, and we need an approach for sending the messages around the system to the correct consumers.

## Decision
Use a messaging queue, such as Azure Service Bus.

## Consequences
### Positive
- Asyncronous processing, speeds up API calls
- Message queues enable asynchronous communication, which means that the endpoints that are producing and consuming messages interact with the queue, not each other. Producers can add requests to the queue without waiting for them to be processed. Consumers process messages only when they are available. No component in the system is ever stalled waiting for another, optimizing data flow
- Loose Coupling will help us decouple applications and services from each other
- There is a known expectation, from the publisher, about how the message is being handled

### Negative
- Complexity is added maintaining data flow between services
