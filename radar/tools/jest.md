---
title: "Jest"
ring: hold
quadrant: "tools"
tags: [typescript, frontend, web, backend, testing]
---

[Jest](https://jestjs.io/) is a JavaScript Testing Framework with a focus on simplicity.

We choose to hold Jest because we are currently using it in our projects, but we are evaluating other testing frameworks like Vitest. Vitest offers support out of the box, and it's a good fit for our projects, while Jest requires some additional configuration (ie. ts-jest, etc.).

As Vitest offers compatibility with most of the Jest API and ecosystem libraries, so in most projects, it should be a drop-in replacement for Jest. Moreover, Vitest gives you a faster run for your unit tests and a jump in DX thanks to the default watch mode using Vite instant Hot Module Reload (HMR).
