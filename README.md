# OpenGI Katas - Flex Exams [Feb 2024]

## Contents
* [Business Case](#business-case)
* [Requirements](#requirements)
* [Architecture](#architecture)
   * Work flows
   * Contex map
   * [Characteristics](#characteristics)
   * [Architectural Style](#architectural-style)
   * [Architecture Decision Records](#architecture-decision-records)
   * [Architectural Principals](#architecture-principals)
   * [Architecture Diagrams](#architecture-diagrams)
   * Deployment
* Development plan
  * Development team   
  * Milestones
 
## Business Context
SSS GmbH, a prominent certification body in Germany, conducts 30,000 exams annually across various sectors. They provide FLEX EXAMS for remote testing and collaborate with Pearson VUE for Test Center Exams. Challenges with the current third-party exam system, including downtime and slow support, prompt SSS to seek a new solution. The objective is an in-house, scalable online exam system aligning with SSS's vision for robust and customizable solutions. The goal is to enhance efficiency, reliability, and business diversification.
## Requirements

_For the original requirements, please see [here](./original_requirements/original_requirements.md)_

### Functional Requirements

- **User management**: for admin users to be able to manage other system administrators and roles
- **Exam management**: for administrators to be able to create exams and preview exams
- **Question management**: for administrators to be able to create and manage exam questions, set scores, score calculations
- **Audit trail**: track changes to data with the following information: Action (created, edited, deleted), Title, Modified By, Modified On. The trail will be available for searching by each of the columns.
- **Participant registration**: register the participant in the system, integrated with a client management system
- **Identity verification**: Allow for uploading of ID documents and video recording/photographing of candidates during the exam
- **Mobile application**: A mobile application, which use of the camera, for additional security and identity checks during the exam
- **Third party integrations**: Integrations with JIRA, Google Business and Salesforce.

### Non-functional requirements

- **Localization**: Ability to easily display multiple languages
- **Branding**: The look and feel of the system should be configurable according to brand guidelines and customers branding guidelines
- **Responsiveness**: Page load times should be under 2 seconds, 5 seconds will be considered acceptable
- **Performance**: The system should support 1000 users at any time, and there should be zero downtime.
- **Modularity**: The system should be easily upgraded in the future with minimal investment
- **GDPR**: The system should be fully compliant with GDPR
- **Support**: There should be 1st level, 24/7, support

## Architecture

During the requirements analysis phase, we identified several architectural characteristics that are significant for the system. We grouped them into driving and implicit characteristics.

Driving and implicit characteristics are important to identify the most preferred architecture style or combination of them.

#### Driving characteristics

| Characteristic | Description |
|--|--|
| Performance | Performance is essential to provide a responsive and user friendly experience |
| Scalability | The system needs to be scalable, so that it can cope with large demand of circa 1000 users |
| Data Integrity | Data across the system must be kept correct, there must be no loss across the system to maintain integrity in the exam certificates issues. Data also includes sensitive information such as ID, so must be kept secure |
| Evolvability | The system will need to be open to new features and services to add new functionality without disrupting existing operations |

### Implicit characteristics

| Characteristic | Description |
|--|--|
| Availability | The system must be available at all times, with 24/7 availability. The system will be multi-region meaning no downtime will be acceptable as the system must be accessable world-wide at all times |
| Changeability | The system needs to be easy to add to later on, as well as be easy to customise so that the branding of SSS can be used across the platform |
| Security | Parts of the system need to be secure and whitelisted to certain people only as well as keeping secure user data  |

### Decision

The team picked three of the most important characteristics, Configurability, Performance and Scalability and came to the conclusion that an **event-driven architecture** would best suit the system. This would allow for features to be easily added, the system to be very scalable and to perform well.

![Architecture Decision](./architecture/architecture_selection.png)

### Architecture Decision Records

- [**ADR-1**](./adrs/1_architecture.md) - Use Event-Driven Microservices Architecture
- [**ADR-2**](./adrs/2_micro_frontends.md) - Use Micro Front-Ends for the Web Applications
- [**ADR-3**](./adrs/3_Message_Service.md)  - Use Message Service for Event Driven Architecture
- [**ADR-4**](./adrs/4_CDN.md) - Use Cloud Content Delivery Network
- [**ADR-5**](./adrs/5_Kubernetes.md) - Use Kubernetes to Deploy and Run Microservices

### Architectural Principals
- **Cloud native** - design the system  to take full advantage of the cloud. 
- **Design for scale** - when designing systems, think about scalability by breaking down components for flexible growth. Use scalable technologies and consider asynchronous design for better performance.
- **Automate everything** - prioritize automation by incorporating it seamlessly into the core design. Ensure the system is built with automation in mind from the beginning, covering automated builds, deployments, testing, monitoring, and alerting.
- **APIs are potential products** - develop APIs with the mindset of creating valuable products. Consider customer needs, emphasize user experience, and ensure ease of use, for external consumers and internal systems or developers.
- **Strategic Adaptability** - build adaptable solutions, balancing innovation with a careful consideration of potential dependencies, customizing the design to benefit from the chosen technology.
- **Zero-downtime deployments** - ensure smooth deployments with zero downtime. 
- **Secure by design** - prioritize security integration from the beginning. Incorporate security as a fundamental part of the development process.

### Architecture Diagrams
In order to visualize, describe and communicate the software architecture  for the system, we will use C4 model. In  ubiquitous language for the C4 diagrams, software system is made up of one or more containers (applications and data stores), each of which contains one or more components, which in turn are implemented by one or more code elements (classes, interfaces, objects, functions, etc).More info for the C4 Modelling approach can be find [here]([./original_requirements/original_requirements.md](https://c4model.com/)https://c4model.com/)_

#### Level 1 - System Context

A System Context Diagram is a visual representation at a high level, ilustrating a system or software application within its broader context. It shows the interactions between the system and external parts, like  users, other systems, thirt party integrations or data sources.
