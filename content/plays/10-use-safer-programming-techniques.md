---
title: "10 - Use Safer Programming Techniques"
---

# Coding standards

It's good to have consistent code standards and formatting to which everyone in the project adheres.  Different kinds of projects require different levels of correctness guarantees, so avoid creating one standard that applies to all projects.  In general though, strong and statically typed languages are preferable to weak and dynamically typed languages.

In addition, languages with consistent formatting like Go, Rust, and Python (via the Black formatter) are often preferable to languages that have more flexibility in formatting but without any significant benefit.

# Type checking and static analysis

There are a variety of programming techniques that can be used in order to increase the safety and security of the software you build.  For example, Facebook has an [excellent article on Zoncolan](https://dl.acm.org/doi/pdf/10.1145/3338112?download=true), their static analysis tooling.  Static analysis is the analysis of code as it sits in files, versus dynamic analysis that would analyze the code while it is running.  In this case, Facebook found that static analysis was one of the most helpful methods in finding security vulnerabilities and bugs in their code, even more so than read teaming/white hat hacking.

In order to get maximum use of static analysis techniques, it is beneficial to use a programming language that is statically typed, or to use a dynamic language that allows for type annotations.

Example languages to use:

* Go
* Python (with type annotations and [Pyre]() or [mypy]() type checker)
* Rust
* TypeScript (a superset of JavaScript that allows for type checking)
* C#
* Java

It is preferable to stay away from fully dynamic and weakly typed languages like JavaScript since the rules of that programming language make it easier to create bugs in software.  The counterargument for this will be that increased automated testing will catch those bugs, but that counterargument is both false and wasteful.  Why rely on a programmer to write tests to look for certain bugs when a compiler or type checker has already been created to do those things, and more?