---
title: "09 - Implement SRE Principles"
---

Site Reliability Engineering (SRE) is basically what modern tech companies call ops.

The practice involves a mix of software development, knowledge of a variety of areas like networking stacks and technologies, in addition to computer hardware and performance.  SRE is keeping the lights on, efficiently, and knowing how to get the power back on when it fails.

Thankfully, because it is such an issue in modern tech companies, Google has done us a favor by writing an entire book on the topic that they make available for free online.

[Site Reliability Engineering](https://landing.google.com/sre/sre-book/toc/index.html) (also available in print from O'Reilly).

It is prudent to go through the book and come up with SRE plans for the software you build.  Make sure there is appropriate and *useful* documentation for how to run the services and fix common errors.  Do not create pointless compliance documentation, but rather straightforward things that developers and operations people will need in order to keep the lights on.

Consider these perspectives below:

## Thoughts from an SRE

1. Runbooks go out of date faster than anything. Therefore it is absolutely crucial to have the whole book on a single page and alerts vector to the proper subsection. Also pepper each section with a good set of keywords. This will allow users and newbies to easily search for procedures or related alerts when links invariably break.

1. Group related alerts ("host xyz down") in a single section with many section titles. One for each possible xyz.

1. Go ahead and put commandline commands in the runbook, in shell-command or code highlighted boxes (NEVER inside sentences). User defined fields should be delineated with $HOST etc (never <host>) and sample values for the vars given beforehand with sample output afterward. Never use a copyable $ to delineate shell commands. This creates the best possible user experience for people reusing your commands by cut and paste so they can more easily change values and so they know what to expect.

1. Link all relevant consoles in very small links (CPU usage in clusters: ym qf ij) including historical links to console views for past problems and how they look.

1. Section templates might look like this:

    >1.8. Too many cacheservers are down
    >
    >1.8.1 Definition. This means that 25% of the hosts (on average) have been down over the past 10 minutes
    >
    >1.8.2 Severity. Our load balancer will route all requests to surviving hosts and clients will retry on timeout so normally this is not severe (there is only a performance impact). However it could cascade due to RAM exhaustion or a query-of-death or due to a config push of broken software so assess the service right away for these problems.
    >
    >1.8.2 Remediation ... Rollback or resource scaling or bypassing the cache service on the command line ...

Google search SRE (williamDafoe on HN)