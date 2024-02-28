# ADR 4: Use Cloud Content Delivery Network
**Date:** 28/02/2024

## Status
Adopted 

## Context
Our system should support at any time up to 1000 consecutive users. Ideally expected page load time should be under 2 seconds regardless of users' location. The system should do a live video streaming that eequres a high availability.
## Decision
We will use a cloud-based content delivery network to distribute content to the optimal geographic location for the user.

## Consequences
### Positive
* Performance - serving static and dynamic content via a content delivery network, closer to the user's device, will help lower latency and response times.
* Scalability - by offloading content delivery to the CDN, our system gains scalability benefits, ensuring consistent performance even during traffic spikes.
### Negative
* Cost - multi-region deployments and cloud-based CDN are more expensive than single region deployments.
* Complexity - multi-region deployments could be more complex to manage. Ease of implementation should be considered when selecting a cloud CDN.

