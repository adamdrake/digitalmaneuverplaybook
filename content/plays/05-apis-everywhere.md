---
title: "05 - APIs Everywhere"
---

Of the many smart things that Amazon did in order to increase their speed and scale up their organization, dictating that all systems are only allowed to communicate by API was probably one of the most impactful.

Steve Yegge described it thusly:

    ...one day Jeff Bezos issued a mandate, sometime back around 2002 (give or take a year):

        * All teams will henceforth expose their data and functionality through service interfaces.

        * Teams must communicate with each other through these interfaces.

        * There will be no other form of inter-process communication allowed: no direct linking, no direct reads of another team’s data store, no shared-memory model, no back-doors whatsoever. The only communication allowed is via service interface calls over the network.

        * It doesn’t matter what technology they use.

        * All service interfaces, without exception, must be designed from the ground up to be externalizable. That is to say, the team must plan and design to be able to expose the interface to developers in the outside world. No exceptions.

    The mandate closed with:

        Anyone who doesn’t do this will be fired.  Thank you; have a nice day!

By mandating that systems only communicate by well-defined interfaces, and forbidding the interprocess communication and direct database connections that can often happen as organizations grow, Bezos ensured that the organization was building technology in a way that allowed it to scale to very large internal organizational structure sizes without creating stovepipes or a Big Ball of Mud architecture.

Well-defined interfaces are like contracts between systems.  Those interfaces allow systems of systems to be easily and independently constructed and altered without impacting other connected systems.

Ensure that all systems have industry standard APIs (e.g., gRPC, REST) and do not allow proprietary interfaces unless necessary by some design constraints.