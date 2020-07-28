## Monolithic vs Microservices
In traditional, monolithic apps, the locations of resources are well known, relatively static, and found in configuration files (or hard coded). Even if a monolithic app has been divided into different tiers, such as for the user interface, app logic, database access, and others, the location of resources used by the app tend to be well defined and static. Often times, all tiers of the app are hosted in the same geographical location even if they are replicated for availability. Connections among the different parts of the app tend to be well defined, and they don’t tend to change very much.

However, this is not the case for a microservices implementation. Whether that app is built from scratch or is gradually being built by breaking off functions of a monolithic app, the location of a given service could be anywhere. The microservice could be in a corporate data center, a public cloud provider, or some combination. It could be hosted on bare metal servers, virtual machines, containers, or all these.

## SOA vs Microservices Architecture
services oriented architecture (SOA) relates to exposing business functions and data via standardized interfaces for re-use across the enterprise.
For large enterprises, with a multitude of aging systems of record, an SOA program is likely to spend a significant amount of time solving hard integration problems in order to surface complex back end systems of record as re-usable interfaces. After a while, it may start to feel like SOA was all about integration.

The aim of a microservice architecture is to completely decouple application components from one another. This is typically with the aim of improving agility; the velocity at which functionality can be delivered. 

    Some microservices principles are really different to SOA
It’s also worth knowing that microservices architecture introduces some principles that will be pretty surprising to someone from an SOA background. Here are some key examples:
- Re-use: Microservices is about creating small truly independent components. So for example, for SOA re-use was one of the primary perceived benefits. The ability to re-use data and function from one application in another. However, for microservice components, re-using a component, especially at runtime, and perhaps even at design time results in dependencies that make the resulting solution fragile, so re-use is often discouraged.
- Inter-communication: SOA typically resulted in the exposure of synchronous web services such as SOAP/HTTP. In microservices, a synchronous protocol such as HTTP, whether SOAP or REST based causes a real-time dependency between components, so messaging is the preferred transport between microservices wherever possible. REST is used, but generally reserved just for exposing the microservice beyond the bounds of the application, or to the outside world.


