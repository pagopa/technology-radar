---
title: "CommonJS"
ring: hold
quadrant: "languages-and-frameworks"
tags: [javascript, nodejs, typescript]
---

[CommonJS](https://nodejs.org/api/modules.html#modules-commonjs-modules) is a module system and module format that was originally designed for Node.js, allowing you to split JavaScript code into separate files and requiring them using the `require()` function. While it has been widely used in Node.js applications and was essential for the early development of the Node.js ecosystem, we recommend using ECMAScript Modules (ESM) instead for new projects.

## Reasons for Hold Status

1. **ESM is the Standard**: ECMAScript Modules is the official standardized module system for JavaScript, supported by modern browsers and Node.js. It provides a more consistent development experience across different environments.

2. **Better Static Analysis**: ESM's static module structure enables better tree-shaking (dead code elimination) and optimization by bundlers, while CommonJS's dynamic nature makes these optimizations more difficult.

3. **Asynchronous by Design**: ESM supports both synchronous and asynchronous module loading, while CommonJS is synchronous by nature, which can lead to performance bottlenecks.

4. **Interoperability Issues**: Using CommonJS alongside ESM can lead to interoperability challenges, especially in projects that use both module systems. Some tools and libraries may require additional configuration or transpilation steps.

## Working with ESM

When working with existing CommonJS projects:

1. Use the `.cjs` extension for CommonJS files and `.mjs` for ESM files to make the module system explicit
2. Add `"type": "module"` to your `package.json` to use ESM by default
3. For new modules within existing projects, prefer using ESM syntax:
   ```javascript
   // Instead of CommonJS
   const { foo } = require('bar');
   module.exports = { baz };

   // Use ESM
   import { foo } from 'bar';
   export { baz };
   ```

## Reference of usage in our organization

While we still maintain some legacy projects using CommonJS, all new TypeScript/JavaScript projects should use ESM. For existing projects using CommonJS, consider gradually migrating to ESM when making substantial changes to the codebase.
