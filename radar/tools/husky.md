---
title: "Husky"
ring: adopt
quadrant: "tools"
tags: [git]
---

[Husky](https://typicode.github.io/husky/) is a tool that allows to easily
manage Git hooks. We use it in our projects to run scripts before committing or
pushing code. Husky supports all [client-side Git
hooks](https://git-scm.com/docs/githooks). It's easy to configure and use,
compared to Git hooks, and it's well documented.

Husky is specifically designed for Git hooks in JavaScript projects. Although it
can be extended to work with other languages through Node.js, it's primarily
JavaScript-oriented, using npm scripts for hooks and being an npm package itself.

Consider using `pre-commit` instead when:

- you need to support multiple languages
- you need to ensure that each hook runs in an isolated environment
- you need fine-grained control over how and hooks run

## Use cases

Run scripts before committing or pushing code to, for example:

- lint commit messages
- lint code
- run tests

## Reference of usage in our organization

A non exhaustive list of our projects that use Husky:

- [io-app](https://github.com/pagopa/io-app)
- [io-web-profile](https://github.com/pagopa/io-web-profile)
- [pagopa-editorial-components](https://github.com/pagopa/pagopa-editorial-components)
- [developer-portal](https://github.com/pagopa/developer-portal)
