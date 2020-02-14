---
title: "07 - Standardize Smartly"
---

Standards for development are very important because the reduced variation allows teams to execute repeatable processes more quickly.  In addition, standardization allows for teams to build and share a common body of knowledge and it decreases the onboarding time for new hires.

However, standards that are too strict and constrain the solution space unnecessarily lead to sub-optimal solutions to critical business problems.

These concerns must be balanced by standardizing smartly.  In other words, standardize on very basic and high-level things (like all systems my communicate by API) and do not create standards for things that are not actually critical to the solution (like a specific programming language or CI/CD tool).

This approach of abstract standardization was employed very well by Amazon in their API mandate, and similarly successful companies also standardize at generally the same level of detail.

Standardizing a process as mentioned previously is a good example of this.  If an effective process is designed and implemented, the particular tool used to fulfill the process requirements is usually not important.

Large organizations tend to over-standardize in a misguided attempt to maximize repeatability and minimize a variety of risks.  However, overly constraining the solution space for people who are actually building solutions is, in itself, a very big risk.

Therefore, standardize at the right level of detail and no more.

Examples of things that usually make sense to standardize in software:

* Programming patterns, idioms, style, and formatting for a particular language.  Use the standard approaches of the community wherever possible.

* High-level development processes like how version control will be used.  For example, is the GitFlow or GitHub Flow process being used?  Does every feature have a new branch?  Is code review required?

* Architecture patterns.  Example: all systems are only allowed to communicate by well-defined APIs with REST or gRPC.  That is an appropriate level of detail and makes some constraints on the solution space, but is still general enough to allow teams to build appropriately.

*  Data standards.  Example: all data must have a schema that can be used to understand the structure of the data and preserve its integrity.  This can be achieved in a variety of ways, like Protocol Buffers or JSON Schema, but does not mandate that all teams use a particular method of enforcing schemas.