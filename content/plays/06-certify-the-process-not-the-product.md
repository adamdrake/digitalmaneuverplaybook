---
title: "06 - Certify the Process Not the Product"
---

In a large organization that produces software, there may be hundreds of teams doing thousands of deployments every single day.  Each of these teams needs both the autonomy to operate independently and quickly and also needs to have appropriate constraints on the tools and technologies they are allowed to use.  This provides maximum benefit to the organization with an appropriate reduction in risk.

In order to accomplish this appropriately, focus on certifying or approving the higher level processes themselves rather than the tools used for following those processes.  This is especially true in software development where there can be significant differences in the ease with which a problem can be solved with some tools or architectures rather than others.

As an example, the process below could be certified/approved for building software in a larger organization.  Note that even in cases where specific tools are listed, there are multiple tools that could all be used to solve the same problem.  This allows for appropriate flexibility.

----

* All development will be done using a version control system.  The version control system must support branches.  When developing a new feature it will be done in a new branch and that branch can be merged into the master branch after it has been reviewed.

* Before merging code into the master branch it will be reviewed by another team member or competent software developer.  The master branch will be considered equivalent to the production branch of the software, and production deployments will only come from the master branch via CI/CD pipelines.

* All code will have appropriate unit tests and integration tests.  This will be defined as > 85% test coverage for all unit tests, for example.  Empty/blank passing tests will be avoided due to code review as specified above.

* All linting/formatting and unit tests will be run locally on the deveoper's machine before committing to the feature branch.  If using git, for example, these checks will be done as a pre-commit hook in order to ensure that no code that has failing tests or formatting problems will be committed.

* In addition to automated unit and integration testing, all software will undergo automated security scans as part of the CI/CD process.

* The following tools are approved:

        Program languages: Go, Python (with type annotations), Rust, Java, JavaScript (via TypeScript)
        Database: SQLite, PostgreSQL
        Web server: nginx
        Caches: Redis, memcached
        Version control: git
        Hosted version control platform: GitHub, GitLab, Gitea
        CI/CD: GitHub Actions, TravisCI, CircleCI, Jenkins

Any tooling not in this list is only usable with specific permission.

* All software built on cloud infrastructure must be built in such a way so as not to make use of any vendor-specific services.  Building software with services specific to a particular cloud provider is not permitted.

----

It is possible to write a high-level process like the above that ensures reasonable standardization and security while also not being overly burdensome to software developers.  This allows the organization to manage and mitigate risk without incurring the risk of opportunity cost because developers are constantly blocked by compliance and authorization issues.