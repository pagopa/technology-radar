---
title: "pre-commit"
ring: adopt
quadrant: "tools"
tags: [git]
---

[pre-commit](https://pre-commit.com/) is a framework for managing and
maintaining multi-language pre-commit hooks.It supports hooks written in any
language, not just JavaScript, making it versatile for projects using multiple
programming languages. 

- Has a good community with many shared hooks for various tools like linters,
  formatters, etc. 
- Requires Python to be installed on the system, but hooks can be in any language.

Consider using `husky` instead when you need a simpler setup, don't need to
support multiple languages and you are working on a JavaScript / Typescript
project.

## Use cases

* Ensuring code quality by running linters and formatters before committing code.
* Automating repetitive tasks to maintain code standards.

## Reference of usage in our organization

