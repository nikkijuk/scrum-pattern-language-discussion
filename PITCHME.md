### Scrum Pattern Language Discussion
![Logo](jambit_logo.png)
---
## What is this about?
- definition of patterns and pattern language 
- well known examples
- scrum as pattern language
- design, especially software architecture, patterns 
- discussion if software development can be given direction with company specific pattern laguage?
---
## Definitions
---
[A pattern]( https://en.wikipedia.org/wiki/Pattern) is a regularity in the world, in human-made design, or in abstract ideas. As such, the elements of a pattern repeat in a predictable manner.
---
[Software design pattern](https://en.wikipedia.org/wiki/Software_design_pattern) is a general, reusable solution to a commonly occurring problem within a given context in software design.
---
[A pattern language](https://en.wikipedia.org/wiki/Pattern_language) is an organized and coherent set of patterns, each of which describes a problem and the core of a solution that can be used in many ways within a specific field of expertise. 
---
## Examples
---
### GOF aka Gamma et al 1995. 
- Design Patterns: Elements of Reusable Object-Oriented Software.  
- Creational, Behavioral and Structural patterns
- Iterator, visitor, Bridge, Builder, Decorator, ..
---
![gof](gof_patterns.gif)
---
### POSA 1 aka Buschmann et al 1996. 
- Pattern-Oriented Software Architecture, Volume 1: A System of Patterns.
- Architectural and Design Pattern, Idioms
- Layers, Pipes and Filters, Broker, Model-View-Controller, .. 
---
![posa-1](posa1_patterns.png)
---
### Hohpe & Woolf 2003. 
- Enterprise Integration Patterns: Designing, Building, and Deploying Messaging Solutions. 
- Channel, Message Construction, Routing, Transformation, Endpoint and System Management Patterns.
- Idempotent Receiver, Message Bus, Canonical Data Model, ..
---
![eai](eai_patterns.png)
---
### Evans 2004. 
- Domain-Driven Design: Tackling Complexity in the Heart of Software.
- Organized by process, not by patterns
- Bounded Context, Ubiquitous language, ..
---
![ddd](ddd_patterns.png)
---
## Pros
---
### Technology Heterogeneity
- best tool for the job can be picked (e.g. different programming language or persistence
  technology)
- service with smallest impact can be chosen for trying out a new technology
---
### Resilience
- monolith: if the backend fails, the result is total system outage
- if one service in the system fails, the error should not cascade
- several instances of a service can be run -> if one fails, the other one takes over
---
### Scaling
- monolith: all or nothing can be scaled
- ms architecture: dedicated services can be scaled depending on their workload
---
### Ease of deployment
- changing and deploying one single service is less likely to bring the whole system down
- services can be deployed independently
- deployment problems can be isolated more quickly
- less fear to release -> more releases
- features get shipped more quickly
---
### Organization alignment
- distributed teams (one team per service) is possible
- smaller teams working on smaller codebases tend to be more productive
- teams can work with independent processes (scrum, kanban, ...)
--- 
### Composability
- microservices allow for functionality being consumed from different parties in different ways for different purposes
- e.g. useable from other services, web apps, desktop applications…
--- 
### Optimizing for replaceability
- small services should be rewriteable in a couple of weeks
- less fear to throw things away or change existing services
---
## Cons
---
### Distributed system
- performance decreases (communication via network)
- added complexity for asynchronous messaging
- services might be not reachable -> more effort for error handling
- distributed systems are harder to debug
---
### Eventual consistency
- microservices imply autonomy and decentralized data management
- distributed transactions are often not used (especially across domains)
- developers have to be aware of consistency issues
---
### Operational complexity
- continiuous delivery essential for microservices
- more services to monitor, deploy and manage
---
## Sources 
- Sam Newman, Building Microservices, Chapter 1: Microservices - Key Benefits
- Martin Fowler, Microservices Trade-offs, https://martinfowler.com/articles/microservice-trade-offs.html
--- 
## Thanks for discussing!
- https://www.github.com/gernd/microservice-discussion
