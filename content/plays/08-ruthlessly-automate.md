---
title: "08 - Ruthlessly Automate"
---

Many organizations, especially those that see software development or technology as a cost center rather than a profit center, have a tendency of allocating more people to solving a problem or slow process when the correct answer is to focusing on automating that bottleneck.  This is especially true in organizations that also perceive themselves to have a lack of software development talent.

Automation is helpful not only for ensuring that more work is done in less time and with fewer errors, but also because it helps free up valuable human capacities for other work that cannot be automated.

From a software development perspective, things that should be automated include testing of all kinds, software builds, and non-functional testing like performance and load analysis.  These components of a software development process should be automated and run locally on the developer's machine or on the CI/CD server with every new commit of code to the master branch of the code repository.

While automation has excellent ROI, it is also the case that some technologists can automate prematurely.  Premature optimization is the root of all evil, as the saying goes, and this applies to automation as well.  Consider only automating a process if it is executed multiple times (e.g. running unit tests with pre-commit hooks) vs. a process that is relatively new and/or requires human involvement (e.g., code review).

If something will be done by multiple people, or will be done multiple times by the same person, consider whether or not it costs less to automate it vs. hiring and retaining a person to execute that process.  Include the fully-loaded cost of the person or people executing the process **in addition to** the opportunity cost of being slower, and making more mistakes, due to humans executing the process rather than machines.