---
description: Codeclimate
keywords: codeclimate, coverage, service
title: Codeclimate
---

### WHAT IS CODE CLIMATE ?

In short: Code climate is tracking Coverage as-a-Service

Code Climate helps your team ship better code, faster, by incorporating fully-configurable static analysis and test coverage data into your development workflow.

Deep integration with pull request workflows immediately increases the visibility of code quality throughout your organization and gives your team the information they need to improve code quality with every commit.

Improved code quality means better maintainability, increased test coverage, fewer bugs, and more efficient code reviews – all of which make for a happier, more productive team.

### Duplication

https://docs.codeclimate.com/v1.0/docs/duplication-concept

Code Climate's [duplication engine](https://docs.codeclimate.com/v1.0/docs/duplication), at its heart, uses a fairly simple algorithm to decide which parts of your code are duplicated. First, source files are parsed into abstract syntax trees (ASTs). ASTs are made up of nodes: each node has a type (which might be something like "variable assignment" or "if statement"), and a set of values (which might be a variable name or another AST node representing a sub-expression). Each node is assigned a numerical mass, calculated as the number of sub-nodes plus 1

When looking for duplication, each node in each AST is compared to every other node in the parsed ASTs. Nodes have the same structure if they have the same type as each other, and if all of their sub-nodes also have the same structure. Nodes that have the same structure but different values (like 2 "variable assignment" nodes assigning variables with different names and types), are considered "similar". Nodes that have the same structure, and also have the same values are considered "identical".