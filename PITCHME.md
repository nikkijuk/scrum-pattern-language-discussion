### Microservice Architecture Discussion
![Logo](jambit_logo.png)
---
## What is this about?
- discussion of several pros/cons for microservice architecture
- share your "real world experience" 
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
