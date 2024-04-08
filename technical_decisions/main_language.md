---
title: Main programming language
layout: default
parent: Technical decisions
nav_order: 1
---

During the initial planning phase of 'Neighbourhood' we debated between using JavaScript (which we were already familiar with) or switching to TypeScript.
JavaScript is a dynamically typed language, which means that variables are not assigned a specific data type when they are declared. Instead, the type of a variable is determined at runtime based on the type of value it is assigned. In statically typed languages, each variable must be assigned a specific data type when it is declared, and functions must specify the type of value they return.
In order to make a decision we had to carefully weigh the pros and cons and see if taking the time to learn TypeScript will pay off during the project's development.

### Advantages of TypeScript

- catches errors at compile-time, adding to the overall quality of the codebase and improving maintainability;
- defining types aids code readability;
- requires a slower, more deliberate approach to coding;

### Disadvantages of TypeScript

- the typing system can be difficult to properly implement and results in more lines of code;
- slower development due to having to define types and interfaces;
- external packages need to have a corresponding type package in order to work correctly.

According to the above pros and cons JavaScript is simpler and faster if you want to quickly prototype a feature, but overall we decided that the extra safety features provided by TypeScript were worth the time investment required to learn it.
