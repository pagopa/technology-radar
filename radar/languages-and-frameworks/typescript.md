---
title: "TypeScript"
ring: adopt
quadrant: "languages-and-frameworks"
tags: [typescript]
---

[TypeScript](https://www.typescriptlang.org/) is a superset of JavaScript that adds static typing to the language. It transpiles to JavaScript, meaning that an application written in TypeScript will be executed in the Javascript runtime. The JavaScript runtime, whether it's a browser environment or Node.js, doesn't have direct awareness of the original TypeScript source code. It treats the transpiled JavaScript code just like any other JavaScript code.

The purpose of using TypeScript is for making it easier for developers to write safer and more maintainable code.
This is achieved by influencing the developer experience with several factors:

1. **Types help describe code**: Types act as a form of documentation within the code, providing explicit information about the expected data structures and formats. Developers can quickly understand the purpose and usage of functions and variables just by looking at their type annotations. This does not imply comments become obsolete; on the opposite, they can focus on explaing the design choices.
1. **Types require developers to reason about function inputs**: By specifying types for function parameters, TypeScript encourages developers to think about the valid input values a function can accept. This helps in designing functions that are more robust and resilient to unexpected input. Also, developers are often required to parse and validate input data to ensure it aligns with the expected types. This leads to more defensive programming practices, reducing the likelihood of runtime errors caused by unexpected data types or values.
1. **Types help to spot corner cases**: Types enable the identification of edge cases within the code, prompting developers to address and handle scenarios that might be overlooked. It leads to a more informed design of the application and to a better modeled domain.

Sometimes, working with types requires developers to deal with TypeScript-specific activities that have no direct impact on the transpiled code; developer communities often call this "type gymnastic".
We accept the effort as we believe the advantage for the produced applications and the developer experience are worth the investment.

### Use cases
TypeScript can be used with along side with other frameworks to create:
* web applications that run in the browser;
* mobile applications using `react-native`
* web services using Node.js

### Repositories using Typesctipt
On [our GitHub organization](https://github.com/pagopa?q=&type=all&language=typescript) there are applications actually written in TypeScript
